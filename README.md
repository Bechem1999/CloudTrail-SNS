# CloudTrail+SNS
Root account monitoring with CloudTrail+SNS

OBJECTIVE: Simulate  sensitive activity from the AWS root account and detect it using logginh and alerts

TOOL NEEDED: CloudTrail, SNS(Simpl Notification Service), IAM,AWS CONSOLE

WHAT I DID
- log into AWS CONSOLE using root account( not recommended in production)
- Performed a sensitive action( disabled MFA, view billing dashboard)
- Enabled CloudTrail in my AWS account that log activities to my s3 bicket
- Set up an SNS topic and subscribe my email
- Created a cloudwatch event rule to detect RootAccount Usage and trigger the SNS alert
- Tested the setup by logging in again as root and checking that i have received a notification

WHAT I LEARNED

Through this project, I learned the following key concepts:

-Monitoring and Logging Root Account Activity: I gained hands-on experience with AWS CloudTrail to monitor and log sensitive root account activities. By using CloudTrail, I was able to track actions performed by the root user, ensuring accountability and traceability for any high-risk operations.

-Setting up CloudWatch Event Rules: I learned how to set up CloudWatch Event Rules to filter and detect specific activities, particularly those performed by the root account, and then trigger notifications for those events.

-Using SNS for Real-Time Alerts: I configured AWS Simple Notification Service (SNS) to receive real-time alerts whenever specific root account actions occurred, improving security awareness and proactive incident management.

-Best Practices for Root Account Security: The project reinforced the importance of minimizing the use of the root account and monitoring its activity closely. It also demonstrated how to use IAM roles and policies to restrict root access and protect sensitive resources.

-Hands-On Experience with AWS Security Tools: Overall, I strengthened my understanding of AWS's security features, including IAM, CloudTrail, CloudWatch, and SNS, and learned how to integrate them for comprehensive security monitoring in AWS environments. 
