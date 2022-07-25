you make the VC the delegate of UIScrollView
<img width="1481" alt="image" src="https://user-images.githubusercontent.com/81428296/180816851-e5474d94-b062-43d3-b2a8-e73c2c138e72.png">
official doc: https://developer.apple.com/documentation/uikit/uiscrollviewdelegate/1619392-scrollviewdidscroll

the code to detect if the far right of the horizaontal scroll view is detected (if reach the end, reset the scale and location):

        func scrollViewDidScroll(_ scrollView: UIScrollView) {
                let width = scrollView.frame.size.width
                   let contentXoffset = scrollView.contentOffset.x
                   let distanceFromFarRight = scrollView.contentSize.width - contentXoffset
                   if distanceFromFarRight < width {
                           print(" you reached the end")
                           guard currChartDataSetIndex + 1 < chartsDataSets.count else{return}
                           currChartDataSetIndex += 1
                           self.lineChartView.zoomToCenter(scaleX: 0, scaleY: 0)
                           self.scrollView.setContentOffset(CGPoint.zero, animated: true)
                           //self.setChartData(lineChartView: lineChartView, yValues: chartsDataSets[currChartDataSetIndex])
                   }
            }
