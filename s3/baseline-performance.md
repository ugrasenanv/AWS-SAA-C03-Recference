# Baseline Performance for Amazon S3

Amazon S3 is designed to scale automatically to handle high request rates, ensuring robust performance for your applications. Here's a quick overview of what you can expect in terms of latency and request handling:

## Latency

- **Average Latency**: 100-200 ms for most operations, providing a responsive experience for end-users and systems interacting with S3.

## Request Rate

- **PUT/COPY/POST/DELETE Requests**: S3 can handle at least 3500 of these requests per second for each prefix within a bucket.
- **GET/HEAD Requests**: For read operations, S3 can process at least 5500 requests per second per prefix.

## Prefixes and Scalability

- **Unlimited Prefixes**: There is no limit to the number of prefixes you can have in a bucket, allowing for flexible organization and scalability.
- **Prefix Example**: An object path like `bucket/folder1/sub1/file` translates to a prefix of `folder1/sub1`.

## Maximizing Throughput

By distributing your read operations (GET/HEAD requests) evenly across multiple prefixes, you can significantly increase your total request rate. For example, with four prefixes, you could achieve:

- **22,000 Requests/Second for GET and HEAD**: Spreading reads across `folder1/sub1`, `folder2/sub2`, `/1/`, and `/2/` enables you to maximize throughput and leverage S3's scalability.

This performance baseline ensures that S3 can meet the demands of high-load applications, making it a reliable choice for storage solutions that require fast access and high throughput.