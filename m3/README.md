### Basic Information 
* Provider used for this example is "AWS"
* Credentails - "aws_access_key" and "aws_secret_key" of the account under which we need to create instances
* Other following information
  * Region details
  * AMI details through datasource
  * Instance types 

### Prerequisities
* IDE - Visual Studio is preferred
  * Install plugin - "Hashicorp Terraform"
* Download and install terraform
* Check the version of terraform

```bash
terraform version
```

### Configuration files creation
* Create a ".tfvars" file that defines variables information
* Create a ".tf" file that defines IaaC code
  * Implementation of variables
  * Provider details with access details
  * Data - To pull data from the provider
    * Eg: AMI details
  * Resources - Eg: VPC, Security Groups with its vpc, ports and protocols and instance details
  * Details of what operations to be performed after creation of instance
    * Eg: version check, install some binaries
  * O/P details


### Commands
* This will give suggestions or help on commands
```bash
terraform
```

* To check version
```bash
terraform version
```

* To initialize the environment by getting provider. This also downloads (if not available in local) the provider plugin (say AWS here) by looking at the configuration file (.tf)
```
terraform init
```

* Terraform plan - It checks the configuration files at pwd along with .tfvars for variables. We also need to specify a file to store this plan, so that it can be reused
```bash
terraform plan -out <<PLAN_NAME>>.tfplan
Eg: terraform plan -out m3.tfplan
```

* Applying the plan - This actually create necessary resources defined in the plan.
  * Also stores current stage of configuration in "terraform.tfstate" file
```bash
terraform apply "<<PLAN_NAME>>.tfplan"
Eg: terraform apply "m3.tfplan"
```

* Destroying/Deleting the resources
```bash
terraform destroy
```
