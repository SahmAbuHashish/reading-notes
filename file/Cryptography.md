# Reading Questions


### What is the basic principle behind the Caesar Cipher, and how was it used historically?

- The Caesar Cipher is a simple substitution cipher that shifts each letter in the plaintext by a fixed number of positions down the alphabet. The basic principle is to replace each letter in the message with a letter that is a fixed number of positions ahead (or behind) in the alphabet.

- Historically, the Caesar Cipher was used by Julius Caesar to protect sensitive military information during communication. It served as a means of encryption, where the intended recipient knew the fixed shift value and could decipher the message by shifting the letters back to their original positions.

---

### What are the key differences between symmetric and asymmetric encryption? How is asymmetric used in secure communication today?

- Symmetric encryption uses a single shared key for both encryption and decryption. The same key is used by both the sender and the recipient. It is typically faster and more efficient for encrypting and decrypting large amounts of data. However, it requires a secure mechanism to share the key beforehand.

- Asymmetric encryption, also known as public-key encryption, uses a pair of mathematically related keys: a public key and a private key. The public key is used for encryption, while the private key is used for decryption. One key cannot be feasibly derived from the other. Asymmetric encryption provides key exchange, digital signatures, and secure communication without requiring a prior shared key. It is commonly used in secure communication protocols like HTTPS, SSH, and PGP.

---

### How do computers generate random numbers, and what are the differences between true random number generation (TRNG) and pseudo-random number generation (PRNG)? Discuss their use cases in cryptography.

Computers generate random numbers using algorithms called random number generators (RNGs). True random number generation (TRNG) relies on unpredictable physical processes, such as atmospheric noise or radioactive decay, to generate random values. TRNGs provide true randomness but can be slower and require specialized hardware.

Pseudo-random number generation (PRNG) algorithms, use deterministic mathematical formulas and an initial seed value to generate seemingly random numbers. PRNGs are faster and more readily available in software, but their outputs are deterministic and repeatable if the same seed is used.

- TRNGs are preferred for generating cryptographic keys or nonces, as true randomness ensures stronger security. 
- PRNGs are used for generating encryption keys in situations where speed and efficiency are crucial, and the cryptographic strength relies on the secrecy of the seed value.

---

### What’s the difference between encryption and decryption? Explain with an analogy.

Encryption is the process of converting plaintext into ciphertext using an encryption algorithm and a key. It scrambles the original message in a way that it becomes unreadable and unintelligible to unauthorized parties. 

- An analogy for encryption is locking a letter in a box using a padlock. The letter represents the plaintext, the padlock is the encryption algorithm, and the key to open the padlock is the encryption key. Only those with the correct key can unlock the box and read the letter.

Decryption,is the reverse process of encryption. It involves converting ciphertext back into plaintext using a decryption algorithm and the corresponding key. It restores the original message from the encrypted form. 

- Using the analogy, decryption is opening the locked box with the correct key, retrieving the letter, and reading its contents