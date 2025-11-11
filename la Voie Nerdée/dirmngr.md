A background daemon that [[GnuPG]] uses for all network-related operations, like:

- 🌐 Accessing PGP keyservers
- 🔑 Fetching keys from them
- 🔏 Resolving and verifying certificates
- etc.

Think of it as GPG’s *network butler* — GPG itself doesn’t open sockets or handle TLS directly; it politely asks `dirmngr` to do it