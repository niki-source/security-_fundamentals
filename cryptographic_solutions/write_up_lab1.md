## Overview
The purpose of lab 1(Create and Verify a Digital Signature) is to verify the authenticity and integrity of digital documents, messages, and transactions. 

Brief Description of What You Did

Tools / Environment Used (High-Level)
The lab was conducted using Alma Linux 9.1- a standalone Linux server. To create the public and private keys, the tool OpenSSL was used. 

Learning Objective / Skills Gained

Why This Lab Is Important (Real-World Relevance)


## Steps Performed

### Part 1- Creating a Private and Public Key
![Creating Directories and a private key](private_key.png)

The directories Digital_Signature, Alice, and Bob were created. In the Alice directory, a private key was created. 

The RSA algorithm was used to make the key for Alice, which will then be later used to encrypt, decrypt, or for digital signatures. 


![Creating public key from private key for Alice](public_key.png)

This command creates a public key from the private key we created for Alice. 


### Part 2- Creating a Digital Signature

![Creating a Digest File](digest.png)

The command creates a digest (a file) that is going to be hashed and encrypted by the private key I made earlier. This will be sent to Bob so he can hash the file as well and compare his result to the encrypted hash in the digital signature. 


![Create Digital Signature](digital_signature.png)
This command creates Alice's digital signature by hashing the alice_digest.txt file and encrypting the hash output with alice_privatekey.pem. The resulting file (which is the signature file) is alice_signature.bin. 


### Part 3- Receiving and Verifying the Digital Signature 

![Sending Files to Bob](sending_files.png)

This command simulates sending the files Alice's public key, the signature file, and the digest to Bob. 


### Part 4- Verifying Alice's Digital Signature (Last Part)
![Verifying Alice's Digital Signature](verify.png)

This command verifies Alice's digital signature and we received "Verified OK" for confirmation. 





