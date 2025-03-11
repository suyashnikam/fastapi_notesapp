# fastapi_notesapp


After cloning you can look into gitignore file

create and activate venv 

then install requirements using pip install -r requirements.txt

see config directory is ignored as it containes database configuration:

copy below content and paste it insdie your config/db.py

--------------

from pymongo import MongoClient

MONGO_URI = "your_mongo_uri"

conn = MongoClient(MONGO_URI)

--------------

To run the project as dev server :

fastapi dev index.py
