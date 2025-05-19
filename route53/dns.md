# Domain Name System (DNS)

DNS, or Domain Name System, is a critical component of the internet's infrastructure, designed to translate human-friendly hostnames into machine-readable IP addresses. This system allows users to access websites using domain names, such as `www.google.com`, instead of having to remember complex IP addresses like `172.217.18.36`.

## Key Features

- **Translation**: Converts domain names to IP addresses, enabling browsers to load internet resources.
- **Hierarchical Structure**: Organizes its naming structure in a hierarchical manner, allowing for efficient query resolution.
- **Backbone of the Internet**: Acts as the internet's phone book, essential for the functionality of the global internet.

## How DNS Works

When a user enters a domain name into their browser, the DNS system is responsible for translating that domain name into an IP address. This process involves multiple steps:
1. **Local DNS Resolver**: The user's device queries a local DNS resolver, such as the one provided by the ISP.
2. **Root DNS Servers**: If the local resolver does not have the IP address, it queries the root DNS servers to find the authoritative name servers for the top-level domain (TLD).
3. **TLD Name Servers**: The root DNS servers return the IP addresses of the TLD name servers, which are responsible for the specific top-level domain (e.g., `.com`, `.org`, `.net`).
4. **Authoritative Name Servers**: The TLD name servers provide the IP addresses of the authoritative name servers for the domain in question.
5. **Domain Name Resolution**: The authoritative name servers return the IP address of the domain, allowing the user's device to connect to the desired website or service.

- Top Level Domain (TLD): .com, .us, .in, .gov,...
- Second Level Domain (SLD): amazon.com, google.com,...

DNS plays a pivotal role in how users interact with the internet, making it possible to access websites and services through easy-to-remember domain names.

![DNS Overview](../z_resources/images/route53/dns-overview.png)