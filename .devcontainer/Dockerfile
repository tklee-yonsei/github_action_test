FROM python:3.10-slim

# 시스템 패키지 설치
RUN apt-get update && \
    apt-get install -y git gcc && \
    rm -rf /var/lib/apt/lists/*

# Python 패키지 설치
COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

# pre-commit 설치
RUN pip install pre-commit black flake8 pylint
