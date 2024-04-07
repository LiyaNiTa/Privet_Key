# Privet_Key

Server

[Interface]
PrivateKey = 9TeQbAALAKubrzi/XyJQFWZBtrSYv9Go/XI/qsZN2XY=
Address = 10.0.0.1/24 #Указывается адрес для vpn-сети, может быть изменен по вашему усмотрению
ListenPort = 51820
PostUp = iptables -A FORWARD -i %i -j ACCEPT; iptables -t nat -A POSTROUTING -o **ens18** -j MASQUERADE
PostDown = iptables -D FORWARD -i %i -j ACCEPT; iptables -t nat -D POSTROUTING -o** ens18 **-j MASQUERADE


[Peer]
PublicKey = SVnpueFZnwST5deVpaVzB+FBPGx3n9tsGtw8GQeNERs=
AllowedIPs = 10.0.0.2/32 #В данном поле указывается разрешенный диапазон IP для клиентов


Server 9TeQbAALAKubrzi/XyJQFWZBtrSYv9Go/XI/qsZN2XY=
Client SVnpueFZnwST5deVpaVzB+FBPGx3n9tsGtw8GQeNERs=
