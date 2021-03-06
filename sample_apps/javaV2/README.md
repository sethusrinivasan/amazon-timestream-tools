# TimestreamCustomerSampleJavaV2

Sample Java application for AWS SDK V2

----
## How to use it

Ensure your Java SDK and runtime are 1.8 or higher.

1. Install maven: https://maven.apache.org/install.html

1. Go to Timestream Java V2 sample app directory

1. You can compile and run your source code with the below command:
    ```shell
   mvn clean compile
   mvn exec:java -Dexec.mainClass="com.amazonaws.services.timestream.Main"
    ``` 
   NOTE: You might need to change the version of timestreamwrite and timestreamquery dependencies in `pom.xml` file based on the version of SDK jar you are using.
   
1. To run with sample application and ingest data from sample csv data file, you can use the following command: 
   ```shell
   mvn clean compile
   mvn exec:java -Dexec.mainClass="com.amazonaws.services.timestream.Main" -Dexec.args="--inputFile ../data/sample.csv"
   ```

1. To run with sample application and include database CMK update to a kms "valid-kms-id" registered in your account run  
   ```shell
   mvn clean compile
   mvn exec:java -Dexec.mainClass="com.amazonaws.services.timestream.Main" -Dexec.args="--kmsId valid-kms-id"
   ``` 

