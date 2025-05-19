# Athena - Performance Improvement

## Use Columnar Data for Cost Savings
- **Recommendation**: Use Apache Parquet or ORC.
- **Benefit**: Significant cost savings due to less data scanned.
- **Performance**: Huge performance improvement.
- **Tool**: Use AWS Glue to convert your data to Parquet or ORC.

## Compress Data for Smaller Retrievals
- **Compression Formats**: bzip2, gzip, snappy, zlib, etc.

## Partition Datasets in S3
- **Benefit**: Easy querying on virtual columns.

## Use Larger Files
- **Recommendation**: Use files larger than 128MB.
- **Benefit**: Minimize overhead.