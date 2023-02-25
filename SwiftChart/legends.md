    let legendEntry1 = LegendEntry(label: "After Explosure")
    let legendEntry2 = LegendEntry(label: "After Response Prevention")
    let legendEntry3 = LegendEntry(label: "Difference")
    legendEntry1.form = .circle
    legendEntry2.form = .circle
    legendEntry3.form = .default
    legendEntry1.formColor = UIColor(named: "blueBlack")
    legendEntry2.formColor = UIColor(named: "blue")
    combinedChartView.legend.setCustom(entries: [legendEntry1, legendEntry2, legendEntry3])
    
    
## if want to use custom legends and disable build-in legends
    combinedChartView.legend.enabled = false
