# AWS Cli

For full documentation visit 

[AWS Cli](https://aws.amazon.com/cli/)


## Installation

    $ brew install awscli

## Commands

Run configuration for a given profile.

	$ aws configure
	$ aws configure --profile sathesh@sathesh

List all available profiles

	$ aws configure list-profiles

Set a default profile for all subsequent calls

	$ export AWS_PROFILE=sathesh@sathesh

Edit config and credentials

	$ nano ~/.aws/config
	$ nano ~/.aws/credentials

List all users in the account

	$ aws iam list-users
	$ aws iam list-users --profile sathesh@sathesh

Display configuration information, access_key and secret_key

	$ aws configure list

## S3 commands


List all S3 buckets

	$ aws s3 ls

One-way sync - This can be used to download all of your files.

	$ aws s3 sync s3://bucket_name .

Downloads all files from a particular S3 sub folder 
	
	$ aws s3 cp s3://bucket_name/resource_name local_folder_name --recursive



[BACK to TOC](./../README.md)

----------