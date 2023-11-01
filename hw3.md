<h1>hw3</h1>

```swift


  import SwiftUI
struct ContentView:View{
    var body:some View{
        
        ZStack{
            Image("Back")
                .resizable()
            VStack(spacing:120){
                HStack(spacing:80){
                    p1View()
                    p2View()
                    p3View()
                }
                .padding(.top,-30)
                HStack(spacing:80){
                    p4View()
                    p5View()
                    p6View()
                }
                .padding(.leading,15)
                HStack(spacing:80){
                    p7View()
                    p8View()
                    p9View()
                }
                .padding(.bottom,-50)
            }
            
        }
    }
}
struct p1View: View {
    var body: some View {
        VStack {
            Image("P1")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 200,height: 100,alignment: .center)
                .position(x:100,y: 150)
        }
    }
}
struct p2View:View{
    var body:some View{
        VStack{
            Image("P2")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 200,height: 100,alignment: .center)
                .position(x:70,y: 150)
        }
    }
}
struct p3View:View{
    var body:some View{
        VStack{
            Image("P3")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 200,height: 100,alignment: .center)
                .position(x:35,y: 150)
        }
    }
}
struct p4View:View{
    var body:some View{
        VStack{
            Image("P4")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 200,height: 100,alignment: .center)
                .position(x:85,y: 60)
        }
    }
}
struct p5View:View{
    var body:some View{
        VStack{
            Image("P5")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 600,height: 120,alignment: .center)
                .position(x:60,y: 60)
        }
    }
}
struct p6View:View{
    var body:some View{
        VStack{
            Image("P6")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 150,height: 100,alignment: .center)
                .position(x:30,y: 60)
        }
    }
}
struct p7View:View{
    var body:some View{
        VStack{
            Image("P7")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 200,height: 100,alignment: .center)
                .position(x:100,y: 10)
        }
    }
}
struct p8View:View{
    var body:some View{
        VStack{
            Image("P8")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 150,height: 100,alignment: .center)
                .position(x:70,y: 10)
        }
    }
}
struct p9View:View{
    var body:some View{
        VStack{
            Image("P9")
                .resizable()
                .aspectRatio( contentMode: .fit)
                .frame(width: 150,height: 100,alignment: .center)
                .position(x:30,y: 10)
        }
    }
}

```

img src="https://raw.githubusercontent.com/Jhan711069/Swiftui/main/IMG_0050.jpeg">
