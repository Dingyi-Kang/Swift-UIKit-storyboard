
    combinedChartView.rightAxis.enabled = false
    combinedChartView.xAxis.labelPosition = .bottom
    combinedChartView.xAxis.drawGridLinesEnabled = false
    yLabel.transform = CGAffineTransform(rotationAngle: -CGFloat.pi / 2)
    combinedChartView.xAxis.valueFormatter = CustomAxisFormatter()
    //MARK: this can avoid the half cover of the triangle at the edges
    combinedChartView.xAxis.axisMinimum = 0.5
    combinedChartView.xAxis.axisMaximum = xV+0.5
    combinedChartView.xAxis.labelCount = Int(xV)
    
## note: the inputs of x and y are double, hence, to display the x, y axis labels we want, like integer, literal strings(month), we need to create our custom IndexAxisValueFormatter 
    class CustomAxisFormatter:IndexAxisValueFormatter{
        override func stringForValue(_ value: Double, axis: AxisBase?) -> String {
            let roundValue = Int(value)
            return Double(roundValue) == value ? "\(roundValue)" : ""
        }
    } 
