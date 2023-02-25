## Note 1: if want to triangular marker, we cannot use lineChartView (which only supports circle marker). We should use scatterChartView
## note 2: to integrate scatterChartView and lineChartView, others, we need to combinedChartView instead

    var afterExpValEntries = [ChartDataEntry]()
    var afterHabValEntries = [ChartDataEntry]()
    var diffHabValEntries = [ChartDataEntry]()

    //TODO: share via pdf
    var x = 0.0
    for s in practice.hasSessions! {
        x += 1
        let session = s as! Session
        afterExpValEntries.append(ChartDataEntry(x: x, y: Double(session.afterExposureValInt)))
        afterHabValEntries.append(ChartDataEntry(x: x, y: Double(session.afterHabituationValInt)))
        diffHabValEntries.append(ChartDataEntry(x: x, y: Double(session.difference)))
    }

    let set1 = LineChartDataSet(entries: afterExpValEntries)
    let set2 = LineChartDataSet(entries: afterHabValEntries)
    let set3 = ScatterChartDataSet(entries: diffHabValEntries)

    set1.colors = [UIColor(named: "blueBlack")!]
    set2.colors = [UIColor(named: "blue")!]
    set3.colors = [UIColor(named: "grayBlue")!]
    set1.drawValuesEnabled = false
    set2.drawValuesEnabled = false
    set3.drawValuesEnabled = false

    set1.circleRadius = 5.0
    set1.circleHoleRadius = 0
    set1.circleColors = [UIColor(named: "blueBlack")!]

    set2.circleRadius = 5.0
    set2.circleHoleRadius = 0
    set2.circleColors = [UIColor(named: "blue")!]

    set3.setScatterShape(.triangle)
    set3.scatterShapeSize = 12.0


    let scatterData = ScatterChartData(dataSet: set3)
    let lineData = LineChartData(dataSets: [set1, set2])
    let combinedData = CombinedChartData()
    combinedData.lineData = lineData
    combinedData.scatterData = scatterData

    combinedChartView.data = combinedData
