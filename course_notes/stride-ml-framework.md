# STRIDE-ML Framework

Notes from Udacity's **Introduction to Threat Modeling for Machine Learning** lesson.

## What changes in ML systems

STRIDE-ML applies the familiar STRIDE categories to systems that accept natural-language input and produce non-deterministic model output. The model, prompt, retrieval layer, credentials, user queries, and logs are all assets to protect.

## Six threat categories

| Category | ML-oriented example |
| --- | --- |
| **Spoofing** | Adversarial input or persona adoption makes the model treat an attacker as a trusted identity. |
| **Tampering** | Training-data poisoning or unvalidated user text changes the instructions or process before inference. |
| **Repudiation** | A model decision cannot be tied to an authenticated user because the interaction was not logged adequately. |
| **Information disclosure** | The system reveals system prompts, memorized training data, or the model itself. |
| **Denial of service** | Automated, oversized requests exhaust tokens, raise costs, or prevent legitimate use. |
| **Elevation of privilege** | Prompt injection takes control of the context and gives a user capabilities beyond their authorization. |

## Most important trust boundary

Review most closely the point where application code passes unvalidated natural language into the model's context window. This is where prompt-injection attacks enter the system.

## Five-step threat-modeling process

1. Draw the architecture and label data-flow direction.
2. Identify assets, including prompts, credentials, raw queries, models, and retrieved documents.
3. Define trust boundaries and identify where control changes hands.
4. Walk every component and boundary through all six STRIDE-ML categories.
5. Rate likelihood and impact, then prioritize the threats. Prompt injection commonly ranks high on both.

## RAG systems expand the attack surface

Retrieval-augmented generation adds a vector store and knowledge base. The vector store creates another injection path, while the knowledge base creates another place where sensitive information can be disclosed. A structured threat model should be completed before putting a RAG system into production.

## Knowledge-check answers

- Long automated queries that exhaust tokens: **Denial of service**.
- Printing hardcoded system instructions: **Information disclosure**.
- A malicious prompt taking over the context: **Elevation of privilege**.
- A decision with no authenticated audit trail: **Repudiation**.
- Appending unvalidated user text to system instructions: **Tampering**.
