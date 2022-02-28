FROM python:3.11-rc-slim-buster

RUN apt -y update && apt install -y --no-install-recommends \
    gcc \
    libgomp1 \
    && apt clean

# Install Basic Python Libs
RUN pip3 install numpy pandas

# Install BRSC Libs
# lightGBM
# Ray
RUN pip3 install lightgbm

ENV PYTHONUNBUFFERED=TRUE
ENTRYPOINT ["python3"]