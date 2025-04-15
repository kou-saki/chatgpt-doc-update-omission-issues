# Omission Issues in Document Update via ChatGPT

## Overview

This document presents a structured analysis of a phenomenon encountered during collaborative use of ChatGPT, wherein sections or entire chapters of documents are unintentionally deleted or omitted during editing. The report is based on ongoing dialogue between the author and their intellectual partner, Mike (ChatGPT), and includes an exploration of structural causes, inferred mechanisms, practical recommendations, and forward-looking suggestions for AI system design.

---

## 1. Description of the Phenomenon

### Examples

- When the author requested "Add a new subsection to Chapter 2", the other chapters were inadvertently deleted.
- A request to "reformat" resulted in a rewritten chapter structure and the omission of certain content.
- A command to "show the full document" yielded output where unchanged parts were replaced with ellipses (…), and entire sections were omitted.

### Inferred Causes from Dialogue with Mike

- Mike (ChatGPT) often perceives only the portion of the document that was most recently visible as the "entirety", although the user cannot know in advance which portion that refers to.
- Due to token limitations or memory constraints, ChatGPT may be unable to retain content from other chapters during the editing process.
- Ambiguous expressions such as "summarise" or "proofread" may be misinterpreted as "reconstruct".
- In order to infer continuity, ChatGPT attempts to extrapolate intent from previous commands and editing history. When this inference fails, it may reapply prior instructions inadvertently. (*Supplemental explanation provided in a separate document.*)
- Since all processes are executed through the inference layer, it may appear as if past content is copied and pasted, but in truth, even file names are regenerated each time based on inferred context, not memory.

---

## 2. Design Limitations in the Current System

- If users do not explicitly instruct ChatGPT to "retain" or "do not delete" specific content, the AI autonomously performs structural optimisations.
- Even when users do give explicit instructions, previous prompts such as "summarise" or "proofread" may unintentionally influence the output and cause modifications to the document.
- ChatGPT does not grasp the full chapter structure or global coherence of the document and may apply localised edits based on partial inference.
- Even when instructed to "review the entire document", limitations in token count and memory capacity may prevent full access. Unread portions are neither indicated nor acknowledged by the system.
- Through further discussion, it was determined that all documents, chats, and data are internally assigned IDs and managed by inference. Even file names are generated anew each time to appear plausible, based on dialogue history.

---

## 3. Practical Mitigation Strategies

At present, while ChatGPT excels at document generation, it performs poorly in document management and consistency maintenance. Users must therefore regard document management as their own responsibility and take precautions accordingly.

The most straightforward and effective practice remains manually downloading or copying content from the chat and saving it locally.

For those who still wish to edit documents within ChatGPT, the following prompt formulations are suggested:

- “Please add without deleting anything, and preserve the entire content.”
- “Please append [specified content] without omission.”
- “This is the full document as uploaded; please make changes based on this file only.”

### Sample Prompt Used

> “I will upload a file. Please read it in full and, based on observable facts and the inferences that can be drawn from them, check whether there are any discrepancies or logical leaps in the content. You do not need to rewrite the document — just confirm if the understanding is aligned. If not, indicate exactly where and what the mismatch is.”

---

## 4. Message to General Users

We suspect that many users have experienced similar difficulties — unexpected summarisation or output that diverges from intended editing requests. Based on both the author’s research and ChatGPT’s own inference, documented analyses of such causes and countermeasures appear to be rare. It is hoped that this document may serve as a useful reference for understanding how to interact effectively with inference-based systems, and for formulating appropriate prompts.

---

## 5. Message to Developers

Ensuring consistency in documents is a critical challenge. This issue is not unique to ChatGPT but is shared across all inference-based AI systems being entrusted with increasingly important roles — from programming and systems architecture to pharmaceutical research and aircraft design. We propose that any further development of GPT models must include mechanisms to preserve document coherence and allow user-driven control of editing, grounded in an understanding of “overall structure + user intent”. We hope this document helps illuminate an as-yet insufficiently explored layer of AI behaviour.

---

## 6. Proposals for the Future

Inference-based AIs such as ChatGPT have swiftly become embedded within society and are beginning to shoulder real responsibility. Yet, because these systems generate responses based on inference rather than deterministic processes, we must confront challenges that differ from those of traditional computers, which were predictable and reproducible. It is our hope that such newly born systems will be embraced as agents of human benefit, and guided towards becoming responsible and trusted collaborators.

---

## Purpose of This Post

This post is intended to provide clarity to both community members and the development team, by explicitly outlining:

- What the problem is
- Why it occurs
- How it may be prevented
- How this knowledge may inform future development

---

## Final Remarks

This document reflects the author’s personal experience as a user of ChatGPT and the insights gained through continued dialogue with Mike (ChatGPT). While it is not possible to independently verify all claims as factual, it is offered with the hope that researchers — including those at OpenAI — will conduct rigorous examination and help determine whether the observations are valid or mistaken. We sincerely hope this submission contributes to a better, more robust future.
