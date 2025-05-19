## Objects in S3

### Key Concepts

- **Objects and Keys**: In S3, objects (files) are identified by a unique key, which represents the full path of the object within a bucket. For example:
    - `s3://my-bucket/my_file.txt`
    - `s3://my-bucket/my_folder/another_folder/my_file.txt`
- **Key Composition**: A key is composed of a prefix (the path) and the object name. There's no actual concept of "directories" within buckets, but the use of slashes ("/") in keys simulates a directory structure.
- **Object Values**: The value of an object is the content of its body. The maximum size for an object is 5TB. For objects larger than 5GB, a "multi-part upload" process must be used.
- **Metadata**: Objects can have metadata, which are a list of text key/value pairs that can be system-defined or user-defined.
- **Tags**: Objects can also have tags, which are Unicode key/value pairs, with a limit of up to 10 tags per object. Tags are useful for security and lifecycle management.
- **Version ID**: If versioning is enabled on the bucket, each object will have a version ID to distinguish different versions of the same object.