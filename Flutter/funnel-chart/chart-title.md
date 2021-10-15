---
layout: post
title: Chart title in Flutter Funnel Chart widget | Syncfusion 
description: Learn here all about Chart title feature of Syncfusion Flutter Funnel Chart (SfFunnelChart) widget and more.
platform: flutter
control: Chart
documentation: ug
---

# Chart title in Flutter Funnel Chart (SfFunnelChart)

You can define and customize the Chart title using [`title`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/SfFunnelChart/title.html) property of [`SfFunnelChart`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/SfFunnelChart-class.html). The [`text`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle/text.html) property of [`ChartTitle`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle-class.html) is used to set the text for the title. 

Following properties can be used to customize its appearance.

* [`backgroundColor`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle/backgroundColor.html) - used to change the background color.
* [`borderColor`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle/borderColor.html) - used to change the border color.
* [`borderWidth`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle/borderWidth.html) - used to change the border width.
* [`textStyle`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle/textStyle.html) - used to change the text color, size, font family, fontStyle, and font weight.
* [`color`](https://api.flutter.dev/flutter/painting/TextStyle/color.html) - used to change the color of the text.
* [`fontFamily`](https://api.flutter.dev/flutter/painting/TextStyle/fontFamily.html) - used to change the font family for chart title. 
* [`fontStyle`](https://api.flutter.dev/flutter/painting/TextStyle/fontStyle.html) - used to change the font style for the chart title.
* [`fontSize`](https://api.flutter.dev/flutter/painting/TextStyle/fontSize.html) - used to change the font size for the chart title.

### Title Alignment

You can align the title text content horizontally to the near, center or far of the chart using the [`alignment`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/ChartTitle/alignment.html) property of the [`title`](https://pub.dev/documentation/syncfusion_flutter_charts/latest/charts/SfFunnelChart/title.html).

{% highlight dart %} 

      @override
      Widget build(BuildContext context) {
        return Scaffold(
          body: Center(
            child: Container(
              child: SfFunnelChart(
                title: ChartTitle(
                  text: 'Half yearly sales analysis',
                  backgroundColor: Colors.lightGreen,
                  borderColor: Colors.blue,
                  borderWidth: 2,
                  // Aligns the chart title to left
                  alignment: ChartAlignment.near,
                  textStyle: TextStyle(
                    color: Colors.red,
                    fontFamily: 'Roboto',
                    fontStyle: FontStyle.italic,
                    fontSize: 14,
                  )
                ),
                // Initialize category axis
                series: FunnelSeries<SalesData, String>(
                    dataSource: [
                      // Bind data source
                      SalesData('Jan', 35),
                      SalesData('Feb', 28),
                      SalesData('Mar', 34),
                      SalesData('Apr', 32),
                      SalesData('May', 40)
                    ],
                    xValueMapper: (SalesData sales, _) =>   sales.year,
                    yValueMapper: (SalesData sales, _) => sales.sales
                  )
              )
            )
          )
        );
      }

{% endhighlight %}

![Chart title](images/chart-title/chart_title.png)