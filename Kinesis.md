#### Kinesis

It is a platform on AWS to send your streaming data to.
It makes it easy to load and analyse streaming data, and also providing the ability for you to build your own custom applications for your business needs.

3 different types of Kinesis.

**Kinesis Streams**
It is a place to store data produced by producers from 24h to 7 days into shards where consumers can analyse the data.

**Kinesis Firehose**
It is a place to analyse the data using lambda and output the result to S3 or ElasticSearch cluster. It can also be sent to Redshift through S3. There is no data persistence.

**Kinesis Analytics**
It works with Kinesis Streams and Kinesis Firehoseand can analyse the data on the fly inside either service and then stores the data either in S3, Redshit or ElascticSearch cluster. 