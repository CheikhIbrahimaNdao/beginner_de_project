# Dockerfile for webserver service
FROM python:3.8

# Install required packages
RUN pip install --upgrade pip
RUN pip install apache-airflow[postgres]

# Install isort
RUN pip install isort

# Set the working directory
WORKDIR /opt/airflow

# Specify the entrypoint
ENTRYPOINT ["/entrypoint.sh"]

# Define the command to run the webserver
CMD ["webserver"]

FROM apache/airflow:2.2.0
COPY requirements.txt /
RUN pip install --no-cache-dir -r containers/airflow/requirements.txt
