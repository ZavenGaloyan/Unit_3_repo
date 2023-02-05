 # PYTHON Code
 ```.py
 from kivymd.app import MDApp

class Quiz_039(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0
    def build(self):
        return
    def increase(self):
        self.count += 1
        self.root.ids.my_label.text = f" Count {self.count}"
m = Quiz_039()
m.run()
```
 # KIVY Code
 ```.py
 Screen:
    size:500,500 #width, height
    MDBoxLayout:
        orientation: "horizontal"
        size_hint: 0.7, 0.3 #percentages of the screen
        pos_hint:{"center_x":0.5, "center_y":0.5}
        MDLabel:
            id: my_label
            halign: "center"
            text: "Count"
            size_hint: 0.5,1
            font_size: 34
            pos_hint:{"center_x":0.75, "center_y":0.5}
        MDRaisedButton:
            id: my_button
            text: "Add +1"
            size_hint: 0.5,1
            md_bg_color: 0,34,10,0
            pos_hint:{"center_x":0.75, "center_y":0.5}
            font_size: 34
            on_release:
                app.increase()
```
## Code Evidence
![]()
