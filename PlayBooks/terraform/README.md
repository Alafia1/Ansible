# Terraform Installation Playbook

### This playbook was created using ChatGPT and below is its explaination

- This playbook assumes that you have specified the version of Terraform you want to install in the variable terraform_version. You can update the playbook to use a different version as needed.

- Note: This is just an example and may not cover all the steps required for setting up Terraform in a production environment. You should modify this playbook as per your specific requirements and best practices.

### Adjustments Made

- hard code the variable 'terraform version' to 1.4.0-alpha20221207
- added unzip installation, because the package needs to be unzipped and if you are using a newly provisioned server without unzip package, it is required to complete the installation