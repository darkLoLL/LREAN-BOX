```cpp
// 新建一个QChart类
chart = new QChart;
// 新建一个数据系列
scatterSeries = new QScatterSeries;
// 新建x和y轴
xi = new QValueAxis;  
yi = new QValueAxis;  
  
xi->setRange(0, 5);  
yi->setRange(-1.5, 1.5);  
  
chart->addSeries(scatterSeries);  
chart->addAxis(xi, Qt::AlignmentFlag::AlignBottom);  
chart->addAxis(yi, Qt::AlignmentFlag::AlignRight);  
  
scatterSeries->attachAxis(xi);  
scatterSeries->attachAxis(yi);  
  
for (int i = 0; i < 100; ++i) {  
    scatterSeries->append(0.0614 * i, sin(0.0614 * i));  
}  
  
chartView = new QChartView;  
chartView->setChart(chart);  
chartView->show();  
```