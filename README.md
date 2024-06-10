# Solana-SPL-Program-Tutorial

A highly requested tutorial! We are covering from start to finish how to write Solana SPL Token Program to launch your own token on the Solana blockchain. 


<img src="https://raw.githubusercontent.com/net2devcrypto/misc/main/anchorlogo.png" width="200" height="70"> <img src="https://raw.githubusercontent.com/net2devcrypto/misc/main/sol-logo.png" width="260" height="70">

> [!NOTE]  
> THE FILES ATTACHED TO THIS REPO ARE FOR EDUCATIONAL PURPOSES ONLY.
> NOT FINANCIAL ADVICE
> USE IT AT YOUR OWN RISK, I'M NOT RESPONSIBLE FOR ANY USE, ISSUES.

<h3>Video 1</h3>

<a href="https://youtu.be/g2YK_YBWA9A" target="_blank"><img src="https://github.com/net2devcrypto/misc/blob/main/ytlogo2.png" width="150" height="40"></a>

<h3>Video 2</h3>

<a href="https://youtu.be/tzaZJXS7AWM" target="_blank"><img src="https://github.com/net2devcrypto/misc/blob/main/ytlogo2.png" width="150" height="40"></a>

<h3>Video 2 Instructions</h3>

<h4>The steps below are compatible with Ubuntu 22.04</h4>

> [!NOTE]  
> If you have Windows, please download VMware Workstation Player, install then create a virtual machine. Follow the tutorial video for full guidance.
> 
> VMware Workstation Player for Windows: https://www.techspot.com/downloads/downloadnowfile/1969/?evp=4c50cf08866937ea246522b86f4d4286&file=2171
>
> Ubuntu Desktop 22.04 ISO: https://releases.ubuntu.com/jammy/ubuntu-22.04.4-desktop-amd64.iso
> 

<h4>Step 1 Dependencies</h4>

```shell
sudo apt-get update && sudo apt-get upgrade && sudo apt-get install -y curl pkg-config build-essential libudev-dev libssl-dev
```

<h4>Step 2 Install Rust</h4>

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Press Enter When Prompted.

<h4>Step 3 Install Solana CLI</h4>

```shell
sh -c "$(curl -sSfL https://release.solana.com/v1.18.14/install)"
```

<h4>Step 4 Update PATH (UBUNTU ONLY)</h4>

```shell
nano ~/.bashrc
```

Add this line to end of file:

```shell
export PATH="/root/.local/share/solana/install/active_release/bin:$PATH"
```

save by :  CTRL + X , Press Y, ENTER

Reboot PC.

Open back the terminal then confirm that Solana Cli is active by typing "solana" and press ENTER.

<h4>Step 5 Install NodeJS</h4>

```shell
curl -fsSL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh
```

```shell
sudo -E bash nodesource_setup.sh
```

```shell
sudo apt-get install -y nodejs
```

Verify Installation:

```shell
node -v
```

<h4>Step 6 Install Yarn</h4>

```shell
corepack enable
yarn init -2
```

Ignore Error: Internal Error: Process git failed to spawn

<h4>Step 7 Install Anchor</h4>

```shell
cargo install --git https://github.com/coral-xyz/anchor avm --locked --force
```

```shell
avm install latest
avm use latest
```

Verify Installation:

```shell
anchor --version
```

<h4>Step 8 Generate Dev Solana Wallet </h4>

```shell
solana-keygen new
```
