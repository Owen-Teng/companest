# Mail assistant: implemented capabilities and how to try them

Companest starts with a concrete workflow: understand a conversation, prepare a reply, make the decision, and follow the same matter as circumstances change.

## A project example in the actual application

### 01 · Find a matter on the board

Enter the mail room and open the fictional P042 project-delivery matter.

![Actual mail matter board](media/scene-mail-room.jpg)

### 02 · Read the latest message and earlier context

The matter window presents new information and the earlier agreement beside the available handling choices.

![Actual matter window and context](media/scene-matter.jpg)

### 03 · Edit the reply in your own words

Choose an approach or write your own reply. The example adds a request for a list of unresolved items. Edits are saved locally.

![Actual editable draft](media/scene-edited.jpg)

### 04 · Decide, then follow up

The built-in example simulates a reply without sending external email. The matter can remain visible while waiting for a response.

![Actual follow-up state after a simulated reply](media/scene-followup.jpg)

### 05 · Review a changed request

The sender moves delivery from 20:00 to 22:00. The update stays with the original matter, and the existing draft is retained with a prompt to review the new context.

![Actual changed deadline and draft-review prompt](media/scene-update-detail.jpg)

[GIF montage](media/mail-scenes.gif) · [HD MP4 montage](media/mail-scenes.mp4)

These are real application screenshots from the version before renaming, using isolated fictional data. They still show Friday branding. The montage uses reading holds and transitions; it is not a continuous recording. Original assistant scene animation is not a business execution trace. The current application interface is in Chinese.

## Capabilities and conditions

| Capability | What it enables | Current evidence and limit |
|---|---|---|
| Account-free examples | Read fictional mail, edit drafts, simulate replies and incoming changes | Previously exercised in the local interface; no real account connection |
| Matter board and message viewing | Find pending matters, inspect messages and context | Implemented; shown in the examples |
| Editable, saved drafts | Choose an approach or write a reply and retain edits locally | Implemented, with example interaction and automated checks |
| Continued follow-up | Associate later messages with an existing matter | Implemented and tested synthetically; identical subjects alone do not establish a match |
| Draft review after updates | Preserve existing text while prompting review of new context | Demonstrated with the 20:00 to 22:00 example |
| 163 Mail connection and sync | Connect the user's own account and authorization code | Implemented; no fresh real-account verification in this presentation |
| Multiple accounts | Maintain account-specific cursors and use the matter's account for a reply | Implemented with local automated checks; not universal provider support |
| Explicitly confirmed sending | Review recipient and content, send, and retain result state | SMTP implementation and local protocol tests; server acceptance is not recipient delivery |
| Filter correction | Correct classification and mark or restore advertising mail | Implemented and automatically checked; not a guarantee of classification accuracy |
| Mail context and AI suggestions | Use related history, inspect suggested wording, citations, and uncertainty | Requires supported local Codex CLI setup, the user's login and usage allowance; not a live-model demonstration here |
| Local records and credential protection | Retain local work records and protect credentials through the local mechanism | Implemented; optional AI requests still transmit selected context to the configured service |

Implemented code, synthetic demonstrations, automated tests, live connections, and accepted business outcomes are distinct forms of evidence.

## Current limits

General onboarding supports 163 Mail. The company adapter needs its specific environment and independent certificates. This release does not claim universal mailbox support, automatic sending without explicit confirmation, complete understanding of all mail and attachments, or completed workflows for all six assistants. A general model-provider selector, mobile app, team sharing, and automatic updates are not delivered.

[Preview access](ACCESS.md) · [Source access](ACCESS.md) · [Data boundaries](ACCESS.md) · [Product story](ORIGIN.md)
