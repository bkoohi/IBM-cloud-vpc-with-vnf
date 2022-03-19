Follow these steps to setup your jump server or laptop with appropriate software and configurations for running terraforms to build your environment.
## 1. Setup IBM Cloud Account

IBM Cloud account is required. An Enterprise account is recommended but Pay as you Go account suffices to deploy secure landing zone cloud resources. 

If you do not already have an account, follow instructions [to create the account](https://cloud.ibm.com/docs/account?topic=account-account-getting-started#account-gs-createlite) and [upgrade to Pay-as-you-Go](https://cloud.ibm.com/docs/account?topic=account-account-getting-started#account-gs-upgrade)

- Have access to an [IBM Cloud account](https://cloud.ibm.com/docs/account?topic=account-account-getting-started). An Enterprise account is recommended but a Pay as you Go account should also work with this automation.
- Install the [IBM Cloud CLI](https://cloud.ibm.com/docs/cli?topic=cli-getting-started) and associated tooling.

1. Log into IBM Cloud [console](https://cloud.ibm.com) using the IBMid you used to setup the account. This IBMid user is the account __owner__ and has all the IAM accesses.

## 2 Setup CLI tools
Following CLI tools should be installed on your local machine for devtest and any validation work.
Detailed instructions are available [here](https://cloud.ibm.com/docs/cli?topic=cli-getting-started)

### 2.1. Install IBM Cloud CLI
Linux and MacOS
```bash
curl -sL https://raw.githubusercontent.com/IBM-Cloud/ibm-cloud-developer-tools/master/linux-installer/idt-installer | bash
```

Windows 10 Pro
```bash
[Net.ServicePointManager]::SecurityProtocol = "Tls12, Tls11, Tls, Ssl3"; iex(New-Object Net.WebClient).DownloadString('https://raw.githubusercontent.com/IBM-Cloud/ibm-cloud-developer-tools/master/windows-installer/idt-win-installer.ps1')
```

**Verify Installation**
```bash
ibmcloud version
```

### 2.2. Install Terraform v0.13.5
MacOS
```bash
sudo mkdir -p /usr/local/terraform/v0117
cd /usr/local/terraform/v0135 && sudo curl https://releases.hashicorp.com/terraform/0.13.5/terraform_1.1.7_darwin_amd64.zip --output tf12.zip
sudo unzip tf12.zip
sudo mv terraform /usr/local/bin/terraform0117
ln -s /usr/local/bin/terraform0117 /usr/local/bin/terraform
```

Linux
```bash
sudo mkdir -p /usr/local/terraform/v117
cd /usr/local/terraform/v117 && sudo curl https://releases.hashicorp.com/terraform/1.1.7/terraform_1.1.7_linux_amd64.zip --output tf117.zip
sudo unzip tf117.zip
sudo mv terraform /usr/local/bin/terraform0117
ln -s /usr/local/bin/terraform0117 /usr/local/bin/terraform
```

Windows
Download the CLI binary from https://releases.hashicorp.com/terraform/0.13.5/terraform_1.17_windows_amd64.zip and install on your Windows machine.

**Verify Installation**
```bash
terraform --version
```

### 2.3. Install jq
MacOS
```bash
brew install jq
```
Linux
```bash
apt install jq
```
Linux and Windows  
Find the jq binary matching your Linux/Windows OS and install with the respective install tool. Download [link here](https://stedolan.github.io/jq/download/).

**Verify Installation**
```bash
jq version
```
1. [Create an IBM Cloud API Key](https://cloud.ibm.com/docs/account?topic=account-userapikey#create_user_key). User owning this key should be part of __admins__ group.


## 3. Optional IBM Cloud Account setup

1. Log into IBM Cloud [console](https://cloud.ibm.com) using the IBMid you used to setup the account. This IBMid user is the account __owner__ and has all the IAM accesses.

2. [Complete the company profile and contacts information](https://cloud.ibm.com/docs/account?topic=account-contact-info) for the account. (best practice)

3. [Enable the flag](https://cloud.ibm.com/docs/account?topic=account-enabling-fs-validated) to designate your IBM Cloud account to be Financial Services Validated. (optional)

4. Enable VRF and Service Endpoints. This requires creating a support case. Follow [instructions](https://cloud.ibm.com/docs/account?topic=account-vrf-service-endpoint#vrf) carefully. (optional)

6.[Setup MFA for all IBM Cloud IAM users](https://cloud.ibm.com/docs/account?topic=account-account-getting-started#account-gs-mfa). (optional)

7. [Setup Cloud IAM Access Groups](https://cloud.ibm.com/docs/account?topic=account-account-getting-started#account-gs-accessgroups). User access to cloud resources will be controlled using the Access Policies assigned to Access Groups. IBM Cloud Financial Services profile requires that all IAM users do not get assigned any accesses directly to any cloud resources. When assigning Access policies, Click "All Identity Access Enabled Services" from drop down menu.

8.[Create an IBM Cloud Resource group](https://cloud.ibm.com/docs/account?topic=account-rgs) for the installation. (optional)
    - It can be a single group or (recommended) two groups as follows:
      - Management Resource Group
      - Workload Resource Group
      
9. [Add Resource Group access](https://cloud.ibm.com/docs/account?topic=account-groups) (optional)
   - It is recommended to have at least two access groups - one giving manager permissions to resources and one giving only viewer permissions.

10. Enable Activity Tracking with COS for IBM Cloud Services audit events. [See More Instructions to setup audit logging for IBM Cloud events here](https://test.cloud.ibm.com/docs/allowlist/framework-financial-services?topic=framework-financial-services-vpc-architecture-logging-audit). (optional)
