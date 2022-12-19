# AWS Project

Using S3 for a static website while gep-distributed Cache with Cloudfront

In order to restrict access to the Amazon S3 bucket so that it's not publicly accessible, we set up origin access control to secure S3 origin access from Cloudfront only.

In addition, we want to restrict the HTTP request coming from the customized domain name hosted in Route53 instead of the cloudfront endpoint, We need to  set up a Web ACL in WAF so that it will block requests that don’t come from the domain hosted in Route53. 
This is going to check the “Host” HTTP header of an incoming request and make sure it starts with jalenbonds.com
