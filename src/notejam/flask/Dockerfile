FROM python:2.7.18-alpine

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN apk add --no-cache postgresql-libs && \
 apk add --no-cache --virtual .build-deps gcc musl-dev postgresql-dev && \
pip install --no-cache-dir -r requirements.txt
COPY . .
CMD [ "python", "./runserver.py" ]
