# DFS


#### 1、[Terraform](https://www.terraform.io/) Usage

This part mainly introduce how to use `Alicloud provider terraform`  [alicloud terraform](https://registry.terraform.io/providers/aliyun/alicloud/latest/docs) to manage your infrastructure resource.

+ install terraform
```commandline
brew install terraform
```

+ setup Ali access_key and access_secret [Obtain an AccessKey pair](https://www.alibabacloud.com/help/en/basics-for-beginners/latest/obtain-an-accesskey-pair)

+ setup Alicloud provider
```commandline
provider "alicloud" {
  access_key = "${var.access_key}"
  secret_key = "${var.secret_key}"
  region     = "${var.region}"
}

/or config it as your environment variables

$ export ALICLOUD_ACCESS_KEY = "anaccesskey"
$ export ALICLOUD_SECRET_KEY = "asecretkey"
$ export ALICLOUD_REGION     = "cn-shanghai"
```

+ Apply your terraform script
```commandline
terraform init  # prepare your working directory for other commands
terraform plan  # show changes required by the current configuration
terraform apply # create or update infrastructure
```
