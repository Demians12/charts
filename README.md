# CHART

This repository provides a Crossplane configuration for deploying a pre-configured Amazon DynamoDB table. The purpose of the repository is to allow users to quickly and easily deploy this DynamoDB table to their AWS account.

## Features

- Amazon DynamoDB table configured with the following attributes: 
    - `UserId` of type String
    - `GameTitle` of type String
    - `TopScore` of type Number
- The table operates in `PROVISIONED` billing mode.
- Global Secondary Index on `GameTitle` with `TopScore` as range key.
- Tagged with `Environment: production` and `Name: dynamodb-table-1`.
- Provisioned Read and Write capacity of 20 units.

## Usage

To deploy this DynamoDB table to your AWS account, you'll need to have Crossplane installed and configured with your AWS credentials. Then, you can apply the configuration in this repository with the command:

```bash
kubectl apply -f <configuration-file.yaml>
```
