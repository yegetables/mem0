FROM python:3.12-slim

WORKDIR /app

ENV PIP_INDEX_URL=https://mirrors.cloud.tencent.com/pypi/simple/
ENV PIP_TRUSTED_HOST=mirrors.cloud.tencent.com
ENV PIP_NO_CACHE_DIR=1

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8000

ENV PYTHONUNBUFFERED=1

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
