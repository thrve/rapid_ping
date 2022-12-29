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

• ॐ  ~ ➛ ping 10.205.5.3 -r
PING 10.205.5.3 (10.205.5.3) 56(84) bytes of data.
......................................................................^C
--- 10.205.5.3 ping statistics ---
70 packets transmitted, 0 received, 100% packet loss, time 1000

to use normal ping add backslash before the command: \ping [...] ip addres

• ॐ  ~ ➛ \ping 10.205.5.250
PING 10.205.5.250 (10.205.5.250) 56(84) bytes of data.
64 bytes from 10.205.5.250: icmp_seq=1 ttl=62 time=22.2 ms
64 bytes from 10.205.5.250: icmp_seq=2 ttl=62 time=27.6 ms
64 bytes from 10.205.5.250: icmp_seq=3 ttl=62 time=24.4 ms
64 bytes from 10.205.5.250: icmp_seq=4 ttl=62 time=19.3 ms
^C
--- 10.205.5.250 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3005ms
rtt min/avg/max/mdev = 19.338/23.399/27.584/3.018 ms
