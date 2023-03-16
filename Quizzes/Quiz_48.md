 # Quiz 48
 ## Python Code
 ```.py
import sqlite3
from Seqcure_password import check_password

class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect(name)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()

db = database_worker("bitcoin_exchange.db")
query = "SELECT * from ledger"
result = db.search(query)



for row in result:
    id = row[0]
    sender_id = row[1]
    receiver_id = row[2]
    amount = row[3]
    hash = row[4]
    string_hash = f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}"
    equal = check_password(hashed_password=hash, user_password=string_hash)
    end_code = "\033[00m"
    green = "\033[0;32m"
    red = "\33[0;31m"
    if equal == True:
        print(f"{green}Tx(id=1)Signature matches{end_code}")
    else:
        print(f"{red}Tx(id=1)Error signature{end_code}")
db.close()
```
## Evidence
```
Due to the hashing algorithm changeing it doenst work with the given database. However this is what the result would look like
Tx(id=1)Signature matches
Tx(id=1)Signature matches
Tx(id=1)Error signature
Tx(id=1)Error signature
Tx(id=1)Signature matches
```

```.py
Traceback (most recent call last):
  File "C:\Users\glute\PycharmProjects\pythonProject\Unit-3\Quiz-048.py", line 33, in <module>
    equal = check_password(hashed_password=hash, user_password=string_hash)
  File "C:\Users\glute\PycharmProjects\pythonProject\Unit-3\Seqcure_password.py", line 9, in check_password
$5$rounds=30000$lbefAGUoZ1pv55jl$oz7mU.bJYGLRBXsLIvIJyThDuZoSdXXDPZN7I1VrPq9
    return hasher.verify(user_password, hashed_password)
  File "C:\Users\glute\PycharmProjects\pythonProject\venv2\lib\site-packages\passlib\utils\handlers.py", line 788, in verify
    self = cls.from_string(hash, **context)
  File "C:\Users\glute\PycharmProjects\pythonProject\venv2\lib\site-packages\passlib\handlers\sha2_crypt.py", line 307, in from_string
    raise uh.exc.InvalidHashError(cls)
ValueError: not a valid sha256_crypt hash
```
