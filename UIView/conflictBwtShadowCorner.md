Normally, a UIView can make corner and makeShadow without conflicts (UIKit handle that for you)

However, if you want to make corner and shadows of an embedded views, you will have to explicitly make maskToBounds true, which will make corner visible while clip the shadow

So, to draw the shadow, we need an underline shadow view. Of course, to we also need to corner this shadow view or make its background color be clear
