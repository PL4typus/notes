The def of "secure" in crypto changes with time
small set of crypto components is beneficial

OpenSSH and SmartCards

 - KeX
 - Symmetric cipher
 - Asymmetric cryptography
    key/keyhole
    Signature: proof of the possession of the private key without revealing the piv key

Authenticity of server /etc/ssh/ssh_host_{...}

ssh -Q
debug output can be read to see what is offered by server.

Compression: Not a good idea. Length can be used to determine information.

PKCS#11 is the API used by application to access the cards

### FIPS140
NO OTHER CRYPTOGRAPHY ALLOWED
enforced by crypto team
enforcement done with the PELC tool
packages mustn't implement crypto but rather use the core cryptography
"vim needs crypto to run on Amiga"
Sound engineering principles:
 - Unit tested
 - separation of crypto from app code
 - Best practices
  - Zeroization of keys, acceptable key sizes standard algorithms

FIPS approves a set of algorithms (Protocols, asym, sym, modes, hashes, curves, and DRBGenerators)


