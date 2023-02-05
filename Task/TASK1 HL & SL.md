 # TASK1 CREATING VARIOUS CONVERTERS
 ## SL YEN TO USD CONVERTER
```.py
from kivy.lang import Builder
from kivymd.app import MDApp


class Currency_converter(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)


    def build(self):
        self.theme_cls.theme_style = "Light"
        self.theme_cls.primary_palette = "Blue"
        return Builder.load_file('Currency_converter.kv')

    def USD_YEN(self):
        self.output_amount = self.root.ids.Converted.text
        self.input_amount = self.root.ids.user.text
        self.Total = 0
        if self.input_amount.isdigit():
            self.Total = f"{int(self.input_amount)*130}¥"
            print(self.Total)
        else:
            self.output_amount = "Enter Posative value"


    def YEN_USD(self):
        self.output_amount = self.root.ids.Converted.text
        self.input_amount = self.root.ids.user.text
        self.Total = 0
        if self.input_amount.isdigit():
            self.Total= f"{int(self.input_amount)/130}$"
            print(type(self.input_amount))
        else:
            self.Total = "Enter Positive value"


    def convert(self):
        self.root.ids.Converted.text = f"TOTAL:{self.Total}"

m = Currency_converter()
m.run()
```
 ### KIVY FILE
```.py
Screen:

    MDCard:
        size_hint: None, None
        size: 700, 500
        pos_hint: {"center_x": 0.5, "center_y": 0.5}
        elevation: 10
        padding: 25
        spacing: 25
        orientation: 'vertical'

        MDLabel:
            id: welcome_label
            text: "Currency Converter"
            font_size: 40
            halign: 'center'
            size_hint_y: None
            height: self.texture_size[1]
            padding_y: -5

        MDTextField:
            id: user
            hint_text: "Amount"
            icon_right: "dollar"
            size_hint_x: None
            halign: 'left'
            width: 200
            font_size: 60
            pos_hint: {"center_x": 0.19,"center_y":1}

        MDRoundFlatButton:
            icon: "currency-jpy"
            text: "YEN to USD"
            font_size: 25
            pos_hint: {"center_x": 0.5}
            halign: 'left'
            theme_text_color: "Custom"
            text_color: "red"
            line_color: "red"
            theme_icon_color: "Custom"
            icon_color: "blue"
            halign: 'left'
            on_press: app.YEN_USD()

        MDRoundFlatButton:
            icon: "currency-usd"
            text: "USD to YEN"
            font_size: 25
            pos_hint: {"center_x": 0.5}
            theme_text_color: "Custom"
            text_color: "blue"
            line_color: "blue"
            theme_icon_color: "Custom"
            icon_color: "blue"
            on_press: app.USD_YEN()

        MDRectangleFlatIconButton:
            icon: "cash-plus"
            text: "Convert"
            pos_hint: {"center_x": 0.5}
            theme_text_color: "Custom"
            text_color: "black"
            line_color: "black"
            theme_icon_color: "Custom"
            icon_color: "blue"
            font_size: 20
            on_press: app.convert()

        MDLabel:
            id: Converted
            text: "Total:"
            font_size: 40
            halign: 'left'
            size_hint_y: None
            height: self.texture_size[1]
            padding_y: 1

```
 # EVIDENCE
![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Task/SL_CONVERTER.jpg)
### HL part
```.py
from kivy.lang import Builder
from kivymd.app import MDApp


class Bites_converter(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)


    def build(self):
        self.theme_cls.theme_style = "Light"
        self.theme_cls.primary_palette = "Blue"
        return Builder.load_file('Bites_converter.kv')

    def MEGA(self):
        print("HELLO")
        self.output_amount = self.root.ids.Final_Conversion.text
        self.input_amount = self.root.ids.USER_INPUT.text
        print(self.input_amount)
        if self.input_amount.isdigit():
            self.root.ids.Final_Conversion.text = f" MEGA {(int(self.root.ids.USER_INPUT.text)/8)/1_000_000} BITES"
        else:
            self.output_amount = "Enter Positive value"

    def KILO(self):
        self.output_amount = self.root.ids.Final_Conversion.text
        self.input_amount = self.root.ids.USER_INPUT.text
        if self.input_amount.isdigit():
            self.root.ids.Final_Conversion.text = f"KILO {(int(self.input_amount)/8)/1_000} BITES"
        else:
            self.output_amount = "Enter Positive value"
    def GIGA(self):
        self.output_amount = self.root.ids.Final_Conversion.text
        self.input_amount = self.root.ids.USER_INPUT.text
        if self.input_amount.isdigit():
            self.root.ids.Final_Conversion.text = f"GIGA {(int(self.input_amount)/8)/1_000_000_000} BITES"
        else:
            self.output_amount = "Enter Positive value"
    def TERA(self):
        self.output_amount = self.root.ids.Final_Conversion.text
        self.input_amount = self.root.ids.USER_INPUT.text
        if self.input_amount.isdigit():
            self.root.ids.Final_Conversion.text = f"TERA {(int(self.input_amount)/8)/1_000_000_000_000} BITES"
        else:
            self.output_amount = "Enter Positive value"
    def PETA(self):
        self.output_amount = self.root.ids.Final_Conversion.text
        self.input_amount = self.root.ids.USER_INPUT.text
        if self.input_amount.isdigit():
            self.root.ids.Final_Conversion.text = f"PETA {(int(self.input_amount)/8)/1_000_000_000_000_000} BITES"
        else:
            self.output_amount = "Enter Posative value"
    def EXTA(self):
        self.output_amount = self.root.ids.Final_Conversion.text
        self.input_amount = self.root.ids.USER_INPUT.text
        if self.input_amount.isdigit():
            self.root.ids.Final_Conversion.text = f"EXTA {(int(self.input_amount)/8)/1_000_000_000_000_000_000} BITES"
        else:
            self.output_amount = "Enter Positive value"

m = Bites_converter()
m.run()
```
 ### KIVY FILE
```.py
Screen:

    MDCard:
        size_hint: None, None
        size: 700, 500
        pos_hint: {"center_x": 0.5, "center_y": 0.5}
        elevation: 10
        padding: 25
        spacing: 25
        orientation: 'horizontal'

    MDLabel:
        id: welcome_label
        text: "Bites to Bytes"
        font_size: 40
        halign: 'center'
        size_hint_y: None
        height: self.texture_size[1]
        padding_y: 480

    MDTextField:
        id: USER_INPUT
        hint_text: "Enter Value of Bites"
        mode: "round"
        pos_hint: {"center_x":0.5, "center_y": 0.7}
        width: 100
        size_hint_x: 0.5
        font_size: 50

    MDLabel:
        text: "MULTIPLE"
        font_style: 'H2'
        font_size: 30
        halign: 'center'
        size_hint_y: None
        height: self.texture_size[1]
        padding_y: 331
        text_color: 0, 0, 1, 1,

    MDRectangleFlatButton:
        id: MEGA
        text: "MEGA"
        font_size: 25
        theme_text_color: "Custom"
        text_color: "red"
        line_color: "red"
        pos_hint: {"center_x":0.5, "center_y": 0.5}
        on_press: app.MEGA()

    MDRectangleFlatButton:
        id: KILO
        text: "KIlO"
        font_size: 25
        theme_text_color: "Custom"
        text_color: "red"
        line_color: "red"
        pos_hint: {"center_x":0.2, "center_y": 0.5}
        on_press: app.KILO()

    MDRectangleFlatButton:
        id: GIGA
        text: "GIGA"
        font_size: 25
        theme_text_color: "Custom"
        text_color: "red"
        line_color: "red"
        pos_hint: {"center_x":0.8, "center_y": 0.5}
        on_press: app.GIGA()

    MDRectangleFlatButton:
        id: PETA
        text: "PETA"
        font_size: 25
        theme_text_color: "Custom"
        text_color: "red"
        line_color: "red"
        pos_hint: {"center_x":0.5, "center_y": 0.4}
        on_press: app.PETA()

    MDRectangleFlatButton:
        id: TERA
        text: "TERA"
        font_size: 25
        theme_text_color: "Custom"
        text_color: "red"
        line_color: "red"
        pos_hint: {"center_x":0.2, "center_y": 0.4}
        on_press: app.TERA()

    MDRectangleFlatButton:
        id: EXTA
        text: "EXTA"
        font_size: 25
        theme_text_color: "Custom"
        text_color: "red"
        line_color: "red"
        pos_hint: {"center_x":0.8, "center_y": 0.4}
        on_press: app.EXTA()

    MDLabel
        id: Final_Conversion
        text: "TOTAL:"
        font_size: 40
        halign: 'center'
        size_hint_y: None
        height: self.texture_size[1]
        padding_y: 100

```
EVIDENCE
![](https://github.com/ZavenGaloyan/Unit_3_repo/blob/main/Task/HL_CONVERTER.jpg)
