# Quiz 46
## Python
```.py
import sqlite3

haiku = """Code flow like a stream
Algortihms guide its way
In silence, it solves
"""
connection = sqlite3.connect("Quiz-046.db")
cursor = connection.cursor()

query = f""" CREATE TABLE if not exists Words(
    id INTEGER PRIMARY KEY,
    words text NOT NULL unique
    )
    """
cursor.execute(query)
connection.commit()

for word in haiku.split():
    query1 = f"""INSERT into WORDS(word,length) values ('{word}', 3)"""
    cursor.execute(query)
    connection.commit()
```
 ## Evidence
 ![image](https://user-images.githubusercontent.com/111752809/225646732-62252351-ac4f-486b-ad57-e60ef522b749.png)



