# Cardano

I have done a lot of work related to Smart-Contracts on the Cardano blockchain and also contributed to its documenation in various places like the smart contracts pages on [developers.cardano.org](https://developers.cardano.org/docs/smart-contracts/) and [docs.cardano.org](https://docs.cardano.org/about-cardano/new-to-cardano/what-is-a-smart-contract/) and also the [Marlowe page on developers.cardano.org](https://developers.cardano.org/docs/smart-contracts/marlowe) .

For some time now I have not worked actively on anything Cardano related, but the community is very friendly and I learnt a lot about blockchain technologies, smart contracts and language parsing while doing so. It's also the first instance of where I had to understand the inner workings of WASM which was a lot of fun.

These are some of my own projects related to Cardano: 

- [marlowe-rs](https://github.com/OlofBlomqvist/marlowe-rs)
    : A DSL parser, serializer, deserializer & CBOR encoder/decoder for Marlowe (V1) smart contracts. Can be used for driving contracts on chain without the normal runtime infrastructure requirements.

- [marlowe-py](https://github.com/OlofBlomqvist/marlowe-py)
    : A python wrapper around marlowe-rs.

- [marlowe-lsp](https://github.com/OlofBlomqvist/marlowe-lsp)
    : A language server and client, both possible to compile to wasm, building on the work done in marlowe-rs.

- [marlowe-indexer](https://github.com/OlofBlomqvist/marlowe-indexer)
    : An indexer for Marlowe contracts on the Cardano blockchain using a GraphQL interface for querying and realtime events.

- [plutus-data](https://github.com/OlofBlomqvist/plutus_data)
    : Macro tooling for converting between plutus-data cbor and rust structs.