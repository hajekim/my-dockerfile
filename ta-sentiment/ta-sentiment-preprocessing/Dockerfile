FROM python:3.11-slim-buster

RUN apt -y update && apt install -y --no-install-recommends \
    libgomp1 \
    && apt clean

# Install Basic Python Libs
RUN pip3 install numpy pandas scikit-learn

# Install AWS Libs
RUN pip3 install awscli boto3 pyathena awswrangler

# Install TA-Sentiment Libs

ENV PYTHONUNBUFFERED=TRUE
ENTRYPOINT ["python3"]