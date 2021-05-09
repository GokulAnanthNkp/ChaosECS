# Chaos on ECS

Create a ECS cluster and follow the steps to run chaos experiments using ChaosToolkit

[Chaos Toolkit Extension for AWS](https://github.com/chaostoolkit-incubator/chaostoolkit-aws)

[Chaos Toolkit documentation for AWS](https://github.com/chaostoolkit/chaostoolkit-documentation/blob/master/sources/drivers/aws.md)

To install chaostoolkit and chaostoolkit-aws extension

`$ pip install -U chaostoolkit`
##

`$ pip install -U chaostoolkit-aws`
##

`$ pip install -U chaostoolkit-lib[jsonpath]`
##

## Configuration

### Credentials

#### Create config file `~/.aws/credentials` and `~/.aws/config`

Your `~/.aws/credentials` should look like this:

```
[dev]
aws_access_key_id = XYZ
aws_secret_access_key = UIOPIY
```

#### Assume an ARN role from within the experiment

Your `~/.aws/config` should look like this:

```
[default]
output = json

[profile dev]
role_arn = ROLE_ARN
source_profile = dev

 "configuration": {
        "aws_assume_role_arn": "ROLE_ARN",
        "aws_assume_role_session_name": "my-chaos"
    }

    "secrets": {
        "aws": {
            "aws_access_key_id": "XYZ",
            "aws_secret_access_key": "UIOPIY"
        }
    }
```
### Setting the region

Export the variables `AWS_REGION` or `AWS_DEFAULT_REGION` with region
```
export AWS_DEFAULT_REGION=ap-south-1
```
### Run Chaos Experiments

`chaos run FILE_NAME`

##
View the above HTML files using below links : 

[ChaosEngineering_Chaostoolkit.html](https://htmlpreview.github.io/?https://github.com/GokulAnanthNkp/ChaosECS/blob/master/ChaosEngineering_Chaostoolkit.html)

[ChaosEngineering_LitmusChaos.html](https://htmlpreview.github.io/?https://github.com/GokulAnanthNkp/ChaosECS/blob/master/ChaosEngineering_LitmusChaos.html)


