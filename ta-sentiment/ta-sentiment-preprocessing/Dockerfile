FROM python:3.7-slim-buster

RUN apt-get update -y && apt-get install -y --no-install-recommends \
    gcc libgomp1 \
    expat glibc-source glibc-doc \
    && apt-get full-upgrade -y \
    && apt-get clean
    # libexpat1-dev libc6-dev \

# Install Requirement Python Libs
RUN /usr/local/bin/python3 -m pip install --upgrade pip && \
    /usr/local/bin/python3 -m pip install \
            numpy pandas scikit-learn \
            awscli boto3 pyathena awswrangler

ENV PYTHONUNBUFFERED=TRUE

ENTRYPOINT ["python3"]