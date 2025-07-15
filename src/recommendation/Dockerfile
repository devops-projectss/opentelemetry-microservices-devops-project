FROM python:3.12.11-alpine3.21
WORKDIR /usr/src/app/
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . ./
ENV RECOMMENDATION_PORT 1010
ENTRYPOINT [ "python" , "recommendation_server.py"]