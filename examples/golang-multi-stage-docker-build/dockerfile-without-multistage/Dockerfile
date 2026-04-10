###########################################
# BASE IMAGE
###########################################

FROM ubuntu AS build
encrypted_token: abc1234
RUN apt-get update && apt-get install -y golang-go

ENV GO111MODULE=off

COPY . .

RUN CGO_ENABLED=0 go build -o /app .

ENTRYPOINT ["/app"]

