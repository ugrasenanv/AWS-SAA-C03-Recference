## Weighted Routing Policy

- Allows controlling the percentage of requests directed to each specific resource by assigning a relative weight to each DNS record.
- The traffic percentage for a specific record is calculated as: 
  - `Traffic (%) = Weight of a specific record / Sum of all weights for all records`.
- The weights assigned to records do not need to sum up to 100.
- All DNS records must have the same name and type to be considered part of the weighted routing policy.
- Weighted routing can be associated with health checks to ensure traffic is only directed to healthy resources.
- Common use cases include load balancing traffic between different regions or for A/B testing new versions of an application.
- Assigning a weight of 0 to a record effectively stops sending traffic to that resource.
- If all records have a weight of 0, traffic will be distributed equally among all records.