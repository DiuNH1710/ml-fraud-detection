FROM apache/airflow:3.0.4

#create model directory and set ownership
USER root
RUN mkdir -p /app/models

USER airflow
#copy  requirements file
COPY requirements.txt /tmp/requirements.txt

#Install Python packages as root (system-wide)
RUN pip install -r /tmp/requirements.txt

#Switch back to airflow user for safety
USER airflow