## chat_menmory_by_Mongo

**Author:** ssssshql
**Version:** 0.0.1
**Type:** tool

### Description
A Dify plugin to Record chat history

### Require

You need a MongoDB

### Tools

### Retrieve Messages:

#### 1. `conversation_id`
- **Type**: `string`
- **Required**: `true`
- **Description**:  
  The unique identifier of the conversation where the message will be stored. This ensures the message is correctly associated with the right conversation thread.

#### 2. `user_id`
- **Type**: `string`
- **Required**: `true`
- **Description**:  
  The unique identifier of the user sending/storing the message. This associates the message with the correct user account.

#### 3. `max_count`
- **Type**: `number`
- **Required**: `false` (optional)
- **Default**: `50`
- **Description**:  
  The maximum number of messages to retrieve. Limits the response size when querying messages.

### Store Message

#### 1. `user_id`
- **Type**: `string`
- **Required**: `true`
- **Description**:  
  The unique identifier of the user sending/storing the message. This associates the message with the correct user account.

#### 2. `role`
- **Type**: `select`
- **Required**: `true`
- **Description**:  
  The sender's role in the message exchange. Valid options are `user` (human) or `assistant` (AI).
- **Options**:
  - `user`: Human user
  - `assistant`: AI/bot response
- **Placeholder**: `Please select a role`

#### 3. `text`
- **Type**: `string`
- **Required**: `true`
- **Description**:  
  The actual text content of the message to be stored.

#### 4. `conversation_id`
- **Type**: `string`
- **Required**: `true`
- **Description**:  
  The unique identifier of the conversation thread where this message belongs.

### Delete Message:

#### 1. `conversation_id`
- **Type**: `string`
- **Required**: `true`
- **Description**:  
  The unique identifier of the conversation thread where this message belongs.


### Github
[https://github.com/ssssshql/dify-plugin-chat-memory-by-Mongo](https://github.com/ssssshql/dify-plugin-chat-memory-by-mongo)
