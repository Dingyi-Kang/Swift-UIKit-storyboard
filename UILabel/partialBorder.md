              extension CALayer {

                  func addBorder(edge: UIRectEdge, color: UIColor, thickness: CGFloat) {

                      let border = CALayer()

                      switch edge {
                      case UIRectEdge.top:
                          border.frame = CGRect(x: 0, y: 0, width: self.frame.width, height: thickness)
                          break
                      case UIRectEdge.bottom:
                          border.frame = CGRect(x: 0, y: self.frame.height - thickness, width: self.frame.width, height: thickness)
                          break
                      case UIRectEdge.left:
                          border.frame = CGRect(x: 0, y: 0, width: thickness, height: self.frame.height)
                          break
                      case UIRectEdge.right:
                          border.frame = CGRect(x: self.frame.width - 2*thickness, y: 0, width: thickness, height: self.frame.height)
                          break
                      default:
                          break
                      }

                      border.backgroundColor = color.cgColor;

                      self.addSublayer(border)
                  }

              }
              
              
              
 <img width="585" alt="image" src="https://user-images.githubusercontent.com/81428296/209449397-94e2fa1a-06e2-448e-b0ce-5dbedd7913ca.png">
