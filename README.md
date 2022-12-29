rapid_ping

a python wrapper that turns ping into a "rapid ping" like Cisco or Juniper

git clone https://github.com/thrve/rapid_ping.git && mv rapid_ping/rapid_ping .local/bin

echo "alias ping=rapid_ping" >> ~/.zshrc

• ॐ  ~ ➛ ping 10.205.5.250
PING 10.205.5.250 (10.205.5.250) 56(84) bytes of data.
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!.!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
!!!!!!!!!!!!!!!!!!!!^C
--- 10.205.5.250 ping statistics ---
220 packets transmitted, 219 received, 0% packet loss, time 8000ms
rtt min/avg/max/mdev = 18.67/24.810/94.381/10.244 ms

• ॐ  ~ ➛ ping 10.205.5.250 -r -c 100
PING 10.205.5.250 (10.205.5.250) 56(84) bytes of data.
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

--- 10.205.5.250 ping statistics ---
100 packets transmitted, 100 received, 0% packet loss, time 3000ms
rtt min/avg/max/mdev = 18.818/24.658/116.708/11.426 ms

• ॐ  ~ ➛ ping 10.205.5.250 -r -c 100 -s 1500
PING 10.205.5.250 (10.205.5.250) 1500(1528) bytes of data.
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

--- 10.205.5.250 ping statistics ---
100 packets transmitted, 100 received, 0% packet loss, time 3000ms
rtt min/avg/max/mdev = 18.613/25.201/87.104/8.805 ms


