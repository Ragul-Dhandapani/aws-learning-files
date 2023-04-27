$env:AWS_ACCESS_KEY_ID=""
$env:AWS_SECRET_ACCESS_KEY=""
$env:AWS_DEFAULT_REGION="us-east-1"

Paste all the above commands in Terminal with Access Key and secret
Then terraform init => terraform validate => terraform plan => terraform apply --auto-approve