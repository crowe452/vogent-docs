Model

Flow Builder



    * Quickstart





    * Agents

        * Configuration

    * Model

                            * Post-Call Analysis

  * Voices

  * Tools

            



    * Importing via SIP

  



      



  * Webhooks

      



  * [Building an Agent with Flow Builder](#building-an-agent-with-flow-builder)
  * [Understanding the Flow Builder](#understanding-the-flow-builder)
  * [Adding Nodes](#adding-nodes)
  * [Question Nodes](#question-nodes)
  * [Freeform Nodes](#freeform-nodes)
  * [Function Call Nodes](#function-call-nodes)
  * [Connecting Nodes](#connecting-nodes)



Model

# Flow Builder

Build more structured agents with explicit conditional logic

Flow Builder enables you to create agents with structured conversation paths and explicit decision points. More specifically, the Flow Builder allows you to delineate lists of questions, along with branching logic that determines which questions are asked next. Each agent created this way intelligently navigates through questions, probing for additional information until it receives a satisfactory answer before moving to the appropriate next step based on that response. Under the hood, the Flow Builder comprises two models: one that maintains context for the current question, and another that interprets the user’s response to determine what context to pass to the first model for the next step.

## 

[​](#building-an-agent-with-flow-builder)

Building an Agent with Flow Builder

To access the Flow Builder, go to the **Agents** tab and select an agent (or create a new one). Then, navigate to the agent’s **Model** tab, select _Elto Survey New_ under _Model_ and _Flow_ under _Agent Type_. The prompting interface should then be replaced by a visual flow builder.

### 

[​](#understanding-the-flow-builder)

Understanding the Flow Builder

The Flow Builder is a collection of nodes and edges (a directed graph). Each node is a question, and each edge is a conditional branch. At any point in the conversation, the agent will be in one of the nodes. The survey model will be given the context of the current node, as well as relevant information from past nodes, to carry out the conversation and gather the information necessary to move on from the current node. Once the information is gathered, a separate model will interpret the user’s response and the possible subsequent nodes to determine which node to transition to next.

### 

[​](#adding-nodes)

Adding Nodes

The conversation begins with the node connected to the **Start** node. To add a node to the conversation, click on the **Edit** button on the bottom left of the Flow Builder interface. Once the UI has expanded, click on the **New Node** button. There are three node types: questions, freeform conversations, and function calls.

#### 

[​](#question-nodes)

Question Nodes

In a question node, the agent will ask the user a question and continue the conversation to get a desired response. Enter your question in the **Question** field, and select an expected response type from the **Answer Type** dropdown.

The possible answers that you designate in the _Multiple Select_ or _Multiple Choice_ answer types are used by the model, along with the conversation history, to determine which node to transition to next. As a result, the user’s response does not have to verbatim match an answer for the agent interpret it as a correct response.

#### 

[​](#freeform-nodes)

Freeform Nodes

In a freeform node, the agent will converse with the respondent based on a set of instructions. The agent progresses from the freeform node based on conditions outlined in the Freeform Node’s prompt. You can also use Freeform nodes as terminal nodes, which can be useful if you want to end the conversation with further instructions or pleasantries for the respondent.

Make sure that there’s a clear path to the next node from the Freeform Node’s prompt; otherwise, your agent may get stuck.

#### 

[​](#function-call-nodes)

Function Call Nodes

In a function call node, the agent will call an external function to get a response, which it can then use in future nodes. For more information on function-calling in Vogent, see the [Function Calling](/platform-overview/agents/model/function-calling) guide.

For any node, you can reference past nodes by using `@` to insert a variable.

### 

[​](#connecting-nodes)

Connecting Nodes

To connect two nodes, click on the white node at the bottom of the node from which you want to branch, and drag an edge to the node to which you want to connect. The behavior of every node transition edge is determined by 3 fields: **Order** , **Variable** , and **Condition Type**.

  * **Order** : The order of the node transition edge determines the order in which the agent will consider the node transition edges.
  * **Variable** : The variable (output from a past node) that the agent will use to determine which node transition edge to take.
  * **Condition Type** : The condition type determines how the agent will interpret the variable to determine which node transition edge to take.

The possible condition types are:

  * _Always_ : This edge will always be taken when considered.
  * _Equal_ : This edge will be taken when the output from the variable is equal to the value specified in the _Condition Value_ field, as determined by the model that interprets the user’s response (i.e. the user’s response does not have to verbatim match the value specified in the **Condition Value** field).
  * _In_ : This edge will be taken when the output from the variable is in the list of values specified in the _Condition Value_ field.



[Prompted Models](/platform-overview/agents/model/prompted-models)[Fine Tuning](/platform-overview/agents/model/fine-tuning)