 # Quiz 47
 ## Python Code
 ```.py
 import sqlite3
from passlib.context import CryptContext

pwd_config = CryptContext(schemes = ["pbkdf2_sha256"],
                          default = "pbkdf2_sha256",
                          pbkdf2_sha256__default_rounds = 30000
                          )


# this function receives unsafe password and returns the hashed password
def encrypt_password(user_passowrd):
    return pwd_config.encrypt(user_passowrd)


def check_password(hashed_password, user_password):
    return pwd_config.verify(user_password, hashed_password)


from kivymd.app import MDApp
from secure_password import encrypt_password


class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect("payments.db")
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()


class quiz047(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.components = {"basic": 0}

    def build(self):
        return

    def save(self):
        pass

    def update(self):
        base = self.root.ids.base.text
        hash = ""
        ids = ["inhabitant", "income_tax", "pension", "health"]
        if base != "":
            total = int(base)
            hash += f"base{total}"
            for id in ids:
                value = self.root.ids[id].text
                if value != "":
                    new_value = f"{int(value) * int(base) // 100} JPY"
                    total -= int(value) * int(base) // 100
                    hash += f"{id}{value}"
                else:
                    new_value = "JPY"
                    hash += f"text"
                self.root.ids[id + "_label"].text = new_value
            hash += f"total{total}"
            self.root.ids.salary_label.text = f"{total} JPY"
            encrypted_hash = encrypt_password(hash)
            self.root.ids.hash.text = encrypted_hash[(len(encrypted_hash) - 50):len(encrypted_hash)]

    def save(self):
        base = self.root.ids.base.text
        hash = ""
        ids = ["inhabitant", "income_tax", "pension", "health"]

        if base != "":
            total = int(base)
            hash += f"base{total}"
            for column in ids:
                value = self.root.ids[column].text
                if value != "":
                    new_value = f"{int(value) * int(base) // 100} JPY"
                    total -= int(value) * int(base) / 100
                    hash += f"id_of_textField{value}"
                else:
                    new_value = " JPY"
                    hash += f"id_of_textField{0}"
                self.root.ids[f"{column}_label"].text = new_value
            hash += f"total{total}"
            self.root.ids.salary_label.text = f"{total} JPY"
            encrypted_hash = encrypt_password(hash)
            self.root.ids.hash.text = encrypted_hash[:50]

        inhabitant = int(self.root.ids.inhabitant_label.text.split(" JPY")[0])
        income_tax = int(self.root.ids.income_tax_label.text.split(" JPY")[0])
        pension = int(self.root.ids.pension_label.text.split(" JPY")[0])
        health = int(self.root.ids.health_label.text.split(" JPY")[0])
        total = int(self.root.ids.salary_label.text.split(" JPY")[0].split('.')[0])
        hash = self.root.ids.hash.text

        query = f"INSERT into payments(base, inhabitant, income_tax, pension, health, total, hash) values('{int(base)}', '{inhabitant}', '{income_tax}', '{pension}', '{health}', '{total}', '{hash}')"
        db = database_worker("payments.db")
        db.run_save(query)
        db.close()
        self.root.ids.hash.text = f"Payment saved"

    def clear(self):
        for label in ["base", "inhabitant", "income_tax", "pension", "health"]:
            self.root.ids[label].text = ""
            self.root.ids[label + "_label"].text = " JPY"

        self.root.ids["salary_label"].text = " JPY"
        self.root.ids.hash.text = "----"


    def fraud(self):
        data = database_worker("payments.db")
        query = "SELECT * from payments"
        result = data.search(query)
        data.close()
        print(len(result))
        for column in result:
            base = column[1]
            inhabitant = column[2]
            income_tax = column[3]
            pension = column[4]
            health = column[5]
            total = column[6]
            hash = column[7]
            hash = hash[-50:]
            hash_to_check = f"base{base},inhabitant{int(inhabitant)//int(base) * 100},income_tax{int(income_tax)//int(base) * 100},pension{int(pension)//int(base)*100},health{int(health)//int(base)*100},total{int(total)//int(base)*100}"
            encrypted_hash = encrypt_password(hash_to_check)
            if encrypted_hash[-50:] == hash:
                print(f"Payment {column[0]} NOT FRAUD")
            else:
                print(f"Payment {column[0]} FRAUD")
m = quiz047()
create = """CREATE TABLE if not exists payments(
            id INTEGER PRIMARY KEY,
            base int,
            inhabitant int,
            income_tax int,
            pension int,
            health int
            total int,
            hash text
    )"""
m.fraud()
m.run()
 ```
 
 ## Kivy Code
 ```.kv
 MDScreen:
    id:bck
    size: 200, 500

    MDBoxLayout:
        id: bck
        size_hint: .8,.9
        md_bg_color: "#F2F2F2"
        orientation: "vertical"
        pos_hint: {"center_x":.5, "center_y":.5}
        spacing: dp(10)

        MDLabel:
            text:"Compensation Calculator"
            halign: "center"
            font_style:"H4"
            color: "#222222"

        MDBoxLayout:
            size_hint_x: .8
            height: dp(46)
            valign: "center"
            md_bg_color: "#FFFFFF"
            pos_hint: {"center_x":.5, "center_y":.5}
            spacing: dp(10)

            MDIcon:
                icon: "plus-circle"
                pos_hint: {"center_x": .5, "center_y": .5}
            MDLabel:
                text:"Base Salary"
                size_hint_x: .4
            MDTextField:
                id:base
                mode: "rectangle"
                input_filter:"int"
                text_color_normal: "#222222"
                line_color_normal: "#222222"
                hint_text: "Base Salary"
                pos_hint: {"center_x": .5, "center_y": .5}
                on_text:
                    root.ids.base_label.text = f"{self.text} JPY"
                    app.update()
            MDLabel:
                id: base_label
                text:" JPY"

        MDBoxLayout:
            size_hint_x: .8
            height: dp(46)
            valign: "center"
            md_bg_color: "#FFFFFF"
            pos_hint: {"center_x":.5, "center_y":.5}
            spacing: dp(10)


            MDIcon:
                icon: "minus-circle"
                pos_hint: {"center_x": .5, "center_y": .5}
                color: "#9d0208"
            MDLabel:
                text:"Health"
                size_hint_x: .4
                color: "#6a040f"
            MDTextField:
                id:health
                mode: "rectangle"
                input_filter:"int"
                hint_text: "% Health"
                pos_hint: {"center_x": .5, "center_y": .5}
                text_color_normal: "#9d0208"
                line_color_normal: "#9d0208"
                on_text:
                    self.text = str(max(0, min(100, int(self.text or 0))))
                    app.update()
            MDLabel:
                id: health_label
                text:" JPY"
                color: "#9d0208"

        MDBoxLayout:
            size_hint_x: .8
            height: dp(46)
            valign: "center"
            md_bg_color: "#FFFFFF"
            pos_hint: {"center_x":.5, "center_y":.5}
            spacing: dp(10)


            MDIcon:
                icon: "minus-circle"
                pos_hint: {"center_x": .5, "center_y": .5}
                color: "#9d0208"
            MDLabel:
                text: "Pension"
                size_hint_x: .4
                color: "#9d0208"
            MDTextField:
                id:pension
                mode: "rectangle"
                input_filter:"int"
                hint_text: "% Pension"
                text_color_normal: "#9d0208"
                line_color_normal: "#9d0208"
                pos_hint: {"center_x": .5, "center_y": .5}
                on_text:
                    self.text = str(max(0, min(100, int(self.text or 0))))
                    app.update()
            MDLabel:
                id: pension_label
                text:" JPY"
                color: "#9d0208"


        MDBoxLayout:
            size_hint_x: .8
            height: dp(46)
            valign: "center"
            md_bg_color: "#FFFFFF"
            pos_hint: {"center_x":.5, "center_y":.5}
            spacing: dp(10)

            MDIcon:
                icon: "minus-circle"
                pos_hint: {"center_x": .5, "center_y": .5}
                color: "#9d0208"
            MDLabel:
                text:"Income Tax"
                size_hint_x: .4
                color: "#9d0208"
            MDTextField:
                id:income_tax
                mode: "rectangle"
                input_filter:"int"
                hint_text: "% Income"
                text_color_normal: "#9d0208"
                line_color_normal: "#9d0208"
                pos_hint: {"center_x": .5, "center_y": .5}
                on_text:
                    self.text = str(max(0, min(100, int(self.text or 0))))
                    app.update()
            MDLabel:
                id: income_tax_label
                text:" JPY"
                color: "#9d0208"

        MDBoxLayout:
            size_hint_x: .8
            height: dp(46)
            valign: "center"
            md_bg_color: "#FFFFFF"
            pos_hint: {"center_x":.5, "center_y":.5}
            spacing: dp(10)


            MDIcon:
                icon: "minus-circle"
                pos_hint: {"center_x": .5, "center_y": .5}
                color: "#9d0208"
            MDLabel:
                text:"Inhabitant Tax"
                size_hint_x: .4
                color: "#9d0208"
            MDTextField:
                id:inhabitant
                mode: "rectangle"
                input_filter:"int"
                hint_text: "%  Income"
                text_color_normal: "#9d0208"
                line_color_normal: "#9d0208"
                pos_hint: {"center_x": .5, "center_y": .5}
                on_text:
                    self.text = str(max(0, min(100, int(self.text or 0))))
                    app.update()
            MDLabel:
                id: inhabitant_label
                text:" JPY"
                color: "#9d0208"


        MDBoxLayout:
            size_hint_x: .8
            height: dp(46)
            valign: "center"
            md_bg_color: "#22223b"
            pos_hint: {"center_x":.5, "center_y":.5}
            spacing: dp(10)

            MDLabel:
                size_hint_x: .5
            MDIcon:
                icon: "calculator"
                pos_hint: {"center_x": .5, "center_y": .5}
                color: "#F2F2F2"
            MDLabel:
                text:"Net Salary"
                size_hint_x: .4
                color: "#F2F2F2"
            MDLabel:
                id: salary_label
                text:" JPY"
                color: "#F2F2F2"
            MDFloatingActionButton:
                icon:"content-save-plus"
                md_bg_color:"#ffc300"
                icon_color:"#222222"
                pos_hint: {"center_x": .5, "center_y": .5}
                on_press:
                    app.save()

            MDFloatingActionButton:
                icon:"autorenew"
                md_bg_color:"#2a9d8f"
                icon_color:"#222222"
                pos_hint: {"center_x": .5, "center_y": .5}
                on_press:
                    app.clear()

        MDBoxLayout:
            size_hint: .8, .2
            valign: "center"
            md_bg_color: "#FFFFFF"
            pos_hint: {"center_x":.5, "center_y":.5}

            MDLabel:
                id: hash
                halign: "center"
                text: "----"
                font_style: "Caption"
 ```
 ## Evidence
 ![image](https://user-images.githubusercontent.com/111752809/225647117-37575675-4dd8-4429-8fcc-47b54db28c02.png)

