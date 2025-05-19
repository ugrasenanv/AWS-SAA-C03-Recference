# Config Rules

## Types of Rules

- **AWS Managed Config Rules**: Can use AWS managed config rules (over 75).
- **Custom Config Rules**: Can make custom config rules (must be defined in AWS Lambda).
    - Example: Evaluate if each EBS disk is of type gp2.
    - Example: Evaluate if each EC2 instance is t2.micro.

## Rule Evaluation

- **Triggering**:
    - For each config change.
    - And/or: At regular time intervals.

## Limitations

- AWS Config Rules does not prevent actions from happening (no deny).

## Pricing

- No free tier.
- $0.003 per configuration item recorded per region.
- $0.001 per config rule evaluation per region.