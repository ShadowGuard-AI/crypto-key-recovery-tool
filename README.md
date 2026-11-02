![The churchyard before it is identified: the path close with gravel, fallen needle litter and one dropped berry near, the yew whole in the middle band with its fluted hollow trunk and the bare earth ring beneath its canopy, and the church tower far behind a wall with a blank clock face and unlit windows, with no letter of any kind](intro-banner.png)

# crypto-key-recovery-tool

Title block: the name above is set in Bilbo Swash Caps in darkened jade on bamboo pale, ruled beneath like the opening of a parish register, with a small berry spray drawn once at the left of the first heading only and nowhere repeated as decoration.

![A single yew berry on a short spray of dark needles on a bamboo pale card: lotus pink for the cup, jade for the needle spray, monsoon grey for the shadow beneath, the pale cup and the seed showing at the mouth of the berry, and the name below in parish register capitals](logo.png)

![A wide churchyard in the hour before evening service: a low church wall and leaning headstones with their faces turned away at the left, the church porch in shadow in the middle, and the yew filling the right half and rising beyond the top edge with berries as lotus pink points, a wooden bench facing the tree with the repo name painted small on its back board](banner.png)

![The churchyard in three bands: the church tower and wall unmoving in the far band, the yew canopy stirring at its outer edge in the middle band while berries drop one at a time to the bare earth, and fallen needle litter drifting a short distance along the path in the near band before resting again](scene.svg)

![Major separator](sep-heavy.svg)


# crypto-key-recovery-tool
What is implemented: deriving an AES key from a password, a hex salt and
an iteration count with PBKDF2, then decrypting a ciphertext file with
that key in AES-CBC mode (PKCS7 unpadding) or AES-GCM mode (hex IV, tag
and optional AAD). A failed derivation or decryption exits 1.
What is not implemented, despite the flags existing: RSA recovery,
memory dump processing, and the known plaintext attack. Those paths
print a placeholder warning only; the RSA path also exits 1.

> Vestry notice, pinned: the install line below names the wrong organisation, ShadowStrikeHQ. The right name is ShadowGuard-AI. The line itself is preserved as printed.

![Minor separator](sep-light.svg)

## Install
`git clone https://github.com/ShadowStrikeHQ/crypto-key-recovery-tool`

> Vestry notice, pinned: the usage line below is a placeholder that the parser accepts in no form. The gathered form the parser does accept is written out in full on the website register.

![Minor separator](sep-light.svg)

## Usage
`./crypto-key-recovery-tool [params]`

> Vestry notice, pinned: three paths in this list end at a warning only: the RSA path, the memory dump path and the known plaintext path. Their entries stand here as the README prints them.

![Minor separator](sep-light.svg)

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

> Vestry notice, pinned: the licence line below names the wrong organisation. The LICENSE file in the repository holds the MIT License text, and the two are left standing side by side without reconciliation.

![Minor separator](sep-light.svg)

## License
Copyright (c) ShadowStrikeHQ

![Major separator](sep-heavy.svg)

## Facts from the code, stated in the prose

Facts from the code, stated in the prose. This record names: PBKDF2, SHA256, AES-CBC, PKCS7, AES-GCM, 100000, latin-1, exit 1, python3 main.py --algorithm AES --key-length BITS --password TEXT --salt HEX --iterations COUNT --ciphertext-file PATH --iv HEX, --tag HEX, --tag-length NUMBER, --aad HEX. The key length is given in bits and halved into bytes by division at the call. The presence of a tag alone decides the mode, since no entry anywhere lets a caller name a mode directly. A tag length is required whenever a tag is present. Where an opening succeeds, the recovered text is printed to the console decoded byte by byte through latin-1, there being no output file control in this program at all. An empty recovered text counts as success. Every value on this page is named by kind; no secret value of any kind is written anywhere on the page.
