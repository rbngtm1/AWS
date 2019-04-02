#### CLOUDWATCH and SNS
  * Create a SNS topic and subscription
  * In cloudwatch, set alarm, select EC2, per instance metrics and in action, State is alarm, and send notification (with the name we created above). 
  * In EC2 action on buttom right, you can recover, stop, terminate, and reboot the instance.
  * You can create a rule in cloudwatch add source and target (you may choose sns, the topic that we created earlier)
#### Cloudwatch Logs
  * sudo yum update -y =>to pick up latest changes
  * sudo yum install -y awslogs  => install awslogs package
https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/QuickStartEC2Instance.html ==> visit this website for detail
To run it directly from the internet, use the following commands and follow the prompts:

curl https://s3.amazonaws.com/aws-cloudwatch/downloads/latest/awslogs-agent-setup.py -O
sudo python ./awslogs-agent-setup.py --region us-east-1
If the preceding command does not work, try the following:

sudo python3 ./awslogs-agent-setup.py --region us-east-1
To download and run it standalone, use the following commands and follow the prompts:

curl https://s3.amazonaws.com/aws-cloudwatch/downloads/latest/awslogs-agent-setup.py -O
curl https://s3.amazonaws.com/aws-cloudwatch/downloads/latest/AgentDependencies.tar.gz -O
tar xvf AgentDependencies.tar.gz -C /tmp/
sudo python ./awslogs-agent-setup.py --region us-east-1 --dependency-path /tmp/AgentDependencies
#### Instead of giving access key and secret key follow below steps:
  * Create a role with cloudwatch logs
  * Assign the role to ec2 machine , go to action, instance settings and attach/replace IAM role and assigh role that you created
  * now go to cloudwatch and logs, you can see logs
