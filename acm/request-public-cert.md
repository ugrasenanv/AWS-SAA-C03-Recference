# ACM - Requesting Public Certificates

## Steps

1. **List Domain Names**: List domain names to be included in the certificate.
    - **Fully Qualified Domain Name (FQDN)**: `corp.example.com`
    - **Wildcard Domain**: `*.example.com`

2. **Select Validation Method**: Choose between DNS Validation or Email Validation.
    - **DNS Validation**: Preferred for automation purposes.
    - **Email Validation**: Sends emails to contact addresses in the WHOIS database.

3. **DNS Validation Details**:
    - Leverages a CNAME record to DNS config (e.g., Route 53).
    - Takes a few hours to get verified.

4. **Automatic Renewal**:
    - The Public Certificate will be enrolled for automatic renewal.
    - ACM automatically renews ACM-generated certificates 60 days before expiry.