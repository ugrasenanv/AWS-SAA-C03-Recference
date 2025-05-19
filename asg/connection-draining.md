# Connection Draining / De-registration Delay

- Known as "Connection Draining" for Classic Load Balancer (CLB) and "De-registration Delay" for Application Load Balancer (ALB) & Network Load Balancer (NLB).

- This feature allows time to complete "in-flight requests" while the instance is de-registering or becoming unhealthy.

- It stops sending new requests to the EC2 instance which is de-registering.

- The time range is between 1 to 3600 seconds, with the default being 300 seconds.

- This feature can be disabled by setting the value to 0.

- If your requests are short, it's recommended to set this value to a low number.