# MITM-ARP-Spoofing

## Docker Version

## Instructions

This repo contains required files in order to get a succesful ARP Spoofing attack between computer/server and router in a controlled environmet ( a docker container )

The tcp_client.py and tcp_server.py are sending each other messages continuously. The job is to intercept these messages from another endpoint located in the same network. The technique is working by sending continuously ARP replies to the server and the router despite of ARP requests sent by either server or router, replies that contain spoofed MAC adress of the attacker.

In order to get this script working you need to deploy the docker container found in the 'docker' folder and then run the files either on server and router. After this step, you need to run the 'ManInTheMiddle.py' from attacker's machine. In case of a sucessful attack, when running 'tcpdump -SntvXX -i any' command in another terminal from attacker's machine you will see the traffic between server and router. 
