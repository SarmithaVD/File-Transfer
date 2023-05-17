# File-Transfer

LANGUAGE USED: Python

MODULES USED: 
threading: This module provides threading and synchronization primitives. It is used for creating and managing threads for each client connection.
os: This module provides a portable way of interacting with the operating system. It is used for getting the list of files in the server directory and calculating the size of a file.
re: This module provides regular expression matching operations. It is used for parsing the received data in the form of bytes.
tqdm: This module provides progress bars for loops. It is used to display the progress of file transfer.
pickle: This module implements binary protocols for serializing and de-serializing a Python object structure. It is used for serializing and de-serializing Python objects for transferring data between the server and the client.
Fernet from cryptography.fernet: This module provides a symmetric encryption algorithm that guarantees confidentiality and integrity of data. It is used for encrypting the files.
warnings: This module is used to ignore the warning messages. It is used to suppress the FutureWarning message that is displayed when a Fernet object is created without passing a bytes object as the key.
socket: This module provides access to the BSD socket interface. It is used for creating sockets for server-client communication over a network.

IDEA:
Password authentication ensures that only authorized users are able to access the data, thereby preventing unauthorized users from accessing or modifying it.
Encryption ensures that the data is secure while it is being transmitted over the network. Even if an attacker is able to intercept the data, they will not be able to read or modify it without the encryption key.
By encrypting the data before it is transmitted, the risk of data interception and theft is greatly reduced, which in turn reduces the risk of data loss.

INTRODUCTION:
The multiserver project is a Python implementation that creates a multithreaded socket server that can upload and download files from multiple clients. It provides secure data transfer by encrypting the file with Fernet encryption before uploading and decrypting after downloading. The server runs on the host machine at a specific port, and clients connect by providing a password. After authentication, the client can either download or upload files by selecting the appropriate option. The server lists all the files on the server-side when the client selects to download a file. The server can handle multiple clients simultaneously by creating a thread for each client. The project provides command-line interaction for the user to enter the number of bytes to send when uploading the file. The project uses the tqdm package to display the upload and download progress in real-time.
