# EC2_ansible
Write ansible playbook that creates EC2 instance

Roles
- create_ec2
Create ec2 instance using the boto module using parameters
  1. Key_name : Name of your keypair (aws privite key)
  2. group : Security group for your VPC
  3. instance_type : example t2-micro,etc 
  4. image : Use AMI for this 
  5. region : What region are you using for your deployment of the ec2 instances
  6. vpc_subnet_id : What subnet are you using in VPC
  7. assign_public_ip : Automatically gives the instance an public IP address

- start_ec2_instance
starts/stops/restarts existing ec2 instance
  1. region : What region are you using for your deployment of the ec2 instances
  2. instance_tags : Name you assigned to the instance (customized)
  3. vpc_subnet_id : What subnet are you using in VPC
  4. assign_public_ip : Automatically gives the instance an public IP address
  5. start : If state_of_instance is ;
        running = start instance
        absent = terminate instance
        stopped = Stopping running instance
        restarted = Restarting instance