FROM golang:1.19

WORKDIR /app

COPY . . 


EXPOSE 8080

RUN go get ./...
RUN go build -o main

ENV DB_HOST=db
ENV DB_USER=admin
ENV DB_PASSWORD=rinnitest
ENV DB_NAME=devops
ENV DB_PORT=5432
ENV ALLOWED_ORIGINS=0.0.0.0/0


CMD ["go", "run", "main.go"]
