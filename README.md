
# lambda_image_resizer


## Creating S3 bucket
''' Go to aws console. 
    S3>S3 bucket> create bucket
    bucket name e.g. src-bkt
    Leave everything default setting and create bucket
    '''

### Role and Policy
''' Go to IAM >Policy> create Policy
   a. Service: S3
   b. Read > Get Object
   c. Resources: 
          specific
          ADD ARNS
              - Resource Bucket name: enter the resource bucket name from s3 src bucket and ARNS from s3 bucket properties sections.
              - Resource Object name: Any Object name
              - Resource ARN: Copy ARN from source bucket
              '''

  ''' ### For Destination Bucket:
     a. Service: S3
     b. Write: PUT OBJECT
     c. Resources: 
          Specific: 
          ADD ARNS:
              - Resource Bucket name: enter the resource bucket name from s3 src bucket and ARNS from s3 bucket properties sections.
              - Resource Object name: Any Object name
              - Resource ARN: Copy ARN from source bucket
              '''


        ''' ### Cloud watch log
      a. Service: Cloudwatch logs
        - create log group
        -create log stream 
        - PutLogEvents
      b. Resources:
        log-group: Any in this account.
        log-stream: Any in this account. 
         Policy name : eg. lambda-imgresizer-policy
         create policy> 
     '''

     ### Role
     '''Use case: Lambda
       ADD Permission and Policy: select the newly created policy ."""