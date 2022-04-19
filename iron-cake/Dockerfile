FROM rustlang/rust:nightly

RUN git clone https://github.com/JoseFilipeFerreira/iron-cake

WORKDIR /iron-cake

RUN cargo build --release

CMD [ "./target/release/iron_cake" ]
