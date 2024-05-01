<h1>Evaluate AWS Config Rules</h1>

<h2>Description</h2>
I evaluated resources in the environment by using AWS managed rules and the AWS Config service. First, I enabled the AWS Config service, and then created a new Amazon Simple Storage Service (Amazon S3) bucket. I reviewed the AWS Config resources, before enabling AWS managed rules to evaluate your resources. <br/>

<h2>Services and Resources Used</h2>

- <b>AWS Config</b>
- <b>AWS managed rules</b>
- <b>Amazon Simple Notification Service (SNS)</b>

<h2>Project Stages:</h2>

<p align="center">
Used AWS Config to create service-linked role:  <br/>
<img src="https://imgur.com/uybM4Af.png" height="80%" width="80%" alt="aws config"/>
<br />
<p align ="left">AWS Config is an AWS managed service that can record configuration information for your AWS resources. You can configure the service to take a snapshot that will create a point-in-time view of your AWS resources. You can also use AWS Config to automatically evaluate your resources by using rules to see if the resources are compliant with your desired settings.<br/>
<br />
The AWS Config service can automatically notify you if a resource change (for example, an addition, modification, or deletion) has taken place.</p> <br />
<p align="center">
AWS Config needs an S3 bucket to store the configuration items that it records, so I created an S3 bucket:  <br/>
<img src="https://imgur.com/W8VbGIJ.png" height="80%" width="80%" alt="aws config"/>
<br />
<br />
Add the desired-instance-type AWS Config managed rule, and then configure the instanceType parameter by using a value of t2.micro: <br/>
<img src="https://imgur.com/A43xHfZ.png" height="80%" width="80%" alt="aws congif"/>
<br />
<br />
I verified that the compliance status was ‘Compliant’:  <br/>
<img src="https://imgur.com/5QRB4Hy.png" height="80%" width="80%" alt="aws config"/>
<br />
<br />
Then I added the s3-bucket-server-side-encryption-enabled rule and checked for compliance: <br/>
<img src="https://imgur.com/BJKZLB7.png" height="80%" width="80%" alt="aws config"/>
</p>
