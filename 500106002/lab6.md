# DevOps Lab 6

## Name: Rakshita Garg
**SAP ID:** 500106002

**Roll Number:** R2142220144

**Batch:** Full Stack AI B1 Hons

## Git FastAPI - Dockerization  

**1. Install python3, python-pip and pipenv in WSL**
**2. Install FastAPI and Uvicorn**
**3. Write a FastAPI application with two GET endpoints:**
   - One returning a fixed JSON response with name and location
   - Another that takes a path parameter and returns it in the response

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Name": "Rakshita", "Location": "Faridabad"}

@app.get("/{data}")
def read_data(data: str):
    return {"hi": data, "Location": "Delhi"}
```

**4. Run this command to host the application:**
   ```
   uvicorn main:app
   ```

**5. Add this code to the Python file:**
   ```python
   if __name__ == "__main__":
       uvicorn.run("main:app", host="0.0.0.0", reload=True, port=80)
   ```

**6. Run the command:**
   ```
   python main.py
   ```

**7. Create a Dockerfile:**
   ```dockerfile
   FROM ubuntu

   RUN apt update -y
   RUN apt install python3 python3-pip pipenv -y

   WORKDIR /app
   COPY . /app/
   RUN pipenv install -r requirements.txt

   EXPOSE 80
   CMD pipenv run python3 ./main.py
   ```

**8. Create a `requirements.txt` file:**
   ```
   uvicorn
   fastapi
   ```

**9. Use the build command to create a Docker image**
   ```
      docker build -t test01:v1.0.1 .
   ```

**10. Check the Docker image formed using command**
   ```
      docker images
   ```

**11. Use the run command to execute the Docker image**
   ```
      docker run test01:1.0.1
   ```

**12. Done**