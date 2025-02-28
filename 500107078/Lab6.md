DevOps Lab 6: Git FastAPI - Dockerization
This guide covers setting up a FastAPI application, Dockerizing it, and running it inside a container.

Step 1: Install Pipenv in WSL
Ensure you have pipenv installed in your WSL (Windows Subsystem for Linux):

sh
Copy
Edit
pip install --user pipenv
Step 2: Install FastAPI and Uvicorn
Navigate to your project directory and install the required dependencies:

sh
Copy
Edit
pipenv install fastapi uvicorn
Step 3: Create a FastAPI Application
Create a main.py file and add the following FastAPI code:

python
Copy
Edit
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
return {"Name": "Piyush", "Location": "Hisar"}

@app.get("/{data}")
def read_data(data: str):
return {"hi": data, "Location": "Hisar"}

if __name__ == "__main__":
import uvicorn
uvicorn.run("main:app", host="0.0.0.0", reload=True, port=80)
Step 4: Run the FastAPI Application
Start the server using Uvicorn:

sh
Copy
Edit
uvicorn main:app
or

sh
Copy
Edit
python main.py
The API should now be accessible at http://localhost:80.

Step 5: Create a Dockerfile
Create a Dockerfile in your project directory with the following content:

dockerfile
Copy
Edit
FROM ubuntu

RUN apt update -y
RUN apt install python3 python3-pip pipenv -y

WORKDIR /app
COPY . /app/
RUN pipenv install -r requirements.txt

EXPOSE 80
CMD pipenv run python3 ./main.py
Step 6: Create a requirements.txt File
Create a requirements.txt file and add the dependencies:

nginx
Copy
Edit
uvicorn
fastapi
Step 7: Build the Docker Image
Run the following command to build a Docker image named test02:

sh
Copy
Edit
docker build -t test02 .
Step 8: Run the Docker Container
Run the container and map port 80 to the host:

sh
Copy
Edit
docker run -p 80:80 test02:latest