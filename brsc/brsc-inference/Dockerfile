FROM python:3.9-slim-buster

RUN apt -y update && apt install -y --no-install-recommends \
    gcc \
    libgomp1 \
    && apt clean

# Install Basic Python Libs
RUN pip3 install numpy pandas scikit-learn

# Install AWS Libs
RUN pip3 install awscli boto3 pyathena

# Install BRSC Libs
# lightGBM
# Ray
RUN pip3 install lightgbm ray

ENV PYTHONUNBUFFERED=TRUE
ENTRYPOINT ["python3"]