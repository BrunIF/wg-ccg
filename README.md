# Wireguard client configuration generator (wg-ccg)

## Additional software

Please install `qr` utility and `pillow` library. Also install wirequrd tools

```bash
pip3 install qrcode[pil]
```

```bash
# For Mac
brew install wg-tools
# for Linux Ubuntu
sudo apt install wireguard
```

## Configure

Please rename file server_info.example and fill correct data

```bash
cp server_info.example server_info
```

You can change DNS to own or public (like Google DNS)

```ini
DNS = 1.2.3.1
```

or

```ini
DNS = 8.8.8.8, 8.8.4.4
```

After you need change `PublicKey` from your Wireguard server and `Endpoint` (IP and Port)

## Usage

Generate client configuration for client and server

```bash
./wg-ccg "10.10.10.2" "Test user"
```

All configuration user files (conf and png) you can find in `clients` folder.
Configuration for sever find in `server-append.conf` file.