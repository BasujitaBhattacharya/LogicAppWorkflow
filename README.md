# LogicApp Standard Workflow


- Sample [stateful-workflow](src/logicApp/Flow-DLQ-Message-Retrieval/workflow.json) triggered when messages are received on Dead Letter Queue of Azure Service Bus.
- This workflow has an action to send the messages from DLQ to Active queue using the SessionID, Content type and Content after a configurable delay of 3 mins.
- It follows this documentation https://learn.microsoft.com/en-us/azure/connectors/connectors-create-api-servicebus?tabs=consumption
- It also has VNET Integration enabled to connect to Service Bus over Private Endpoint

# LogicApp Standard Workflow Designer View

## Service Bus "When a message is received in a queue" Built-in App Trigger Settings
  <img width="934" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/e0c5aad5-d4cf-4487-8336-a156b14457c3">


## Delay Action
  <img width="922" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/91f137ef-dafd-4291-8bff-d4abc9c46257">

    
## Send Message to Queue Action Settings
 <img width="932" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/41ffbb2b-8c8e-4451-b077-7744125be054">


## Service Bus SAS Token settings 
  ![image](https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/c00fb466-d0aa-4f7a-bb65-2fc8a68252f6)


## Logic App Service Provider Connection setting - Using the Primary/Seconday SAS token of Service bus above
  ![image](https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/e0ad3fed-e193-41f5-8d43-136cd4370e1b)


## **Azure Pipelines**
The .pipelines folder contains examples of how to deploy a workflow for the logic app.

### CI Pipeline
Build code and creates a zip of the project
Swaps out parameter files configured specifically for the azure environment
Publishes project zip as pipeline artifact

### CD Pipeline
Downloads CI pipeline artifact containing project zip
Use the Azure Functions task to deploy the project

### Pipeline Variables
For both the classic and container deployment approach, you will need to supply a set of variables to make the deployments possible.

Variable Files
Under the variables/ folder & in some pipeline files, you will need to fill in some variables.

NOTE: You can search for TODO to find all the values you need to replace.

You will need need to create a service connection for your Azure subscription for many of the pipeline tasks to work. Follow this documentation to create your service connection.



