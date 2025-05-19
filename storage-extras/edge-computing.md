# Edge Computing Overview

Edge computing is a distributed computing paradigm that brings computation and data storage closer to the location where it is needed, to improve response times and save bandwidth. This approach is particularly beneficial in scenarios where connectivity to a centralized or cloud-based location is limited, unreliable, or not available.

## Key Characteristics

- **Proximity to Data Source**: Edge computing devices are deployed in close physical proximity to the source of data, such as sensors or cameras.
- **Operational in Remote Locations**: Ideal for environments with limited or no internet access, such as remote industrial sites, vehicles in transit, or maritime operations.
- **Reduced Latency**: By processing data locally, edge computing reduces the latency involved in sending data to a central data center or cloud for processing.

## Edge Computing with AWS Snowball Edge and Snowcone

AWS provides specialized devices like Snowball Edge and Snowcone for edge computing tasks. These devices are designed to operate in environments where traditional computing infrastructure is impractical.

### Use Cases

1. **Preprocess Data**: Data can be filtered, aggregated, or transformed at the edge, reducing the volume of data that needs to be transmitted to the cloud.
2. **Machine Learning at the Edge**: Deploy machine learning models directly on edge devices to make predictions or analyses in real-time, without the need for cloud connectivity.
3. **Transcoding Media Streams**: Media captured at the edge can be transcoded on the device itself, optimizing it for transmission or storage.

### Data Transfer to AWS

When necessary, these devices can be shipped back to AWS. This allows for the efficient transfer of large volumes of processed or raw data to the cloud for further analysis, storage, or long-term archiving.