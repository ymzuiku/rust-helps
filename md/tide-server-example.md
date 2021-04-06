# tide-server-example

rust tide web server all by self to build

## my first rust web server code if it is ugly please forgive. I'm just a fresh man for rust

## Dir list

```text
config
  TEST.toml
src
Cargo.toml
```

config/Test.toml

```toml
[database]
mongo_url="mongodb://root:123456@127.0.0.1:27017"
redis_url="redis://127.0.0.1:6379"
mongo_name="test"

[server]
server="127.0.0.1:8090"
domain="http:://127.0.0.1:8090"

[email]
email_name="lomect@example.com"
email_password="123456"
email_server="smtp.server.com"
```

Cargo.toml

```toml
[package]
name = "tide-server-example"
version = "0.1.0"
authors = ["沉默 <1209518758@qq.com>"]
edition = "2018"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
tide = "0.13.0"
async-std = { version = "1.6.3", features = ["attributes"] }
serde = { version = "1.0.115", features = ["derive"] }
base64 = "0.12.3"
rust-argon2 = "0.8.2"
validator = { version = "0.12", features = ["derive"] }
rand = "0.7.3"
lazy_static = "1.4.0"
chrono = { version = "0.4.19", features=["serde"]}
config = "0.10.1"
lettre = { version = "0.10.0-alpha.5", features=["async-std1", "async-std1-rustls-tls"]}
serde_json = "1.0"

[dependencies.mongodb]
version = "*"
features = ["async-std-runtime"]
default-features = false

[dependencies.redis]
version = "0.17.0"
features = ["async-std-comp"]

```
