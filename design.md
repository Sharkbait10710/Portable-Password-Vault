# Features
- End-to-end encryption.
- Multi-factor authentication.
- Password sharing.
- Password generating.
- Online.
# Data Structures
# Algorithms
- Generate vault key by:
  - Appending the input username + password.
  - Hashing the appended string using PBKDF2 (Password-based Key Derivation Function 2).
- Generate authentication key by:
  - Appending the vault key above + the password.
  - Hash the appended string using PBKDF2 again (salted).
- Then, the server will send back the requested vault to the client.
- The client then uses the vault key to unlock the vault.