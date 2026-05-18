# Connessione del client tramite CLI
Installare openvpn
```bash
sudo apt-get update
sudo apt-get install openvpn
```
## Configurazione
copiare la configurazione
```bash
cp example.ovpn /etc/openvpn/client.conf
```
autostart 
```bash
sudo systemctl enable openvpn@client.service
```
avvio
```bash
sudo systemctl start openvpn@client.service

# Status
sudo systemctl status openvpn@client.service
```

### Avvio manuale per debugs
```bash
sudo openvpn --config client.ovpn
```