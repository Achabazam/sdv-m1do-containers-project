FROM rust:latest
WORKDIR /api
COPY ../sdv-api/ .
RUN cargo build --release

EXPOSE 8000

ENV NAME=DEV

CMD ["/api/target/release/sdv-api"]
