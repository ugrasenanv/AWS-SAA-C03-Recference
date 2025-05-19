# Spot Instances Termination and Spot Fleets

## Spot Instances Termination

To terminate spot instances, you need to cancel the spot request first and then terminate the associated spot instances.

## Spot Fleets

Spot fleets are a set of Spot Instances and optionally, On-Demand Instances. The spot fleet tries to meet the target capacity within the price constraints.

- **Launch Pools**: Define possible launch pools, which include instance type (e.g., m5.large), OS, and AZ. You can have multiple launch pools, so the fleet can choose. The spot fleet stops launching instances when it reaches capacity or the maximum cost.

- **Strategies to Allocate Spot Instances**:
    - **lowestPrice**: Choose from the pool with the lowest price. This is suitable for cost optimization and short workloads.
    - **diversified**: Distribute across all pools. This is great for availability and long workloads.
    - **capacityOptimized**: Choose the pool with the optimal capacity for the number of instances.
    - **priceCapacityOptimized (recommended)**: Choose the pool with the highest capacity available, then select the pool with the lowest price. This is the best choice for most workloads.