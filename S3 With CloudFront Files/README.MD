# Instructions

- First Create the S3 Bucket With static web hosting enablement and upload the all the files (except policies folder)
- Then, Set the permission with the **policy 1** and try to access the S3 Bucket Url from Properties section
- Create a Route53 record (Along with AWS Certification Manager) and map S3 then try to access in HTTP mode see whether you are able to access using route53 Domain Name/DNS
- Do Not forget to buy the same domain in GoDaddy.com . if not then you cannot use the route53 domain over the internet
- Create a CloudFront along with WebAcl and GeoGraphic Location(with in CloudFront section) also include the HTTP to HTTPS redirection.So, that when user launch the Route53 domain name 
- Then map the CloudFront with Route53 Domain Name/DNS
- Try accessing the Route53 URL with/without HTTPS it should work
- Come back to S3 then replace the **Policy 1 with Policy 2** file from this folder and click save
- Edit the CloudFront distribution and select S3 again select OAC (Origin Access Control) and click save. 
  - Above, step is required to make sure nobody can launch the S3 Bucket URL directly without using the Route53 Domain URL
- In S3 Lifecycle Rules are automatically move to different storage options 
- S3 Replication does copy the data to different AZ's automatically (Require IAM role permission to achieve)
- S3 Access Points => To share the data between the teams where the folders with in a same bucket ( for ex: Bucket has Team1 & Team2 folder => Team2 cannot access Team1 folder and same for others so that its useful => **Yet to test**)


## CDN Finder
- After you completed the CloudFront it takes sometime so that you can view your website here : 
  - https://www.cdnplanet.com/tools/cdnfinder/