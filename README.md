# ntf-test-devnet

bash <(curl -sSf https://sugar.metaplex.com/install.sh)
sugar --version

### Setup wallets

# Setup Solana Tool Suite
sh -c "$(curl -sSfL https://release.solana.com/v1.10.32/install)"
solana --version

## 9v8qCkipmtCyfBZ9gQR79PSC5by6r1Cs9aQfwxc4BGiG
solana-keygen new --outfile Users/danie/Desktop/NTFsolana/my-keypair.json

## E9LSB97Xsn14cvPeAMGCTJ8LLEtToXB2CGyLyDn2vC1Y
Treasury ramdon wallets phantom

## Cwceva6wFKyqh9AYD7TUYLBkPLxmEYk1uXJWcPgk6Gef
solana-keygen new --outfile ./wallets/Creator.json

solana config set --keypair Users/danie/Desktop/NTFsolana/my-keypair.json
solana config set --url https://metaplex.devnet.rpcpool.com/

### Prepare Assets
##generate assets
download repositorio hashlips_art_engine.1.1.2_patch_v6
Change Config dir: hashlips_art_engine.1.1.2_patch_v6/src/config.js
yarn generate 

Copy and paste assets of folder-build 
create folder assets and copy in my-project

### Launch Interactive Setup

Config upload assets in my-project
sugar create-config -c my-config.json

# Candy Machine ID: 3QNr5BfoTZ42YGWVsyDbBPosjjDgYGPmR47T5rWYG6oW
sugar launch


### Setup Candy Machine UI

git clone https://github.com/metaplex-foundation/candy-machine-ui ./candy-machine-ui/

cd ./candy-machine-ui/

yarn install

cp .env.example .env

### insert Candy machine ID

yarn start
