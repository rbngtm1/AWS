#### CLOUDWATCH and SNS
  * Create a SNS topic and subscription
  * In cloudwatch, set alarm, select EC2, per instance metrics and in action, State is alarm, and send notification (with the name we created above). 
  * In EC2 action on buttom right, you can recover, stop, terminate, and reboot the instance.
  * You can create a rule in cloudwatch add source and target (you may choose sns, the topic that we created earlier)
#### Cloudwatch Logs
  * sudo yum update -y =>to pick up latest changes
  * sudo yum install -y awslogs  => install awslogs package
  
