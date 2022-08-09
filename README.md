
## Run Locally

Clone the project

```bash
  git clone https://github.com/sernanic/tutorProject.git
```
### Frontend Instructions

Go to the frontend of the project directory

```bash
  cd tutorProject/frontend
```

Install dependencies 

```bash
  npm install
```

### Backend Instructions

Go to the backend of the project directory

```bash
  cd tutorProject/backend
```

#### Create a Python virtual environment

```bash
  python3 -m venv venv
```

#### Enter in the virtual environment (mac)
```bash
  source venv/bin/activate
```

#### obs: Before the next step, check if your python interpreter is set to ./backend/venv/bin/python3


#### Install dependencies 

Installation might change based on OS

Run the following command in the terminal

```bash
  pip install -r requirements.txt
```

### Database Instructions

* Go to the .env.sample file of the backend, rename it to .env 

* Inside the .env file, adjust the DATABASE_URL according to your mysql username and password

```
  DATABASE_URL=mysql+pymysql://user:pass!@localhost:3306/tutorProject
  //example:
  DATABASE_URL=mysql+pymysql://NicolasSerna:Sernanic123!@localhost:3306/tutorProject
```

* Download Mysql 

* Download Mysql Workbench

* Set Mysql password

* run migrations so you have the models in your database (make sure you are in the backend folder)

```bash
  alembic revision --autogenerate -m 'test'
  
  alembig upgrade head
```

### Start the frontend / backend servers

#### backend

```bash
cd tutorProject/backend/app

uvicorn main:app --reload
```

*one a separate command line window*

#### frontend

```bash
cd tutorProject/frontend

npm run start
```




