
#### using snap package
- not recommended as it is slow
## compiling using rust
[documentation](https://github.com/hrkfdn/ncspot/blob/main/doc/developers.md

- install rust compiler [rust documentation](https://www.rust-lang.org/tools/install)
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

- install dependencies
```sh
sudo apt install libdbus-1-dev libncursesw5-dev libpulse-dev libssl-dev libxcb1-dev libxcb-render0-dev libxcb-shape0-dev libxcb-xfixes0-dev
```

- build/compile
```sh
cargo install ncspot
```