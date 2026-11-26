Manage a batch job or Fargate Container 
- Submit a batch job or Fargate task 
- If task fails or succeeds notify via SNS

Transfer Data Records 
- Load up a DynamoDB table
- Add each DynamoDB item to the queue
- As each item is processed remove the item from the DynomoDB table
- when there are no more records report successfully complete