FROM docker.io/library/golang:latest

WORKDIR /app

COPY go.mod .

COPY go.sum .

RUN go mod download 

# Copy the source from the current directory to the working Directory inside the container

COPY . .

COPY .env /app

EXPOSE 8000

ENTRYPOINT CompileDaemon --build="go build main.go" --command=./main



