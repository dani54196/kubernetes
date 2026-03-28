sudo iptables -P INPUT ACCEPT
sudo iptables -P FORWARD ACCEPT
sudo iptables -P OUTPUT ACCEPT

sudo iptables -F

sudo ufw reset

sudo ufw allow 22
sudo ufw allow 80
sudo ufw allow 443
sudo ufw allow from 186.22.225.107 to any port 6443
sudo ufw enable



Cuando algo no conecta:
1. Ver si llega tráfico
👉 tcpdump
2. Ver si hay proceso
👉 ss -tulnp
3. Ver firewall real
👉 iptables -L -n -v


