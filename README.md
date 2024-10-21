# simpyle-xmr-arcade
Simple Jackpot with built in 3-5% house edge

GnuPG and monero wallet rpc Required:

Linux: https://gnupg.org/download/index.html

Windows: https://gnupg.org/ftp/gcrypt/binary/

Please notify me if there are any glaring/conceptual security holes

install monero folder
create wallet only intended for processor

Linux: ./monero-wallet-rpc --rpc-bind-port (wallet_rpc_port) --daemon-address (daemon_ip_with_port) --wallet-file (wallet_name) --prompt-for-password --disable-rpc-login

Windows: monero-wallet-rpc.exe --rpc-bind-port (wallet_rpc_port) --daemon-address (daemon_ip_with_port) --wallet-file (wallet_name) --prompt-for-password --disable-rpc-login

Live Reload:

Useful in development. Recommended to turn off during production for less resource usage.


RPC is hosted on loopback 127.0.0.1 and any requests from host machine is trusted by wallet rpc. If someone hacks your server, rpc login does not protect much as login is stored on server 
anyways. Always treat wallets connected to internet as a hot wallet and only store as much needed for operation. The rest should be periodically sent to a cold wallet.
A hot wallet is always vulnerable to server exploits, server host access, and other ways to get on the server. Plan accordingly. 

Always run under reverse proxy/load balancer (nginx).

Still can be rigged. Never Gamble.

If you would like to donate to help me develop future monero projects:

monero:84wPRTvp1NVMHmgXBoYHd29Q3s7TNC48CWP3kqQHzdofKmy2XSbdNvaCZd1HevB9T77o4ZaAC65DFgckZzL9NfGeV8mKLfm
