# snapshotalyzer-30000
Demo to manage AWS EC2 instance


## About

This project is a demo, and uses boto3 to manage
AWS EC2 instance snapshots.

## Configuring

shotty uses the configuration file created by the AWS cli, i.e.,

`aws configure --profile shotty`

## Running

`pipenv run "python shotty/shotty.py <command> <--project=PROJECT">`

*command* is instances, volumes, or snapshots
*subcommand* depends on command
*project* is optional

## Pre-requisities
1.  Create EC2 instances
    5 instances - t2.micros
    tag project: Valkyrie

2.  IAM
    Add user:  snapshotalyzer
    API only
    no permissions initially
    download access key and secret access key id
    == permissions
    add Permissions to user (not group)
      select the Policy named AmazonEC2FullAccess
      add permissions (take effect nearly immediately)

3.  aws configure --profile shotty
    needs access key and secret access key
    default region name - us-east-1
    output format (enter)

## Pipenv
1.  pipenv --three
2.  pipenv install boto3
3.  pipenv install -d ipython
