# IP-sweep
A simple program which is written in bash script to get active ip addresses (devices) in your local network. Moreover, using Nmap to get variety of information
of the connected devices such as open ports, detection of operating systems...etc.

# What do you need to run the program
1- Linux

2- Nmap

# How to use 

after downloading ipsweep.sh go to terminal and enter the following:

1- ``` ./ipsweep.sh 192.168.1 > ips.txt ```


  at this step, it depends on the subnet mask which is 255.255.0.0, because it's the most popular for our private networks. 
  So, you would you enter the third octet and the program will iterate from 1 to 254 at the last octet.
  Then the program will create a file called ips.txt which would have the result of the ip addresses. 

2-  ``` for ip in $(cat ips.txt); do nmap $ip; done ```

  here we do Nmap on the ip addresses we got in ips.txt


