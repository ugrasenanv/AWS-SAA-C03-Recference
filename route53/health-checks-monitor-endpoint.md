# Monitoring an Endpoint with Route 53 Health Checks

Route 53 Health Checks are designed to monitor the availability and health of your endpoints. Here's how you can configure health checks for an endpoint:

## Global Health Checkers

- Approximately 15 global health checkers will assess the health of the endpoint.

## Health/Unhealthy Threshold

- The default threshold for marking an endpoint as healthy or unhealthy is set to 3.

## Interval

- Health checks are performed every 30 seconds by default.
- This interval can be reduced to 10 seconds for a higher cost, providing more frequent checks.

## Supported Protocols

- Health checks can be conducted over HTTP, HTTPS, and TCP protocols.

## Health Evaluation

- If more than 18% of the health checkers report the endpoint as healthy, Route 53 considers the endpoint to be in a healthy state. Otherwise, it is marked as unhealthy.

## Location Selection

- You have the option to select specific locations from which Route 53 should perform health checks.

## Response Code Criteria

- Health checks pass if the endpoint responds with a status code in the 2xx or 3xx range.

## Response Content Criteria

- Health checks can also be configured to pass or fail based on the presence of specific text within the first 5120 bytes of the response.

## Firewall/Router Configuration

- Ensure your router or firewall is configured to allow incoming requests from Route 53 health checkers to reach your endpoint.