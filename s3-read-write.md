Policy para bucket s3 - permissão de Leitura e Escrita de Objetos:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [ "s3:ListBucket"],
            "Resource" : [ "arn:aws:s3:::<Nome-do-Bucket>" ]
        },
        {
            "Effect": "Allow",
            "Action": [
                "s3:Get*",
                "s3:List*",
                "s3:DeleteObject",
                "s3:PutObject",
                "s3:PutObjectAcl"
            ],
            "Resource": "arn:aws:s3:::<Nome-do-Bucket>/*"
        }
    ]
}
```