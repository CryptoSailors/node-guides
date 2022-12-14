<p align="center">
 <img src="https://miro.medium.com/max/4800/1*witM08dfHB43FdR4yoJdNw.png"width="900"/></a>
</p>

# In this Guide we will install a Manta Trusted Setup

## 1. requirements.
No official paramaters. I recomend to install it on server with following requirements:

2-4 vCPU; 4-8 GBRAM
#### My recommendation: 
- I recommend [Hetzner VPS CX21.](https://hetzner.cloud/?ref=NY9VHC3PPsL0)
- I recommend [MobaXTerm](https://mobaxterm.mobatek.net/download.html) for SSH terminal.
## 2. Preparing for installation.
```
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install make clang pkg-config libssl-dev libclang-dev build-essential git curl ntp jq llvm tmux htop screen unzip cargo cmake -y
```
```
curl https://sh.rustup.rs/ -sSf | sh -s -- -y
```
```
source $HOME/.cargo/env
```
## 3. Installation of Trusted Setup
```
git clone https://github.com/Manta-Network/manta-rs.git
```
```
cd manta-rs
```
```
cargo run --release --package manta-trusted-setup --all-features --bin groth16_phase2_client register
```
## 4. Registration and filling out the form
After installation, the terminal will prompt you to enter your Twitter and e-mail, and immediately generate a key, which must be saved somewhere.

<p align="center">
 <img src="https://miro.medium.com/max/4800/1*6qxCSbZOtoiZNVzCjh7axg.png"width="900"/></a>
</p>

If you have it like in the picture above 👆 then you can start filling out the [form](https://mantanetwork.typeform.com/TrustedSetup?typeform-source=seainvestor.medium.com). The Twitter and email address on the form must be the same as the one you entered in the terminal. That's all for now, wait for further instructions from the Manta Network.

## 5. Contribute
```
cd ~
```
```
mv /root/manta-rs/target/release/groth16_phase2_client /usr/bin/manta-trusted-setup
chmod +x /usr/bin/manta-trusted-setup
```
Creating a screen and making a contribution
```
screen -S manta
```
```
manta-trusted-setup contribute
```
To exit the screen, press CTRL+A,D. To return and see your turn, type:
```
screen -rx manta
```
<p align="center">
 <img src="https://miro.medium.com/max/4800/1*1_kZGZeSF_fwCk6_VhazbA.webp"width="900"/></a>
</p>
#

# 6 Delete Trusted Setup
```
rm -rf /usr/bin/manta-trusted-setup

rm -rf manta-rs
```

👉[Hetzner — server rental](https://hetzner.cloud/?ref=NY9VHC3PPsL0)

👉[SSH terminal MobaxTerm](https://mobaxterm.mobatek.net/download.html)

👉[Discord](https://discord.com/invite/uCyrCmVB2t) 

👉[WebSite](https://www.manta.network/)

👉[Official Guide](https://docs.manta.network/docs/guides/TrustedSetup)

👉[GitHub](https://github.com/Manta-Network/manta-rs/tree/main/manta-trusted-setup)

👉[Form](https://mantanetwork.typeform.com/TrustedSetup?typeform-source=seainvestor.medium.com)

🔰[Our Telegram Channel](https://t.me/CryptoSailorsAnn)

🔰[Our WebSite](cryptosailors.tech)

🔰[Our Twitter](https://twitter.com/Crypto_Sailors)

#### Guide created by 
Pavel-LV | C.Sailors#7698 / @SeaInvestor
