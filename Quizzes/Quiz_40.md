 # PYTHON Code
 ```.py
 from kivymd.app import MDApp
class Quiz_040(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
    def build(self):
        return
    def change_appearance(self):
        print(self.root.ids.main_screen.md_bg_color)
        if self.root.ids.main_screen.md_bg_color == [1.0, 1.0, 1.0, 1.0]:
            self.root.ids.main_screen.md_bg_color = "#000000"
            self.root.ids.changebutton.text_color = 1,1,1,1
            self.root.ids.name.text_color = 1, 1, 1, 1
            self.root.ids.changebutton.text = "Light Mode"
        else:
            self.root.ids.main_screen.md_bg_color = "#FFFFFF"
            self.root.ids.changebutton.text_color = 0,0,0,1
            self.root.ids.name.text_color = 0, 0, 0, 1
            self.root.ids.changebutton.text = "Dark Mode"

test = Quiz_040()
test.run()
```
# KIVY Code
```.py
MDScreen:
    size:500,500
    MDBoxLayout:
        id: main_screen
        orientation:"vertical"
        md_bg_color: "#FFFFFF"
        MDLabel:
            id:name
            text: "Zaven Galoyan"
            halign: "center"
            font_style: "H3"
            theme_text_color: "Custom"
            text_color: 0, 0, 0, 1
            pos_hint: {"center_x": .5, "center_y": .5}
        MDRaisedButton:
            id: changebutton
            text: "Dark Mode"
            pos_hint: {"center_x": 0.06, "center_y": 0.1}
            on_release: app.change_appearance()
```
 ## CODE Evidence
 ![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Quizzes/Quiz-040.jpg)
 ![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Quizzes/Quiz-040_1.jpg)
