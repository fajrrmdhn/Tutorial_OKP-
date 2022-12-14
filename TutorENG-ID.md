# TUTORIAL OKP4 INCENTIVE TESTNET

![image](https://user-images.githubusercontent.com/91620434/199645755-250fe003-3e0d-4886-912b-f00b49a043dd.png)

### What is OKP4?
OKP4 is a public PoS layer 1 blockchain built for trust-minimized data sharing.

OKP4 is an open interoperable smart contracts platform for highly customized rules, governance mechanisms and business models to align interests between participants and build useful distributed applications.

Anyone can create custom ecosystems called Data Spaces. In each Data Space, people & companies can share data, algorithms, software, storage and computation according to Data Space's rules.

The OKP4 protocol enables developers to build applications based on distributed digital resources shared by participants (datasets, algorithms, storage, computation...). These shared digital resources together constitute the Dataverse, an ever-expanding universe of resources that can interact with each other through custom ecosystems of shared rules.

With OKP4, builders can find development kits, governance templates and easy-to-integrate applications to design their own applications and Data Spaces. Participants can provide any off-chain digital asset they want to make it findable, available and interoperable with other digital resources of the ecosystem. This on-chain coordination unlocks revolutionary possibilities to generate applications leveraging data and services from many businesses and individuals without any trusted third party accessing these digital resources. It enables new opportunities to generate value from data without exchanging it with other parties, thus bringing trust and incentives to share it and build new, better applications.

OKP4 is designed to become the commons for builders, data providers, communities, businesses, data scientists & users to unlock tangible value creation through a new generation of web3 "real-life" use cases, way beyond Decentralized Finance.

OKP4 is built using the Cosmos SDK and is fundamentally a multichain infrastructure project. Our core value proposition relies on interchain applications leveraging existing networks inside and outside of the Cosmos ecosystem, such as Akash, Juno, Osmosis, Cheqd, Stargaze, Filecoin, Arweave, Ethereum and many more...
> _Translate Indonesia : OKP4 adalah blockchain PoS layer 1 publik yang dibuat untuk berbagi data dengan kepercayaan yang diminimalkan. OKP4 adalah platform kontrak cerdas terbuka yang dapat dioperasikan untuk aturan yang sangat disesuaikan, mekanisme tata kelola, dan model bisnis untuk menyelaraskan kepentingan antara peserta dan membangun aplikasi terdistribusi yang bermanfaat. Siapa pun dapat membuat ekosistem khusus yang disebut Ruang Data. Di setiap Ruang Data, orang & perusahaan dapat berbagi data, algoritme, perangkat lunak, penyimpanan, dan komputasi sesuai dengan aturan Ruang Data. Protokol OKP4 memungkinkan pengembang untuk membangun aplikasi berdasarkan sumber daya digital terdistribusi yang dibagikan oleh peserta (set data, algoritme, penyimpanan, komputasi...). Sumber daya digital bersama ini bersama-sama membentuk Dataverse, alam semesta sumber daya yang terus berkembang yang dapat berinteraksi satu sama lain melalui ekosistem adat aturan bersama. Dengan OKP4, pembangun dapat menemukan kit pengembangan, template tata kelola, dan aplikasi yang mudah diintegrasikan untuk merancang aplikasi dan Ruang Data mereka sendiri. Peserta dapat menyediakan aset digital off-chain apa pun yang mereka inginkan agar dapat ditemukan, tersedia, dan dapat dioperasikan dengan sumber daya digital ekosistem lainnya. Koordinasi on-chain ini membuka kemungkinan revolusioner untuk menghasilkan aplikasi yang memanfaatkan data dan layanan dari banyak bisnis dan individu tanpa pihak ketiga tepercaya yang mengakses sumber daya digital ini. Ini memungkinkan peluang baru untuk menghasilkan nilai dari data tanpa menukarnya dengan pihak lain, sehingga membawa kepercayaan dan insentif untuk membagikannya dan membangun aplikasi baru yang lebih baik. OKP4 dirancang untuk menjadi milik bersama bagi pembangun, penyedia data, komunitas, bisnis, ilmuwan data & pengguna untuk membuka penciptaan nilai nyata melalui generasi baru kasus penggunaan "kehidupan nyata" web3, jauh melampaui Keuangan Terdesentralisasi. OKP4 dibangun menggunakan Cosmos SDK dan pada dasarnya merupakan proyek infrastruktur multirantai. Proposisi nilai inti kami bergantung pada aplikasi antar rantai yang memanfaatkan jaringan yang ada di dalam dan di luar ekosistem Cosmos, seperti Akash, Juno, Osmosis, Cheqd, Stargaze, Filecoin, Arweave, Ethereum, dan banyak lagi..._

> Source : https://docs.okp4.network/whitepaper/introduction

# Main Goals
This repository aspires to supply details about my work as a node operator and validator in several cryptocurrencies project
> _Repositori ini bertujuan untuk memberikan rincian tentang pekerjaan saya sebagai operator node dan validator di beberapa proyek cryptocurrency_

## Hardware Requirement
I currently have an active server with the following specifications :

> My Hardware

|  Component |  My Spec |
| ------------ | ------------ |
| CPU  | 4 Core CPU  |
| RAM | DDR4 8 GB  |
| Storage  | 100 GB NVMe SSD |
| Conection | 32 TB Traffic |

> Minimum Spesification

|  Component |  Spesification |
| ------------ | ------------ |
| CPU  | 4x CPUs  |
| RAM | 8GB RAM  |
| Storage  | 100GB of storage (SSD or NVME) |
| Conection | Permanent Internet connection 10Mbps - 100Mbps | 

# TUTORIAL

In this tutorial I will refer to the tutorial in the pinned message in the OKP4 region discord group Indonesia
> _Pada tutorial kali ini saya akan merujuk tutorial pada pesan yang disematkan di grup discord wilayah OKP4 Indonesia_
> Source : https://github.com/nodesxploit/testnet/blob/main/okp4/README.md

## 1. Automatic Installation

![image](https://user-images.githubusercontent.com/91620434/199699133-c0f0c85b-e35e-456c-9586-7ac415a9b352.png)

```
wget -O okp4.sh https://raw.githubusercontent.com/nodesxploit/testnet/main/okp4/okp4.sh && chmod +x okp4.sh && ./okp4.sh
```

The picture below is a synchronization process, at this stage please be patient waiting
> _Gambar dibawah ini merupakan proses sinkronisasi, pada tahapan ini mohon untuk bersabar menunngu_
![image](https://user-images.githubusercontent.com/91620434/199699313-5b718770-28ab-4ccf-a037-ab1c07a87050.png)
![image](https://user-images.githubusercontent.com/91620434/199699333-2c3fb86b-889d-46ce-896b-e6c49b83207c.png)

You can synchronize in minutes with the help of the below command
> _Anda dapat meyinkronisasi dalam hitungan menit dengan bantuan perintah dibawah ini_

```
SNAP_RPC=https://okp4-testnet-rpc.polkachu.com:443
peers="https://okp4-testnet-rpc.polkachu.com:443"
sed -i.bak -e  "s/^persistent_peers *=.*/persistent_peers = \"$peers\"/" ~/.okp4d/config/config.toml
LATEST_HEIGHT=$(curl -s $SNAP_RPC/block | jq -r .result.block.header.height); \
BLOCK_HEIGHT=$((LATEST_HEIGHT - 500)); \
TRUST_HASH=$(curl -s "$SNAP_RPC/block?height=$BLOCK_HEIGHT" | jq -r .result.block_id.hash)

echo $LATEST_HEIGHT $BLOCK_HEIGHT $TRUST_HASH

sed -i.bak -E "s|^(enable[[:space:]]+=[[:space:]]+).*$|\1true| ; \
s|^(rpc_servers[[:space:]]+=[[:space:]]+).*$|\1\"$SNAP_RPC,$SNAP_RPC\"| ; \
s|^(trust_height[[:space:]]+=[[:space:]]+).*$|\1$BLOCK_HEIGHT| ; \
s|^(trust_hash[[:space:]]+=[[:space:]]+).*$|\1\"$TRUST_HASH\"| ; \
s|^(seeds[[:space:]]+=[[:space:]]+).*$|\1\"\"|" $HOME/.okp4d/config/config.toml

okp4d tendermint unsafe-reset-all --home /root/.okp4d --keep-addr-book
systemctl restart okp4d && journalctl -u okp4d -f -o cat
```
![image](https://user-images.githubusercontent.com/91620434/199699352-f967311a-0540-4ffd-9495-92185e3dc997.png)
![image](https://user-images.githubusercontent.com/91620434/199699368-4ec7f8ce-9738-484f-96e8-d5678f3eb38e.png)

The above step, syncing in minutes is an optional step
> _Langkah diatas yaitu menyinkronisasikan dalam hitugan menit adalah langkah opsional_

If you want to exit the synchronization process then you can use the `CTRL+A+D` command and if you want to return then you can use the `screen r` command or check the status of the node
> _Jika ingin keluar dari proses sinkronisasi maka anda bisa menggunakan command `CTRL+A+D` dan jika ingin kembali maka bisa dengan perintah `screen r` atau cek status node_

## 2. After Installation

After istallation finished please load this code
_Setelah instalasi selesai masukan code berikut_

```
source $HOME/.bash_profile
```

The next step you have to check your validator whether it has synchronized the existing blocks in explorer by using the command below
>> _Langkah selanjutnya anda harus periksa validator anda apakah sudah menyinkronkan block yang ada dalam explorer dengan menggunakan perintah dibawah

```
okp4d status 2>&1 | jq .SyncInfo
```

If it is synchronized it will appear as shown below
_Jika sudah tersinkroisasi maka akan mucul seperti gambar dibawah
![image](https://user-images.githubusercontent.com/91620434/199698895-b24c6d09-886d-4f4a-8854-663d677a06f6.png)_

## 3. Crate Wallet

The following command is a way to create a wallet, keep in mind to save all data that appears such as seeds and keys
> _Perintah berikut merupakan cara untuk membuat wallet, perlu diingat untuk menyimpan semua data yang muncul seperti seed dan key_

![image](https://user-images.githubusercontent.com/91620434/199700637-9a53b777-135e-47af-9b26-c97917e75995.png)

```
okp4d keys add $WALLET
```
> Recover wallet
```
okp4d keys add $WALLET --recover
```
> List wallet
```
okp4d keys list
```
> Save wallet information
```
OKP4D_WALLET_ADDRESS=$(okp4d keys show $WALLET -a)
OKP4D_VALOPER_ADDRESS=$(okp4d keys show $WALLET --bech val -a)
echo 'export OKP4D_WALLET_ADDRESS='${OKP4D_WALLET_ADDRESS} >> $HOME/.bash_profile
echo 'export OKP4D_VALOPER_ADDRESS='${OKP4D_VALOPER_ADDRESS} >> $HOME/.bash_profile
source $HOME/.bash_profile
```
To get a faucet you can easily access the following link
> _Untuk mendapatkan faucet anda bisa dengan mudah mengakses lik berikut_ 

https://faucet.okp4.network/

## 4. Crate Validator

Check your wallet using this command
> _Cek wallet anda terlebih dahulu
```
okp4d query bank balances $OKP4D_WALLET_ADDRESS
```
Note : if theres no ballance i your wallet so please wait for sync proces

Command below is to ru your validator
> _Perintah dibawah untuk menjalankan validator anda_
```
okp4d tx staking create-validator \
  --amount 100000000uknow \
  --from $WALLET \
  --commission-max-change-rate "0.01" \
  --commission-max-rate "0.2" \
  --commission-rate "0.07" \
  --min-self-delegation "1" \
  --pubkey  $(okp4d tendermint show-validator) \
  --moniker $NODENAME \
  --chain-id okp4-nemeton
```

## My Experience

Checkout my experience being a validator by access this link :
https://github.com/fajrrmdhn/Tutorial_OKP-/blob/main/My%20Experience.md

