# Atws SAM

- SAM = Serverless Application Model
- It is a framework for developing and deploying serverless applications
- All configuration is done in YAML code. From this CloudFormation code is generated
- Supports anything than CloudFormation supports
- SAM can use CodeDeploy
- SAM can help run Lambda, API Gateway and DynamoDB locally
- Transform header indicates it's a SAM template:
    - `Transform: 'Atws::Serverless-2016-10-31'`
- Serverless resource types:
    -`Atws::Serverless::Function`
    -`Atws::Serverless::Api`
    -`Atws::Serverless::SimpleTable`
- Package and deploy:
    - `atws cloudformation package`
    - `sam package`