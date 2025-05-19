## Hibernate

Hibernate allows the in-memory (RAM) state of an instance to be preserved. This results in a much faster boot time as the OS is not stopped or restarted. Under the hood, the RAM state is written to a file in the root EBS volume.

Use cases for hibernation include long-running processes, saving the RAM state, and services that take time to initialize.

### Important Notes

- The instance's RAM size must be less than 150GB.
- Hibernation is not supported for bare metal instances.
- The root volume must be an EBS volume, encrypted, not an instance store, and large enough to store the RAM state.
- Hibernation is available for On-Demand, Reserved, and Spot instances.
- An instance cannot be hibernated for more than 60 days.