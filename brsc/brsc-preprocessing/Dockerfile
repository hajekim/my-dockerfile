FROM python:3.9-slim-buster

RUN apt -y update && apt install -y --no-install-recommends \
    gcc \
    libgomp1 \
    && apt clean

# Install Requirement Python Libs
RUN /usr/local/bin/python3 -m pip install --upgrade pip && \
    /usr/local/bin/python3 -m pip install \
            numpy pandas scikit-learn \
            awscli boto3 pyathena \
            lightgbm ray

ENV PYTHONUNBUFFERED=TRUE
ENTRYPOINT ["python3"]
