# socialsend-util

**Utility functions for SocialSend hashes and targets**

## Usage

`npm install SocialSend/socialsend-util`

### Methods

#### `toHash(hex)`

Takes a hex string that contains a SocialSend hash as input, and returns a SocialSend-protocol-friendly little-endian Buffer. Throws an error if the hex string is not of length 64 (representing a 256-bit hash).

#### `compressTarget(target)`

Converts the difficulty target `target` to its compact representation (used in the "bits" field in block headers). `target` should be a `Buffer` (little-endian, the zeroes should be at the end). Returns a `number`.

#### `expandTarget(bits)`

Converts the compressed target integer `bits` to its target hash representation. Returns a `Buffer`.
