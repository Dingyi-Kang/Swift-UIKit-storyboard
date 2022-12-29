link of post: https://stackoverflow.com/questions/72338658/firebase-auth-and-firestone-error-code-in-swift

<img width="674" alt="image" src="https://user-images.githubusercontent.com/81428296/209899948-6725cbde-cdbb-41af-8806-f2206f606283.png">


### official doc on meanings of different errors
https://firebase.google.com/docs/auth/ios/errors#firauth


### My code:

    func handleResults(error:Error)->String{
        
        let err = error as NSError
        
        switch err.code {
            
        case AuthErrorCode.emailAlreadyInUse.rawValue:
            return "This email is already in use. Please use another email."
        case AuthErrorCode.weakPassword.rawValue:
            return "Password is too weak. Please use a strong one"
            
        case AuthErrorCode.userNotFound.rawValue:
            return "User is not found. Please try another email."
        case AuthErrorCode.wrongPassword.rawValue:
            return "Wrong password. Please try a different password."
        case AuthErrorCode.invalidEmail.rawValue:
            return "Invalid email"
        case AuthErrorCode.accountExistsWithDifferentCredential.rawValue:
            return "accountExistsWithDifferentCredential"
            
        default:
            return "unknown error: \(err.localizedDescription)"
        }
        
    }
