<h1>bonus</h1>

```swift

      import SwiftUI

struct ContentView: View {
    let displayFontype = [".default",".rounded",".monospaced",".serif"]
    @State var displayFontSelected = 0
    @State var IsDeepScheme = false
    @State var colorArray = [255.0,255.0,255.0]
    @State var stepperValue = 0
    @State var sliderValue = 0.0
    @State var DateSelect = Date()
    @State var isDatePickerPresented = false
    var body: some View {
        NavigationView{
            Form(content: {
                Section(header: Text("字型設定"), content: {
                    Picker(selection: $displayFontSelected,
                           label: Text("字型選擇(\(displayFontSelected))"),
                           content: {
                        ForEach(0..<displayFontype.count,
                                id: \.self,
                                content:{
                            Text(self.displayFontype[$0])
                        })
                    })
                })
                Section(header: Text("背景風格"),
                        content: {
                    Toggle(isOn: $IsDeepScheme,
                           label: {Text("深色(\(String(IsDeepScheme)))")
                    })
                })
                Section(header: Text("計數器")){
                    Stepper("Stepper(\(stepperValue))",
                            onIncrement: {stepperValue+=1},
                            onDecrement: {stepperValue-=1})
                }
                Section(header: Text("滑桿(\(sliderValue, specifier:"%.2f"))")){
                    Slider(value: $sliderValue, in: 0...1)
                }
                Section(header: Text("Date Select")){
                    Button(action: {
                        isDatePickerPresented.toggle()
                    }) {
                        Text("Select Date")
                    }
                }
            })
            .navigationTitle("Settings 設定")
            .sheet(isPresented: $isDatePickerPresented, content: {
                    DatePicker("Select Date", selection: $DateSelect, displayedComponents: .date)
                        .datePickerStyle(GraphicalDatePickerStyle())
                        .onChange(of: DateSelect) { newValue in
                            print("Date: \(newValue)")
                        }
            })
        }
    }
}


```

<img src="https://raw.githubusercontent.com/Jhan711069/Swiftui/main/Bonus.gif">
