FROM fl3x3dd/grox:latest

ADD backend_internal/src /app/cache/src

RUN cargo build --bin owner --release

RUN mv target/release/owner /owner

RUN rm -rf /app

ENV ROCKET_ENV=production

WORKDIR /

USER nobody

CMD ["./owner"]