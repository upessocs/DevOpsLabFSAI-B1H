# DevOps Lab 6

## Name: Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

---

## **Git FastAPI - Dockerization**  

### **1. Install Dependencies**  
Install `pipenv` in WSL, then install FastAPI and Uvicorn:  
```sh
pip install pipenv
pipenv install fastapi uvicorn
```

### **2. Write a FastAPI Application**  
Create a `main.py` file with the following code:  
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Name": "Rishitt", "Location": "Delhi"}

@app.get("/{data}")
def read_data(data: str):
    return {"hi": data, "Location": "Delhi"}

if __name__ == "__main__":
    import uvicorn
    uvicorn.run("main:app", host="0.0.0.0", reload=True, port=80)
```

### **3. Run the FastAPI Application**  
```sh
python main.py
```
OR  
```sh
uvicorn main:app
```

---

## **Dockerization**

### **4. Create a `Dockerfile`**  
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

### **5. Create a `requirements.txt` File**  
```txt
uvicorn
fastapi
```

### **6. Build and Run the Docker Container**  
- **Build the Docker image:**  
  ```sh
  docker build -t test02 .
  ```
- **Run the container:**  
  ```sh
  docker run -p 80:80 test02:latest
  ```
Link For Lab 7 - [Lab 7](./Rishitt_Gupta_DevOps_Lab_7.md)