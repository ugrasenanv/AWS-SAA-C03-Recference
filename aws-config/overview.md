# AWS Config

AWS Config helps with auditing and recording compliance of your AWS resources. It helps record configurations and changes over time.

## Questions Solved by AWS Config

- Is there unrestricted SSH access to my security groups?
- Do my buckets have any public access?
- How has my ALB configuration changed over time?

## Features

- **Alerts**: You can receive alerts (SNS notifications) for any changes.
- **Per-Region Service**: AWS Config is a per-region service.
    - Can be aggregated across regions and accounts.
- **Data Storage**: Possibility of storing the configuration data into S3 (analyzed by Athena).