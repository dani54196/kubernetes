✅ Soluciones (ordenadas de mejor a peor)
🥇 Opción correcta: regenerar el cert con la IP pública
En el server k3s:
sudo systemctl stop k3s
Luego editás o recreás el config (según cómo lo instalaste):
Si usaste flags:
Reinstalar con:
curl -sfL https://get.k3s.io | sh -s - \
  --tls-san 163.176.142.141
O config.yaml (mejor práctica):
tls-san:
  - 163.176.142.141
Luego:
sudo systemctl start k3s
👉 Esto hace que el certificado incluya la IP pública.

checkar puertos
daniel@kubernetes-vnic:~$ sudo iptables -L -n | grep 6443

validad ip para el uso de kubectl
sudo iptables -I INPUT -p tcp -s 186.22.225.107 --dport 6443 -j ACCEPT
sudo iptables -I INPUT -p tcp -s 181.46.57.18 --dport 6443 -j ACCEPT