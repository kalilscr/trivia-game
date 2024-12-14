## **AWS Step Functions workflow orchestration**

Because you work in software, you’ll regularly build code that models a workflow in your organization. Sometimes, you’ll model a real-world workflow, such as the steps that are needed to complete an online order. Other times, you’ll model a technical workflow, such as the steps that follow after a user uploads a new profile picture to a social media site.

AWS Step Functions is a service you can use to build and visualize the workflows in your applications. Instead of writing the code to coordinate the components of a distributed applications, you can build a visual workflow that performs the coordination. With AWS Step Functions, you design your workflow as a state machine. State machines are defined with Amazon States Language in a JSON format.

A state machine contains multiple states. Here’s a review of the different states:

* **Task:** Performs some work (for example a Lambda function). You can use optimized integrations for services such as AWS Lambda, Amazon DynamoDB, Amazon Simple Notification Service (Amazon SNS), Amazon Simple Queue Service (Amazon SQS), and more. AWS SDK service integrations are available for over 200 services.  
* **Choice:** Makes a decision for the next branch of execution.  
* **Succeed** or **Fail:** Ends the execution.  
* **Pass:** Passes input to output. This state is convenient for debugging your state machine by hardcoding or overriding values.  
* **Parallel:** Creates multiple branches of execution.  
* **Map:** Runs tasks in parallel on the items in a dataset. The Map state has two modes: inline mode and distributed mode. In inline mode, you work with a JSON array from a previous step in the workflow. In distributed mode, you can work with a larger dataset, such as a JSON file or a comma-separated values (CSV) file from an Amazon Simple Storage Service (Amazon S3) bucket.

By using these states, you can create a graph of steps that will be traversed while a state machine execution runs.

