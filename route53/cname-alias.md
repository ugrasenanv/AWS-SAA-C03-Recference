# CNAME vs Alias

## AWS Resources
AWS Resources (e.g., Load Balancer, CloudFront) expose an AWS hostname, such as `lb1-1234.use-ease-2.elb.amazonaws.com`, and you want `myapp.mydomain.com`.

## CNAME
- Points a hostname to any other hostname (e.g., `app.mydomain.com` => `blabla.anything.com`).
- Only for non-root domain (e.g., `aka.something.mydomain.com`).

## Alias
- Points a hostname to an AWS resource (e.g., `app.mydomain.com` => `blabla.amazonaws.com`).
- Works for root domain and non-root domain (e.g., `aka.mydomain.com`).
- Free of charge.
- Native health check.