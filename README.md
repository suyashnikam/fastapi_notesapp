# fastapi_notesapp


**Step 1: Make a directory locally** 

**Step 2: Open VS code or pycharm for created directory** 

**Step 3: Once open in VS code, Navigate to termial and hit git clone command to clone the project using repo_url along with "." at the end**

git clone repo_url .

**Step 4: Create and activate venv**

python -m venv venv  

source venv/bin/activate

**Step 5: Run the requirement.txt and other commands as below**

pip install "fastapi[standard]"

pip install jinja2

pip install -r requirements.txt

**Step 6: Setting up config direcotry which is gitignore you can also cross check gitignore files**

mkdir config (Make sure you are on project root path)

create a new file inside config as db.py (via pycharm or using cli)

copy below content and paste it inside db.py

--------------

from pymongo import MongoClient

MONGO_URI = "your_mongo_uri"

conn = MongoClient(MONGO_URI)

--------------


**Step 7:Setup MONGO_URI**

You need to login to mongo atlas via webapp

create a new free cluster

Once cluster created you will be able to see it as :
<img width="992" alt="Screenshot 2025-03-12 at 11 49 25 PM" src="https://github.com/user-attachments/assets/ea9110cf-8ff7-45a9-a28c-ee3902eaa9ee" />

After clicking on connect button, you will get: 
<img width="796" alt="Screenshot 2025-03-12 at 11 52 43 PM" src="https://github.com/user-attachments/assets/d7c9669d-bff9-45c9-b8af-96fa5e63967d" />

Select compass option from listed options, once selected you will get window as:
<img width="793" alt="Screenshot 2025-03-12 at 11 55 05 PM" src="https://github.com/user-attachments/assets/b0070e62-e9ed-4eaa-951f-437a6cb3682c" />

Now you should have mongoDB compass installed on your local, if its not then also you can setup as above image explained, just installed it and **Copy that Connection string it is giving**

   
