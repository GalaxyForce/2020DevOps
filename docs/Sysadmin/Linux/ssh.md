## SSH

---

### 

---

### Use RSA private key to generate public key

```
#produce a public-private key pair
openssl genrsa -out key.pem 1024

#extract the public key and print that out
openssl rsa -in key.pem -pubout > pubkey.pub

#To just output the public part of a private key
openssl rsa -in key.pem -pubout -out pubkey.pem

#to get a usable public key for ssh puerposes, use ssh-keygen
ssh-keygen -y -f key.pem > pubkey.pub
```

Refer:https://stackoverflow.com/questions/5244129/use-rsa-private-key-to-generate-public-key


