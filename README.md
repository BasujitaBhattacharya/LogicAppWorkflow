# LogicApp Standard Workflow


- Sample [stateful-workflow](ExampleWorkflow/flowDeadLetterQueue.json) triggered when messages are received on Dead Letter Queue of Azure Service Bus.
- This workflow has an action to send the messages from DLQ to Active queue using the SessionID, Content type and Content after a configurable delay of 3 mins.
- It follows this documentation https://learn.microsoft.com/en-us/azure/connectors/connectors-create-api-servicebus?tabs=consumption

# LogicApp Standard Workflow Designer View


- Service Bus "When a message is received in a queue" Built-in App Trigger Settings
  <img width="934" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/e0c5aad5-d4cf-4487-8336-a156b14457c3">

- Delay Action
  <img width="922" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/91f137ef-dafd-4291-8bff-d4abc9c46257">
    
- Send Message to Queue Action Settings
 <img width="932" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/41ffbb2b-8c8e-4451-b077-7744125be054">


- Service Bus SAS Token settings 
  <img width="920" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/8e7b75e1-6f5c-4cb8-bb38-02cf3c28f5e7">


- Logic App API Connection setting - Using the Primary/Seconday Connection token of Service bus queue above
  <img width="926" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/13cc214a-e89d-46df-9bf2-dbf406c95fe8">




