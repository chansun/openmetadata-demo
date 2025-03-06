FROM openmetadata/ingestion:latest

# Let's use the same workdir as the ingestion image
WORKDIR ingestion
USER airflow

# Install our custom connector
COPY connector connector
COPY setup.py .
COPY sample.csv .
COPY person_info.proto .
RUN pip install --no-deps .