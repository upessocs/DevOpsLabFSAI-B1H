# DevOps Lab 6

## Name: Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

### Git FastAPI - Dockerization  

1. Install pipenv in WSL  
2. Install FastAPI and Uvicorn  
3. Write a FastAPI application with two GET endpoints:  
   - One returning a fixed JSON response with name and location  
   - Another that takes a path parameter and returns it in the response  

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Name": "Rishitt", "Location": "Delhi"}

@app.get("/{data}")
def read_data(data: str):
    return {"hi": data, "Location": "Delhi"}
```

4. Run this command to host the application:
   ```
   uvicorn main:app
   ```

5. Add this code to the Python file:
   ```python
   if __name__ == "__main__":
       uvicorn.run("main:app", host="0.0.0.0", reload=True, port=80)
   ```

6. Run the command:
   ```
   python main.py
   ```

7. Create a Dockerfile:
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

8. Create a `requirements.txt` file:
   ```
   uvicorn
   fastapi
   ```

9. Use the build command to create a Docker image  
   ```
      docker build -t test02 .
   ```

10. Use the run command to execute the Docker image
   ```
      docker run -p 80:80 test02:latest
   ```
