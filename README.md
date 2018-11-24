# aias-masternode

Docker container with aiasd binary to run AIAS Coin masternode

https://www.aiascoin.com/

# Uasage

## Default port 10721

`docker run -d -n aias-mn -p 10721:10721 -e IP=1.2.3.4 -e KEY=mastenode-private-key delfer/aias-masternode`

## Custom port

`docker run -d -n aias-mn -p 10722:10721 -e IP=1.2.3.4 -e KEY=mastenode-private-key -e PORT=10722 delfer/aias-masternode`

## Status
`docker exec -ti aias-mn aias-cli -rpcuser=aias-masternode-docker -rpcpassword=unsecurepassword masternode status`

## Data

All data stored in `/data` folder. You can persist it:

`docker run -d -p 10721:10721 -e IP=1.2.3.4 -e KEY=mastenode-private-key -v aias-mn-data:/data delfer/aias-masternode`

# RPC
You also can set `RPC_PASSWORD` variable and open port `10720` to acces JSON-RPC.

