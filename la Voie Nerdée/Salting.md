In cryptography, a *salt* is random data added to a password before hashing to create a unique value for every hashed password.
This makes it impossible for an attacker to derive passwords from their hashes using [[rainbow tables]], as they would need to create separate tables for every single salt.

# 🧂 How it works

1. When user creates a password, a unique salt is generated for them
2. The password and the salt are combined and then hashed using a secure algorithm (like bcrypt or Argon2)
3. The resulting value is stored in the database;
   The original password is *not* stored
4. During login, the stored salt is retrieved and combined with the entered password
5. This new combination is re-hashed and compared to the stored hash: if they match, the login is successful