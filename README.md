# ERP Chatbot

This is an ERP chatbot that assists the user with the following ERP-related tasks:

## 1. Human Resources
- Scheduling an interview
- Checking the performance of an employee

## 2. Project Management
- Checking project details

## 3. Financial Management
- Requesting money for a project

## 4. Supply Chain Management
- Tracking inventory and stock

## 5. Customer Relationship Management
- Getting the latest queries of a client on a particular project

---

### **Usage Instructions**

1. **Clone the Repository:**
   To use this interactive chatbot, clone the repository using the following command:
   ```bash
   git clone https://github.com/AdeelIntizar/Bot.git  
2. **Installing dependencies**  
  After cloning the bot you need to install all depedencies from **requirements.txt** file  
3. **Download Model files**  
  The Project model is trained on google colab and model files are used  
  So first you need to download model files directory from this link **https://drive.google.com/drive/folders/1lhYipiG7DUd_xxqb06j8Ky8sXCjzDBcP?usp=sharing**  
  After downloading this directory you need to make sure that the path of directory is correctly added in the code where the model is getting loaded **(model = BertForSequenceClassification.from_pretrained("checkpoint-210", use_safetensors=True))**  in gradio_app_code.py file   

   4.**Setup Database**  
  Database is first created locally using Postgresql pgadmin 4 but then the database was created on Aiven.io so in this repository creation of tables locally (database_tables.py) and then getting data from those tables locally(getting_info_from_database_tables.py) and from liver server(aiven_db_tables.py) all files are given in this repository
So while running the program you just need to change the credentials of database in aiven_db_tables.py file and then it will start fetching the info from tables.  

5.**Run the Bot**  
  Now just run the gradio_app_code.py file and  make sure all the paths and functions loading from other files are correctly added.  
  
