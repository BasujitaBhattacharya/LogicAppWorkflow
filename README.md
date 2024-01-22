# LogicApp Standard Workflow
- Sample stateful workflow, triggered when messages are received on Dead Letter Queue of Azure Service Bus.
- This workflow has an action to send the messages from DLQ to Active queue using the SessionID, Content type and Content.

# LogicApp Standard Workflow Designer View
- Service Bus When a message is received in a queue (auto-complete) Built-in Trigger Settings
  <img width="939" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/c0523637-0cc4-4a1b-ac0a-1cad7df4dbe7">
  
- Send Message to Queue Action Settings
  <img width="931" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/664973dc-7bae-4083-bdf8-6107a85f336d">

- Service Bus SAS Token settings 
  <img width="920" alt="image" src="https://github.com/BasujitaBhattacharya/LogicAppWorkflow/assets/121059306/8e7b75e1-6f5c-4cb8-bb38-02cf3c28f5e7">



