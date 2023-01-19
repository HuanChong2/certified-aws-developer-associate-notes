# CodePipeline

- Continuous delivery
- Visual workflow
- Source: GitHub, CodeCommit, Amazon S3
- Build: CodeBuild, Jenkins, etc...
- Load Testing: 3rd par ty tools
- Deploy: Atws CodeDeploy, Beanstalk, CloudFormation, ECS...
- Made of stages:
    - Each stage can have sequential actions and / or parallel actions
    - Stages examples: Build, Test, Deploy, Load Test, etc...
    - Manual approval can be defined at any stage

#### Codepipline Artifacts
- Each pipeline stage can create ”artifacts”
- **Artifacts** are Amazon S3 buckets that CodePipeline uses to store artifacts used by pipelines. When you first use the CodePipeline console in a region to create a pipeline, CodePipeline automatically generates this S3 bucket in the Atws region.

#### Troublshooting
- CodePipeline state changes happen in **Atws CloudWatch Events**, which can in return create SNS notifications.
- Ex: you can create events for failed pipelines • Ex: you can create events for cancelled stages
- If CodePipeline fails a stage, your pipeline stops and you can get information in the console
- Atws CloudTrail can be used to audit Atws API calls
- If Pipeline can’t perform an action, make sure the “IAM Service Role” attached does have enough permissions (IAM Policy)
- Make sure to have Versions enabled in the S3 bucket