FROM python:3.9-slim-buster

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# Include config.yaml and image files
COPY config.yaml config.yaml
COPY MASTER-STILL-Gen3_FrontAerial_Combo.jpg MASTER-STILL-Gen3_FrontAerial_Combo.jpg

EXPOSE 8080

CMD ["streamlit", "run", "streamlit-app.py"]
