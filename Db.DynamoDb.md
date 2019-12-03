#### DynamoDb

- Stored on SSD storage.
- Spread across 3 geographically distinct data centres.

**Consistency**
- Eventually consistent reads. (Default option)
- Strongly consistent reads.

Auto scaling is not activated by default.

Amazon DynamoDb Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDb that delivers up to a 10x performance improvement – from milliseconds to microseconds.

Amazon DynamoDB is integrated with AWS Lambda so that you can create *triggers* that automatically respond to events in DynamoDB Streams.