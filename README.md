 
## 安装node等软件

sudo apt update
sudo apt install libssl-dev pkg-config
sudo apt-get install pkg-config libssl-dev build-essential
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"   
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  
nvm install 20
npm i -g yarn


### 1. 构建程序
 
```bash
git clone https://github.com/njskyun/cat-token-box.git
cd cat-token-box
git checkout catapp
yarn install && yarn build
```

## 2. Run the `tracker` service

Follow the instructions [here](./packages/tracker/README.md) to setup and start the `tracker` service.

## 3. Execute `CLI` commands

After the `tracker` syncs up to the latest block, you can execute all kinds of commands provided by the `cli` package to interact with `CAT` protocol tokens. Refer to [this document](./packages/cli/README.md) to see more details.
 
