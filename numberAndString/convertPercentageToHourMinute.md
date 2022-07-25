<img width="715" alt="image" src="https://user-images.githubusercontent.com/81428296/180839725-4244ca93-9cca-4c9e-ae77-1feae2eeaddb.png">


        func getTime(val:CGFloat)->String{

                let newVal = Int(round(val*24*60))

                let hour = newVal / 60

                let minutes = newVal % 60

                if hour < 12 {
                    return String(format: "%i:%02i AM", hour, minutes)
                }else{
                    return String(format: "%i:%02i PM", hour - 12, minutes)
                }

            }
