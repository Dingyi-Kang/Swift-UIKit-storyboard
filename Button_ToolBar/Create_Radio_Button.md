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
![image](https://user-images.githubusercontent.com/81428296/147296255-627cbba9-0166-4a94-bf4d-7fbf05da850b.png)


Associaed link: https://prograils.com/swift-tutorial-radio-button-pure-code
