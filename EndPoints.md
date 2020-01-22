## EndPoints 
* An endpoint network interface is then created in the selected subnet with a private IP address that serves as an entry point for traffic to the service. 
* You can associate a security group with your interface endpoint to restrict traffic to your endpoint network interface from resources in your Amazon VPC.

# concepts of end points

#### AWS Service Endpoints

To connect programmatically to an AWS service, you use an endpoint. An endpoint is the URL of the entry point for an AWS web service. The AWS SDKs and the AWS Command Line Interface (AWS CLI) automatically use the default endpoint for each service in an AWS Region. But you can specify an alternate endpoint for your API requests.

If a service supports Regions, the resources in each Region are independent of similar resources in other Regions. For example, you can create an Amazon EC2 instance or an Amazon SQS queue in one Region. When you do, the instance or queue is independent of instances or queues in all other Regions.

#### Regional Endpoints
Most Amazon Web Services offer a Regional endpoint that you can use to make your requests. The general syntax of a Regional endpoint is as follows.

```
protocol://service-code.region-code.amazonaws.com
```
Some services, such as IAM, do not support Regions. Thus, the endpoints for those services do not include a Region. Other services, such as Amazon EC2, support Regions but let you specify an endpoint that does not include a Region, such as https://ec2.amazonaws.com. When you use an endpoint with no Region, AWS routes the Amazon EC2 request to US East (N. Virginia) (us-east-1), which is the default Region for API calls.

#### FIPS Endpoints
 Federal Information Processing Standard 

    AWS works with customers to provide the information they need to manage compliance when using the AWS US East/West, AWS GovCloud (US), or AWS Canada (Central) Regions.

Some AWS services offer FIPS endpoints in selected Regions. Unlike standard AWS endpoints, FIPS endpoints use a TLS software library that complies with Federal Information Processing Standards (FIPS) standards. These endpoints might be required by enterprises that interact with the United States government.

To use FIPS endpoints in your requests, use the procedure in your AWS SDK for specifying a custom endpoint. For example, when using the AWS Command Line Interface, use the endpoint-url parameter. The following example uses the FIPS endpoint in the US West (Oregon) Region to create an AWS Key Management Service (AWS KMS) customer master key.
