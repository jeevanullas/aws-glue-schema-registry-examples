## Evolve JSON Schemas in Amazon MSK and Amazon Kinesis Data Streams with the AWS Glue Schema Registry

This repository is a companion to the AWS Big Data Blog, located markdown url [here](https://aws.amazon.com/blogs/big-data/).

## Description

This repository contains the CloudFormation template and code corresponding to the following illustration.

![Illustration](illustration.jpg)

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## Setup Instructions

Step 1. git clone 
Step 2. mvn clean package
Step 3. Specify bootstrap.servers with IAM auth in config.properties
Step 4. Setup MSK cluster with Kafka 2.7.1 and IAM auth
Step 5. Use template.json to create a CFN stack in ap-southeast-2
Step 6. Run the producer using the following command
mvn exec:java -Dexec.mainClass="com.amazonaws.services.gsr.samples.json.kafka.RunKafkaProducer" -Dexec.args="config.properties friends"
Step 7. Run the consumer using the following command
mvn exec:java -Dexec.mainClass="com.amazonaws.services.gsr.samples.json.kafka.RunKafkaConsumer" -Dexec.args="config.properties friends"

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

