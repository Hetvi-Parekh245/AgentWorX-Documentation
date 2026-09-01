# Workspace Settings

Workspace Settings let you configure a workspace after it's already been created — from branding and document access to which agents, workflows, and members are attached. Changes here apply only to the workspace you're editing.

## Short Description

Settings are organized into tabs that closely mirror the [Create Workspace wizard](./creating-and-managing.md), so anything you set up initially can be revisited and changed later from one place.

## When to Use It

Use Workspace Settings when you need to:

- Rebrand the workspace's assistant with a custom profile image
- Turn on personal SharePoint access for members
- Update business tags, retrieval configuration, attached agents/workflows, dashboards, or members
- Delete a workspace entirely

## How to Get Here

- From the **Workspaces** list, click the **⋮** menu on any workspace card and select **Settings**.

## The Settings Screen

![Workspace Settings modal](./assets/workspace-settings-modal.png)

Settings open as a modal over the workspace, organized into the following tabs:

| Tab | Purpose |
|---|---|
| **General Settings** | Assistant branding, Personal SharePoint access, and workspace deletion (see below) |
| **Business info** | Industry, Department, Data Classification, Use Case, and other tags — same fields as [Step 2 of workspace creation](./creating-and-managing.md#step-2-business-info) |
| **Bindings** | The workspace's underlying technical connections — Vector DB, Embedder, and Parser (set initially in [Step 3](./creating-and-managing.md#step-3-workspace-configuration)) |
| **Retrieval** | Controls how the workspace searches and retrieves grounded content from your documents when answering questions |
| **Documents** | Manage the workspace's attached documents — opens the same view as [Document Upload & Grounding](./document-upload.md) |
| **Agents & workflows** | Add or remove the agents and workflows attached to the workspace (see [Steps 5 and 6](./creating-and-managing.md#step-5-agents)) |
| **Dashboard** | Manage embedded Power BI workspaces and reports (see [Step 8](./creating-and-managing.md#step-8-dashboard)) |
| **Members** | Add, remove, or change the role (Admin/Member) of people with access to the workspace — see [Managing Members](./creating-and-managing.md#managing-members) |

### General Settings, in Detail

- **Assistant Profile Image** — upload a custom image (800×800) to personalize how the workspace's assistant appears in chat.
- **Personal SharePoint** — a toggle that, when enabled, lets workspace members connect their own Microsoft account and pull files from their personal SharePoint directly on the upload page. This requires Azure AD SSO to already be configured under Admin settings.
- **Delete Workspace** — permanently deletes the workspace and all of its data for every user. This action cannot be undone.

## Expected Outputs

- Changes made in any tab take effect for all users of that workspace going forward.
- Changing **Bindings** (Vector DB, Embedder, Parser) after documents already exist may require those documents to be re-indexed.
- Deleting a workspace removes it — and all its documents, threads, and configuration — for everyone with access.

## Edge Cases and Limits

- **Delete Workspace is irreversible** — double-check before confirming, especially for shared/team workspaces.
- **Personal SharePoint** only becomes usable once an admin has configured Azure AD SSO; enabling the toggle alone isn't enough.
- Access to Workspace Settings itself may be restricted to Admin-role members — confirm your organization's permission setup if a teammate can't see the Settings option.
