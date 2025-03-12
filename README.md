# FastAPI NotesApp

This guide walks you through setting up and running the FastAPI NotesApp on your local machine.

## 🚀 Getting Started

### Step 1: Create a Project Directory

Create a new directory on your local machine where the project will reside.

### Step 2: Open the Directory in VS Code or PyCharm

Open your newly created directory in VS Code or PyCharm.

### Step 3: Clone the Repository

Open the terminal and run the following command to clone the project:

```sh
git clone <repo_url> .
```

*(Ensure to replace **`<repo_url>`** with the actual repository URL.)*

### Step 4: Create and Activate a Virtual Environment

```sh
python -m venv venv  # Create virtual environment
source venv/bin/activate  # Activate virtual environment (Linux/Mac)
venv\Scripts\activate  # Activate virtual environment (Windows)
```

### Step 5: Install Dependencies

Run the following commands to install the necessary dependencies:

```sh
pip install "fastapi[standard]"
pip install jinja2
pip install -r requirements.txt
```

### Step 6: Configure MongoDB Connection

1. Create a `config` directory inside the project root (if it doesn’t already exist):

   ```sh
   mkdir config
   ```

2. Create a new file inside the `config` directory named `db.py`.

3. Open `db.py` and paste the following content:

   ```python
   from pymongo import MongoClient

   MONGO_URI = "your_mongo_uri"
   conn = MongoClient(MONGO_URI)
   ```

*(Replace **`your_mongo_uri`** with your actual MongoDB connection string.)*

### Step 7: Set Up MongoDB

1. **Login to MongoDB Atlas** via the web application.
2. **Create a new free cluster** and wait for the setup to complete.
   ![MongoDB Cluster](https://github.com/user-attachments/assets/ea9110cf-8ff7-45a9-a28c-ee3902eaa9ee)

3. Dont forget to add current IP address in network access section.
4. **Connect to the cluster**:
   - Click on the **Connect** button as shown in above image.
     ![MongoDB Compass](https://github.com/user-attachments/assets/d7c9669d-bff9-45c9-b8af-96fa5e63967d)
   - Select **MongoDB Compass**.
     ![MongoDB Compass setup](https://github.com/user-attachments/assets/b0070e62-e9ed-4eaa-951f-437a6cb3682c)
   - If you don’t have MongoDB Compass installed, download and install it.
   - Copy the connection string displayed in the second step.
   

5. **Connect via MongoDB Compass**:
   - Open MongoDB Compass.
   - Click **Add Network**.
   - Paste the copied connection string.
     ![MongoDB Connection](https://github.com/user-attachments/assets/b3cebc1c-ee90-4885-9e38-33b6c89c192a)
   - Save and connect.
   
   

6. **Update `db.py` file which you've created in step 6**:
   - Replace `YOUR_MONGO_URI` with the copied connection string from MongoDB Compass.
   

### Step 8: Run the FastAPI Server

Start the FastAPI server using the following command:

```sh
fastapi dev index.py
```

Once the server is running, your app should be accessible and look something like this:

![FastAPI Running](https://github.com/user-attachments/assets/890b269b-50cf-4730-9e9b-7192e29ca6c1)

![FastAPI UI](https://github.com/user-attachments/assets/96448734-9b44-4e14-9386-3d0d2904f762)

---

Now you're ready to start using the FastAPI NotesApp! 🚀

