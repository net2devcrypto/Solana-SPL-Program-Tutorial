# Solana-SPL-Program-Tutorial

Solana SPL Anchor Language Program Tutorial

> [!NOTE]  
> THE FILES ATTACHED TO THIS REPO ARE FOR EDUCATIONAL PURPOSES ONLY.
> NOT FINANCIAL ADVICE
> USE IT AT YOUR OWN RISK, I'M NOT RESPONSIBLE FOR ANY USE, ISSUES.

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