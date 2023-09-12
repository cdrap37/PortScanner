# PortScanner
 Developed a Python-based port scanner to analyze target systems for open ports, enhancing network security and identifying potential vulnerabilities.

The script starts by importing the socket library, which provides the necessary functionality for creating and managing network sockets. The script then sets the target_host variable to the address of the target system you want to scan (in this case, "infosecdraper.com"). Then defines a list called target_ports, which contains the list of port numbers to scan. The script will check if each of these ports is open on the target system. The port_scanner function takes two parameters: target_host (the target system's address) and port (the port number to check). It creates a socket object (client) using the socket.socket() method. AF_INET indicates that it's an IPv4 address, and SOCK_STREAM specifies a TCP socket. It sets a timeout for the connection attempt using socket.setdefaulttimeout(1). This means that if a connection attempt takes longer than 1 second, it will time out. It attempts to connect to the target host and port using client.connect((target_host, port)). If successful, it means the port is open, and it prints a message indicating that the port # is open. It closes the socket using client.close() to release system resources. It uses a try...except block to handle exceptions like socket.timeout and ConnectionRefusedError. If the connection times out or is refused, it means the port is closed or unreachable, and it passes without printing anything. The script then iterates through the list of target_ports using a for loop. For each port in the list, it calls the port_scanner function with the current target_host and port number. 

Copied code over from VS code
