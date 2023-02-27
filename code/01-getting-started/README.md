# hello rust

Passos para montar um ambiente de desenvolvimento com Rust:

## rustup
Instalador e gerenciador de versões do rust
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

O rust é atualizado com bastante frequência, para baixar a versão mais
recente basta executar o comando a seguir:

$ rustup update

? Todos os recursos do rust ficam instalador na pasta: ~/.cargo/bin

## cargo
Ferramenta de compilação e gerenciamento de pacotes

Commands
cargo build             compilar
cargo run               executar
cargo test              testar
cargo doc               gerar documentação
cargo publish           publicar biblioteca em crates.io

## rust-analyzer
Extensão do VSCode para ajudar no desenvolvimento

# rustc
Compilador.

## Estrutura do projeto

cargo new <nome_projeto>
|- Cargo.toml           manifesto, metadados e declarações de depedências
|- Cargo.lock           lista todas as dependências (das dependências também) com suas versões exatas
|- src
  |- main.rs            ponto principal de execução da aplicação

## Dependências
O rust possui várias bibliotecas chamadas de "crates", que podem ser
achadas em crates.io

Para adicionar um dependência basta busca por sua definição no manifesto,
essa informação está na documentação da crate, e fazer o build do projeto,
isso irá fazer as instalações

Ex.:

Cargo.toml
[dependencies]
ferris-says = "0.2"

cargo build