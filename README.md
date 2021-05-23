# AWS Academy - AWS Solution Architect Associate

## CLI Demos

#### Upload to S3 via S3 Transfer Accelerate
1. Create file `time dd if=/dev/zero of=file.dat bs=1G seek=1 count=0`
2. Upload file `aws s3 cp file.dat s3://awsacademydemo/file.dat --region us-east-1 --endpoint-url http://s3-accelerate.amazonaws.com`
3. Check if transfer accelerate is enabled `aws s3api get-bucket-accelerate-configuration --bucket awsacademydemo --query 'Status'`

#### Duplicating CloudFormations & Yaml files to another AWS Region
`aws cloudformation create-stack --stack-name update-cafe-network --template-body file:///home/ec2-user/environment/CFTemplatesRepo/templates/cafe-network.yaml --region us-west-2`
