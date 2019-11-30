#### SQS (Simple Queue Service)

It is a way to store messages in a queue while waiting for a compute to process them.

It decouples components of an application to run them independently.

This service helps to reduce the problem of producers producing work faster than the consumer can process it. 

Messages can contain up 256 KB of text in any format.
Messages can be up 2 GB but they will be stored on S3.

Applications retrieves the messages polling the Amazon SQS API.

Two different types:
-   Standard queues
    -   Nearly unlimited quantity of messages in the queue.
    -   Messages will be delivered at least once (or more rarely).
    -   Occasionally a message can be delivered out of order. 
    -   Visibility Time Out is the amount of time that the message is invisible in the queue after a reader picks-up that message. If the job is not processed the message will become visible again. Visibility timeout maximum is 12 hours.
    -   Messages can be kept in the queue from 1 minute to 14 days. Default is 4 days.
-   FIFO queues:
    - Messages will be delivered exactly once and in strictly in order.
    - No duplicates in the queue.
    - 3000 messages per second.
    - Supports message groups that allow multiple ordered message groups within a single queue.

Consumers must delete messages in the queue when they finish processing them in order for the messages not to become available again.

**Polling**
Regular shot polling returns immediately even if the queue is empty. Long polling does not return a response until a message arrives to the queue or the long poll times out.