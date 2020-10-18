[ja](./README.ja.md)

# Espanso.Config

espanso config.

# DEMO

* [demo](https://ytyaru.github.io/Espanso.Config.20201019082519/)

![img](https://github.com/ytyaru/Espanso.Config.20201019082519/blob/master/doc/0.png?raw=true)

# Features

* sales point

# Requirement

* <time datetime="2020-10-19T08:25:10+0900">2020-10-19</time>
* [Raspbierry Pi](https://ja.wikipedia.org/wiki/Raspberry_Pi) 4 Model B Rev 1.2
* [Raspberry Pi OS](https://ja.wikipedia.org/wiki/Raspbian) buster 10.0 2020-08-20 <small>[setup](http://ytyaru.hatenablog.com/entry/2020/10/06/111111)</small>
* [Raspbian](https://ja.wikipedia.org/wiki/Raspbian) buster 10.0 2019-09-26 <small>[setup](http://ytyaru.hatenablog.com/entry/2019/12/25/222222)</small>
* bash 5.0.3(1)-release
* espanso 0.7.2

```sh
$ uname -a
Linux raspberrypi 5.4.51-v7l+ #1333 SMP Mon Aug 10 16:51:40 BST 2020 armv7l GNU/Linux
```

# Installation

## 1. Rust

* [rust install](https://www.rust-lang.org/tools/install)

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
## 2. espanso

* [manual-installation](https://espanso.org/install/linux/#manual-installation)

```sh
sudo apt install -y cmake libxdo-dev
sudo apt install -y libxtst6 libxdo3 xclip libnotify-bin
```
```sh
cargo build
cargo install --path .
```

### 2-1. modulo

* [installing-modulo](https://espanso.org/install/linux/#installing-modulo)

```sh
sudo apt install -y clang libwxgtk3.0-0v5 libwxgtk3.0-dev build-essential
wget https://github.com/federico-terzi/modulo/archive/v0.1.1.zip
unzip v0.1.1
cd modulo-0.1.1
cargo build --release
sudo cp ./target/release/modulo /usr/bin/modulo
```

form.yml
```yaml
layout: |
  Hey {{name}},
  This form is built with modulo!
```
```sh
modulo form -i form.yml
```

# Usage

## 1. espanso

```sh
espanso start
```
```sh
espanso must be registered to systemd (user level) first. Do you want to proceed? [Y/n] 
```
```sh
Y
```

1. Enter `: espanso` on the terminal or text editor.
1. Outputs `Hi there!`

## 2. config

```bash
git clone https://github.com//Espanso.Config.20201019082519
cd Espanso.Config.20201019082519
copy espanso ~/.config
```

# Author

ytyaru

* [![github](http://www.google.com/s2/favicons?domain=github.com)](https://github.com/ytyaru "github")
* [![hatena](http://www.google.com/s2/favicons?domain=www.hatena.ne.jp)](http://ytyaru.hatenablog.com/ytyaru "hatena")
* [![mastodon](http://www.google.com/s2/favicons?domain=mstdn.jp)](https://mstdn.jp/web/accounts/233143 "mastdon")

# License

This software is CC0 licensed.

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.en)

