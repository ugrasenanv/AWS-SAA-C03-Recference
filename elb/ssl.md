# SSL/TLS - Basics

- An SSL Certificate allows traffic between your clients and your load balancer to be encrypted in transit (in-flight encryption).

- SSL refers to Secure Socket Layer, used to encrypt connections. TLS refers to Transport Layer Security, which is a newer version. Nowadays, TLS certificates are mainly used, but people still refer to them as SSL.

- Public SSL certificates are issued by Certificate Authorities (CA). SSL certificates have an expiration date (you set) and must be renewed.

# Load Balancer - SSL Certificates

- The load balancer uses an X.509 certificate (SSL/TLS server certificate). You can manage certificates using ACM (AWS Certificate Manager) or you can create and upload your own certificates.

- For an HTTPS listener, you must specify a default certificate. You can add an optional list of certificates to support multiple domains.

- Clients can use SNI (Server Name Indication) to specify the hostname they reach. You also have the ability to specify a security policy to support older versions of SSL/TLS.

# SSL - Server Name Indication (SNI)

- SNI solves the problem of loading multiple SSL certificates onto one web server (to serve multiple websites). It's a newer protocol, and requires the client to indicate the hostname of the target server in the initial SSL handshake.

- The server will then find the correct certificate, or return the default one.

- Note: SNI only works for ALB & NLB (newer generation), and CloudFront. It does not work for CLB (older generation).