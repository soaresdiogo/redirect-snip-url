# 🔗 RedirectSnipUrl
## 📝 Description
A serverless URL shortening application built with AWS Lambda, S3, and API Gateway. The system enables efficient and scalable creation and management of short URLs.

## 🚀 Technologies & Tools
- [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) - Programming Language
- [AWS Lambda](https://aws.amazon.com/lambda/) - Serverless Computing
- [Amazon S3](https://aws.amazon.com/s3/) - Storage
- [Amazon API Gateway](https://aws.amazon.com/api-gateway/) - API Management
- [Maven](https://maven.apache.org/) - Dependency Management
- [Lombok 1.18.24](https://projectlombok.org/) - Boilerplate Reduction
- [Jackson 2.13.1](https://github.com/FasterXML/jackson) - JSON Processing
- [AWS SDK for Java 2.x](https://aws.amazon.com/sdk-for-java/) - AWS SDK

## 🏗️ Project Structure
```
src/
└── main/
    └── java/
        └── dev/
            └── diogosoares/
                ├── Main.java      # 🎯 Main Lambda function
                └── UrlData.java   # 📦 Data model
```

## 📋 Prerequisites
- ☕ Java 17 JDK
- 📦 Maven
- 🔑 AWS Account with Lambda, S3, and API Gateway access
- 🛠️ AWS CLI configured

## 🚀 Getting Started

### 📥 Clone the Repository
```bash
git clone <repository-url>
cd RedirectSnipUrl
```

### 💻 Build Project
```bash
mvn clean package
```

## ☁️ AWS Configuration

### Lambda
1. Create a new Lambda function
2. Configure handler: `dev.diogosoares.Main::handleRequest`
3. Upload generated JAR file

### S3
1. Create a bucket to store URL data
2. Configure appropriate permissions

### API Gateway
1. Create a new REST API
2. Configure required endpoints
3. Integrate with Lambda function

## 📦 Main Dependencies
```xml
<dependencies>
    <dependency>
        <groupId>com.amazonaws</groupId>
        <artifactId>aws-lambda-java-core</artifactId>
        <version>1.2.1</version>
    </dependency>
    <dependency>
        <groupId>software.amazon.awssdk</groupId>
        <artifactId>s3</artifactId>
        <version>2.17.106</version>
    </dependency>
</dependencies>
```

## 🛠️ Features
- ✂️ URL Shortening
- 🔄 Automatic Redirection
- 📊 S3 Storage
- ⚡ Serverless Processing

## 🔐 Security
- 🔒 API Gateway Authentication
- 🛡️ Proper IAM Policies
- 🔑 S3 Access Control

## 📝 Logging and Monitoring
- 📊 Automatic CloudWatch Logs
- 📈 Lambda Metrics
- 🔍 API Gateway Tracing

## 🚀 Deploy
```bash
mvn clean package
aws lambda update-function-code \
    --function-name RedirectSnipUrl \
    --zip-file fileb://target/RedirectSnipUrl-1.0-SNAPSHOT.jar
```

Made with ❤️ by Diogo Soares
