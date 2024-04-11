FROM python:3.8
RUN pip install --upgrade pip
RUN pip install apache-airflow[postgres]
RUN pip install isort
WORKDIR /opt/airflow
ENTRYPOINT ["/entrypoint.sh"]
CMD ["webserver"]
FROM apache/airflow:2.2.0
COPY requirements.txt
RUN pip install --no-cache-dir -r containers/airflow/requirements.txt
