
<h1>hw2</h1>
<p>內容介紹：雙人猜拳遊戲並顯示勝負</p>

```swift

      import SwiftUI

struct ContentView: View {
    @State var randomInt1:Int = 0
    @State var randomInt2:Int = 0    
    @State var str1 = ["準備","👊","🖐️","✌️"]
    @State var str2 = ["準備","👊","🖐️","✌️"]
    @State var result = ""
    var body: some View {
        Button(action:{self.randomInt2 = Int.random(in: 1...3)
            checkWinner()
        }, label: {
            Text("A Go")
                .frame(width: 180,height: 80, alignment: .center)
                .font(.system(size:40))
                .bold()
                .background(Color.gray)
                .foregroundColor(.black)
                .cornerRadius(50)
                .position(x:190,y: 70)
                .rotationEffect(.degrees(180))
        })
        Text(String(str2[randomInt2]))
            .font(.system(size:90))
            .bold()
            .foregroundColor(.red)
            .position(x: 190,y:100)
            .rotationEffect(.degrees(180))
            .buttonStyle(BorderlessButtonStyle())
        Text(result)
            .font(.system(size: 30))
            .bold()
            .foregroundColor(.yellow)
            .frame(width: 200,height: 100,alignment: .center)
            .background(Color.black)
            .cornerRadius(20)
        Text(String(str1[randomInt1]))
            .font(.system(size:100))
            .bold()
            .foregroundColor(.red)
            .position(x:190,y:160)
        Button(action:{self.randomInt1 = Int.random(in: 1...3)
            checkWinner()
        }, label: {
            Text("B Go")
                .frame(width: 180,height: 80, alignment: .center)
                .font(.system(size:40))
                .bold()
                .background(Color.gray)
                .foregroundColor(.black)
                .cornerRadius(50)
                .position(x:190,y: 140)
        })
        .buttonStyle(BorderlessButtonStyle())
    }
    func checkWinner() {
        let playerAChoice = randomInt1
        let playerBChoice = randomInt2
        
        if (playerAChoice == playerBChoice) || (playerAChoice == 0 || playerBChoice == 0) {
            result = "平手"
        } else if (playerBChoice == 1 && playerAChoice == 3) ||
                    (playerBChoice == 2 && playerAChoice == 1) ||
                    (playerBChoice == 3 && playerAChoice == 2) {
            result = "A Win！"
        } else {
            result = "B Win！"
        }
    }
}




```

<img src="https://raw.githubusercontent.com/Jhan711069/Swiftui/main/hw2_video.gif">
