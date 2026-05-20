FROM python:3.12-alpine

WORKDIR /app

COPY app.py .

RUN adduser -D app_user

RUN apk add --no-cache curl

USER app_user

EXPOSE 8080

CMD ["python", "app.py"]
