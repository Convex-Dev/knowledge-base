- It is generally shown as a hexadecimal string, looking something like:
- ```clojure
  0x8506cc53f9b7dD152C9BB5386d50C360ff85EFD043049aea55B44362D92C0E1C
  ```
- Technically, the Account Key of a User Account is an  `Ed25519`  Public Key. You must be in possession of the corresponding private key in order to digitally sign transactions for that Account. Actor Accounts have Addresses that are generated via SHA3-256 hash functions (and therefore do not have a corresponding private key, and no transactions can be submitted for them).