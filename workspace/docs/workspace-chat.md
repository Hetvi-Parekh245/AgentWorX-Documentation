# Navigating Workspace Chat

Workspace Chat is where you actually interact with your workspace — asking questions, uploading documents on the fly, referencing your documents, and getting answers from the agents attached to that workspace. You can also switch AI models mid-conversation without losing your thread's context.

![Workspace chat view](./assets/workspace-chat-launched.png)

## Short Description

Once you click **Launch** on a workspace, you land in its chat view. Each workspace can hold multiple **threads** (separate conversations), and every thread runs against the agent(s) configured for that workspace.

## When to Use It

Use Workspace Chat whenever you need to:

- Ask questions about documents stored in the workspace
- Get help from an AI agent scoped to a specific business context (e.g. "CompanyResearchAgent" inside a "CompanyResearchWorkspace")
- Upload a document and immediately start asking questions about it
- Keep separate conversations organized as distinct threads, rather than one long chat

## Configuration Options

| Element | What it does |
|---|---|
| **New Thread** | Starts a fresh, separate conversation within the workspace |
| **Thread list** | Lets you switch between past conversations (the default thread is named **Default**) |
| **Agent selector** (bottom of chat box) | Choose which attached agent should respond in this thread, if more than one is available |
| **Upload a document** link | Add a file directly from the chat screen without leaving the conversation |
| **Attachment / code / text icons** | Attach files, code snippets, or formatted text to your message |
| **Voice input (mic icon)** | Send a message using speech instead of typing — available if Speech-to-Text was configured for the workspace |

## Switching Models Mid-Conversation

The agent/model selector at the bottom of the chat box isn't fixed for the whole thread — you can change it partway through a conversation if you want a different agent or underlying model to handle the next message. Earlier messages in the thread stay visible, so the new model still has the conversation's context.

## Slash Commands

Typing `/` inside the chat box lets you invoke specific agent skills directly, instead of phrasing a full question. This gives you a quicker, more predictable way to trigger an agent's built-in capabilities.

The exact commands available depend on which agent is selected and what skills it has been configured with — type `/` in the chat box to see the list of commands available for the current agent.

## Expected Outputs

- A conversational response from the selected agent, grounded in the documents and configuration of that workspace
- If no documents have been uploaded yet, the workspace prompts you to **upload a document** or **send a chat** to get started
- Each message you send is saved to the active thread, so you can revisit the conversation later

## Edge Cases and Limits

- Every workspace must have at least one agent attached at creation, so this shouldn't come up for a normally-created workspace. However, if all attached agents are later removed via **Workspace Settings → Agents & workflows**, chat may not be able to generate a meaningful response until a new agent is attached.
- Very large or unsupported document types may fail to parse; see [Document Upload](./document-upload.md) for supported formats and limits.
- Switching agents mid-thread may change the tone or accuracy of responses, since different agents can be configured with different instructions or data access.
