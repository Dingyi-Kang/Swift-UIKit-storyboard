// Container view:

let radioView = UIView()

addSubview(radioView)

let radioButton = UIButton()

radioView.addSubview(radioButton)

let radioImage = UIImageView()

radioView.addSubview(radioImage)

radioImage.layer.cornerRadius = 7

if selected {

    radioImage.layer.borderColor = UIColor.blue.cgColor

    radioImage.backgroundColor = .blue

    radioImage.image = UIImage(systemName: "smallcircle.fill.circle")

    radioImage.tintColor = .white

} else {

    radioImage.layer.borderColor = UIColor.gray.cgColor

    radioImage.backgroundColor = .clear

    radioImage.image = nil

}

My code example:

Associaed link: https://prograils.com/swift-tutorial-radio-button-pure-code
