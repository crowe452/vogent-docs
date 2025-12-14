For Developers

Flow Builder Schemas



    * Quickstart





    * Agents

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Function Call](#function-call)
  * [Question](#question)
  * [Freeform](#freeform)



For Developers

# Flow Builder Schemas

The API allows you to describe flow nodes through the API. When creating/updating a versioned prompt, you want to specify an object that conforms to the appropriate schema in the `nodeData` field. If you want to use the output of a previous node in a future node, you can reference it by using double curly braces. For example, if you have a node with the ID `node_1` and you want to use the output of `node_1` in `node_2`, you can reference it as `{{node.node_1.output}}` in any string field. The notation to lookup any data is `{{node.node_id.field_name}}`.

### 

[​](#function-call)

Function Call

**Type:** `function_call` **Schema:**

Copy

```
`{ functionId: string, // The ID of the function to call within vogent inputs: { name: string, value: string }[], // The inputs to the function outputs: { type: "BOOLEAN" | "STRING" | "INTEGER" | "FLOAT" | "CUSTOM", name: string, nullable: bool, description: string, customFieldJsonSchema?: string, // If the type is CUSTOM, this is the JSON schema for the field }[] } `
```

### 

[​](#question)

Question

**Type:** `question` **Schema:**

Copy

```
`{ questionSchemaId?: string, question: string, questionType: "multiple_choice" | "multiple_select" | "freeform" | "numeric", options?: string[], clarificationDetails?: string, // Any clarification details that may be helpful to the model } `
```

### 

[​](#freeform)

Freeform

**Type:** `freeform` **Schema:**

Copy

```
`{ prompt: string // The prompt to feed to the model } `
```

[Dials Statuses](/developers/dial-statuses)