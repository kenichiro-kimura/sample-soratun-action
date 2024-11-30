# sample-soratun-action

This is a sample workflow file that connect to SORACOM with [SORACOM Arc](https://soracom.jp/services/arc/) using [soratun](https://github.com/soracom/soratun/).

# How to use

Create reopository secrets belows. See also [documents of soratun](https://users.soracom.io/ja-jp/docs/arc/create-soratun-settings-file/)

- ARC_SIMID : sim id of virtual sim
- ARC_PRIVATE_KEY : PrivateKey in wireguard.conf
- ARC_PUBLIC_KEY : PublicKey in '[Peer]' section in wireguard.conf
- ARC_ENDPOINT : Endpoint in '[Peer]' section in wireguard.conf
- ARC_CLIENT_PEER_PUBLIC_KEY : Client Peer Public Key (See also [documents](https://users.soracom.io/ja-jp/docs/arc/check-connection-settings/))
- ARC_ADDRESS : Address in wireguard.conf, without '/32'.

And also create repository variables.
  
- ARC_ALLOWED_IPS : AllowedIPs in wireguard.conf like `[ "100.127.0.0/16" , "54.250.252.67/32" ]`

# Warning

This workflow uses priviledged container, so please make sure to pay close attention to security.
