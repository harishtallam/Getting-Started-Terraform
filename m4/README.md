## Continuation to m3 example
### First Run
* In "m3" example, we have used default vpc as a resournce
* In this example, we will be using customized vpc with its depenencies
  * network_address_space
  * subnet1_address_space
  * We would need get the "list of availability zones" as a "data" to provision vpc
  * Other networking resources
    * vpc
    * internet gateway
    * subnet with cidr, vpc_id, availability zone
    * route table
    * route table association
    * security groups
    
* Now, refer to "m4_commands.txt" and execute to provision the changes
    

### Seconds Run
* In this example, we will be adding one more "EC2" instance and a "Load Balancer"
* Map new "EC2" instance with previously shared network/security group
* Add these 2 "EC2" instances to the "Load Balancer

* Refer "modulefour-update.tf.rename" for this
* Rename earlier tf file "modulefour-start.tf" to "modulefour-start.tf.rename", so that terraform does not consider this will generation/creation of plan
* Rename tf file "modulefour-update.tf.rename" to "modulefour-update.tf" for considering plan generation/creation
* We need to required to run "terraform init" as it was already initiazlied in the first run
* Now, overwrite the existing plan with the new one with "terraform plan -out m4.tfplan"
  * It will determine what changes it needed to make inorder to match the configuration
  
