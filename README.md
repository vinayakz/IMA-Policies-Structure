# IMA-Policies-Structure

```sh
{
    "version": "2012-10-17",
    "ID": "S3-Account-Permission",
    "Statement":[
        {
            "Sid": "1",
            "Effect": "Allow",
            "Principal": {
                "AWS": ["arn:aws:iam::123456789012:root"]
            },
            "Action":[
                "s3:GetObject",
                "s3:PutObject"
            ],
            "Resource": ["arn:aws:s3:::mybucket/*"]
        }
    ]
}
```

Consists of

. Version: policy language version, always include "2012-10-17"

. Id: an identifier for the policy (optional)

. Statement: one or more individual statement (required)



Statements consist of

. Sid: and identifier for the statement (optional)

. Effect: whether the statement allows or denies access (Allows, Deny)

. Principal: account/user/role to which this policy applied to

. Action: list of actions this policy allows or denies

. Resource: list of resources to which the actions applied to

. Condition: Condition for when this policy is in effect (optional)
