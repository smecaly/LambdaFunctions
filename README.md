# LambdaFunctions
This repo includes useful lambda functions in different scenarios

1. The auto-update-ec2-ebs.py will automatically update resources (ebs, ec2) based on the event created in cloudwatch. The cloudwatch even rule is: 

{
  "detail-type": [
    "AWS API Call via CloudTrail"
  ],
  "detail": {
    "eventSource": [
      "ec2.amazonaws.com",
      "rds.amazonaws.com"
    ],
    "eventName": [
      "RunInstances",
      "CreateVolume",
      "CreateDBInstance"
    ]
  }
}

2. The AutomateMandatoryTag.py will be manually invoked and will tag resources that are missing tags.



