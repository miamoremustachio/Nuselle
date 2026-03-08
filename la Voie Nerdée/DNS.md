When a user types a domain name (like [google.com](https://google.com)) into a web browser, this will initiate a request to Google’s web server asking for content (the Google homepage).

Using the provided [[IP address]], Google can send a response back to the user’s device.

The system that orchestrates all this is called *DNS*.
It works like a phonebook for IP addresses so that users can access websites using human-readable domain names.

## 🗝️ Key aspects

- Converts domain names into IP addresses
- Works using a hierarchical structure of servers
- Supports caching

## 🗃️ Structure

### ♻️ DNS Resolver

- Acts as a middleman between a client and nameservers.
- After receiving a DNS query from a web client, DNS resolver will either respond with cached data, or send a request to a root nameserver, followed by another request to a TLD nameserver, and then one last request to an authoritative nameserver.
- After receiving a response from the authoritative nameserver containing the requested IP address, DNS resolver then sends a response to the client.

### 🫚 Root Server

- Are at the highest level of the DNS hierarchy.
- Responsible for directing DNS queries to the proper TLD servers.
- Crucial for directing DNS queries to the correct locations.

### TLD Servers

- Manage domain extensions like `.com`, `.org`, `.net` and others.
- For example, a `.com` TLD nameserver contains information for every website that ends in ‘.com’.
- If a user was searching for `google.com`, after receiving a response from a root nameserver, the DNS resolver would then send a query to a `.com` TLD nameserver, which would respond by pointing to the authoritative nameserver for that domain.

### Authoritative Servers

- Store the actual DNS records for domain names.
- Responsible for providing the correct IP addresses that allow users to reach websites.

![[complete-dns-lookup-and-webpage-query.webp]]




[^1]: Sources:
	https://www.cloudflare.com/learning/dns/what-is-dns/
	https://www.cloudflare.com/learning/dns/dns-server-types/
