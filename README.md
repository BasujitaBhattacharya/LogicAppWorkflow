# LogicApp Standard Workflow
- Sample stateful workflow, triggered when messages are received on Dead Letter Queue of Azure Service Bus.
- This workflow has an action to send the messages from DLQ to Active queue using the SessionID, Content type and Content.
