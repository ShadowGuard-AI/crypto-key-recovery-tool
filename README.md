![Banner](banner.png)

# crypto-key-recovery-tool
What is implemented: deriving an AES key from a password, a hex salt and
an iteration count with PBKDF2, then decrypting a ciphertext file with
that key in AES-CBC mode (PKCS7 unpadding) or AES-GCM mode (hex IV, tag
and optional AAD). A failed derivation or decryption exits 1.
What is not implemented, despite the flags existing: RSA recovery,
memory dump processing, and the known plaintext attack. Those paths
print a placeholder warning only; the RSA path also exits 1.

## Install
`git clone https://github.com/ShadowStrikeHQ/crypto-key-recovery-tool`

## Usage
`./crypto-key-recovery-tool [params]`

## Parameters
- `-h`: Show help message and exit
- `--algorithm`: No description provided
- `--key-length`: No description provided
- `--memory-dump`: Path to the memory dump file.
- `--ciphertext-file`: Path to the ciphertext file.
- `--known-plaintext-file`: Path to the known plaintext file for known plaintext attacks.
- `--password`: Password to attempt to derive key using PBKDF2
- `--salt`: No description provided
- `--iterations`: No description provided
- `--iv`: No description provided
- `--tag`: No description provided
- `--tag-length`: No description provided
- `--aad`: No description provided

## License
Copyright (c) ShadowStrikeHQ
