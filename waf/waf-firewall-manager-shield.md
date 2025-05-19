# Comprehensive Protection with WAF, Shield, and Firewall Manager

- **WAF, Shield, and Firewall Manager**: Used together for comprehensive protection.

## AWS WAF

- **Web ACL Rules**: Define your Web ACL rules in WAF.
- **Granular Protection**: For granular protection of your resources, WAF alone is the correct choice.

## AWS Firewall Manager

- **Cross-Account Usage**: If you want to use AWS WAF across accounts, accelerate WAF configuration, and automate the protection of new resources, use Firewall Manager with AWS WAF.

## AWS Shield Advanced

- **Additional Features**: Adds additional features on top of AWS WAF, such as dedicated support from the Shield Response Team (SRT) and advanced reporting.
- **Frequent DDoS Attacks**: If you're prone to frequent DDoS attacks, consider purchasing Shield Advanced.