Link: https://stackoverflow.com/questions/37370801/how-to-add-a-container-view-programmatically
            
            
            
                      override func viewDidLoad() {
                          super.viewDidLoad()

                          // add container

                          let containerView = UIView()
                          containerView.translatesAutoresizingMaskIntoConstraints = false
                          view.addSubview(containerView)
                          NSLayoutConstraint.activate([
                              containerView.leadingAnchor.constraint(equalTo: view.leadingAnchor, constant: 10),
                              containerView.trailingAnchor.constraint(equalTo: view.trailingAnchor, constant: -10),
                              containerView.topAnchor.constraint(equalTo: view.topAnchor, constant: 10),
                              containerView.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -10),
                          ])

                          // add child view controller view to container

                          let controller = storyboard!.instantiateViewController(withIdentifier: "Second")
                          addChild(controller)
                          controller.view.translatesAutoresizingMaskIntoConstraints = false
                          containerView.addSubview(controller.view)

                          NSLayoutConstraint.activate([
                              controller.view.leadingAnchor.constraint(equalTo: containerView.leadingAnchor),
                              controller.view.trailingAnchor.constraint(equalTo: containerView.trailingAnchor),
                              controller.view.topAnchor.constraint(equalTo: containerView.topAnchor),
                              controller.view.bottomAnchor.constraint(equalTo: containerView.bottomAnchor)
                          ])

                          controller.didMove(toParent: self)
                      }
