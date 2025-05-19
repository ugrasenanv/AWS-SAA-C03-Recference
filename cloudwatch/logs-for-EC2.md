# CloudWatch Logs for EC2

By default, no logs from your EC2 machine will go to CloudWatch. To push the log files you want, you need to run a CloudWatch agent on your EC2 instance. Ensure that IAM permissions are correctly configured. The CloudWatch log agent can also be set up on-premises.

## CloudWatch Logs Agent

- **Old Version**:
    - Can only send logs to CloudWatch Logs.

## CloudWatch Unified Agent

- **Additional Metrics**:
    - Collects additional system-level metrics such as RAM, processes, etc.
- **Log Collection**:
    - Collects logs to send to CloudWatch Logs.
- **Centralized Configuration**:
    - Uses SSM Parameter Store for centralized configuration.

## CloudWatch Unified Agent - Metrics

- **Collection**:
    - Collects metrics directly on your Linux server/EC2 instance.
- **Metrics**:
    - **CPU**: Active, guest, idle, system, user, steal.
    - **Disk**: Free, used, total; Disk IO: Writes, reads, bytes, IOPS.
    - **RAM**: Memory usage.
    - **Netstat**: Network statistics.
    - **Processes**: Process information.
    - **Swap Space**: Swap memory usage.
- **Note**: Out-of-box metrics for EC2 include disk, CPU, and network (2 levels).