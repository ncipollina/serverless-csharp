# serverless-csharp
This repository contains the source code for my video on getting started with the Serverless Framework and C#.

## Project Structure

This starter project consists of:
* Function.cs - class file containing the C# method mapped to the single function declared in the template file
* serverless.yml - configuration file containing the definition of the Lambda function and all associated resources


The generated project contains a Serverless template declaration for a single AWS Lambda function that will be exposed through Amazon API Gateway as a HTTP *Get* operation. 

## Here are some steps to follow to get started from the command line:

Once you have edited your template and code you can package your application using the [Amazon.Lambda.Tools Global Tool](https://github.com/aws/aws-extensions-for-dotnet-cli#aws-lambda-amazonlambdatools) from the command line.

Install Amazon.Lambda.Tools Global Tools if not already installed.
```
    dotnet tool install -g Amazon.Lambda.Tools
```

If already installed check if new version is available.
```
    dotnet tool update -g Amazon.Lambda.Tools
```

Execute unit tests
```
    cd "serverless-csharp/test/ServerlessCSharp.Tests"
    dotnet test
```

Package application
```
    cd "serverless-csharp/src/ServerlessCSharp"
    dotnet lambda deploy-serverless
```

Install the Serverless Framework

```
    npm install -g serverless
```

If already installed, update to new versions.

```
    npm update -g serverless
```

To deploy your application, first ensure your aws credentials are set.

```
    $env:AWS_ACCESS_KEY_ID="<<Your Access Key>>"
    $env:AWS_SECRET_ACCESS_KEY="<<Your Secret Access Key>>"
```

To deploy
```
    cd "serverless-csharp/src/ServerlessCSharp
    serverless deploy
```