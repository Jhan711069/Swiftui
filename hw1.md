<h1>hw1</h1>
<table>
  <tr>
    <td>
  ```swift
      import SwiftUI

struct ContentView: View {
    var body: some View {
        ZStack{
            Image("BG3")
                .resizable()
                .aspectRatio(contentMode: .fill)
                .opacity(0.7)
                .frame(width: 780, height: 100, alignment: .center)
            Text("   姓名：詹承羲")
                .font(.title)
                .frame(width: 300, height: 70, alignment: .leading)
                .background(Color.primary)
                .cornerRadius(30)
                .position(x: 350, y: 210)
                .foregroundColor(.black)
                .opacity(0.68)
                .bold()            
            Text("   學號：1103318")
                .font(.title)
                .frame(width: 300, height: 70, alignment: .leading)
                .background(Color.primary)
                .cornerRadius(30)
                .position(x: 350, y: 300)
                .foregroundColor(.black)
                .opacity(0.68)
                .bold()            
            Text("   興趣：打排球")
                .font(.title)
                .frame(width: 300, height: 70, alignment: .leading)
                .background(Color.primary)
                .cornerRadius(30)
                .position(x: 350, y: 390)
                .foregroundColor(.black)
                .opacity(0.68)
                .bold()          
            Image(systemName: "figure.volleyball")
                .foregroundColor(Color.black)
                .font(.system(size: 50))
                .position(x: 430, y: 390)            
           }
        .overlay(
            Text("能坐就不站,\n能躺就不坐")
                .font(.system(size:35))
                .bold()
                .frame(width: 300, height: 90, alignment: .center)
                .foregroundColor(.black)
                .background(Color.primary)
                .opacity(0.7)
                .cornerRadius(30)
            ,
            alignment: .bottom
        )
    }
}
 ```
    </td>
  </tr>
     <img src="https://raw.githubusercontent.com/Jhan711069/Swiftui/main/IMG_0022.jpeg">
</table>
