# Cryptography Notes

## Overview of Cryptography
Cryptography secures data against unauthorized access, modification, and interception through encryption, hashing, and digital certificates.

---

## Symmetric vs. Asymmetric Encryption

### Symmetric Encryption
Uses a **single shared secret key** for both encryption and decryption.
* **Pros:** Fast, efficient for large datasets.
* **Cons:** Key distribution challenge.
* **Common Algorithms:** AES (Advanced Encryption Standard), ChaCha20, 3DES (legacy).

### Asymmetric Encryption
Uses a **key pair**: a **Public Key** for encryption/verification and a **Private Key** for decryption/signing.
* **Pros:** Secure key exchange, provides non-repudiation.
* **Cons:** Computationally slower.
* **Common Algorithms:** RSA, ECC (Elliptic Curve Cryptography), Diffie-Hellman (key exchange).

---

## Hashing
A one-way mathematical function that converts input data of any size into a fixed-length output (hash digest).
* **Properties:** Deterministic, irreversible, collision-resistant, avalanche effect.
* **Common Algorithms:**
  * **MD5:** 128-bit hash. Deprecated and cryptographically broken due to collisions.
  * **SHA-256:** Part of SHA-2 family, produces 256-bit hash. Secure and widely used in digital certificates and blockchain.

---

## Digital Certificates & SSL/TLS
* **Digital Certificate (X.509):** Binds a public key to an identity (domain name or organization) validated by a trusted Certificate Authority (CA).
* **SSL/TLS Protocol:** Encrypts communications at the transport layer. TLS 1.3 is the modern secure standard.
* **Handshake Process:** Negotiates cipher suites, authenticates the server via digital certificate, and establishes symmetric session keys.

---

## OpenSSL Practical Experiment

Below are command-line experiments conducted with `openssl` to demonstrate hashing, symmetric encryption, and asymmetric key generation:

### 1. Hashing Data with MD5 & SHA-256
```bash
# Echo text and generate SHA-256 hash
echo -n "Lab Test Data" | openssl dgst -sha256

# Generate MD5 hash for comparison
echo -n "Lab Test Data" | openssl dgst -md5
```

### 2. Symmetric Encryption using AES-256-CBC
```bash
# Encrypt a file using AES-256-CBC
openssl enc -aes-256-cbc -salt -in secret.txt -out secret.enc -k MySecretPassword

# Decrypt the encrypted file
openssl enc -d -aes-256-cbc -in secret.enc -out secret_decrypted.txt -k MySecretPassword
```

### 3. Asymmetric Key Pair Generation (RSA)
```bash
# Generate 2048-bit RSA Private Key
openssl genpkey -algorithm RSA -out private_key.pem -pkeyopt rsa_keygen_bits:2048

# Extract Public Key from Private Key
openssl rsa -pubout -in private_key.pem -out public_key.pem
```
