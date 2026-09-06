# The Cognition Scale Taxonomy

## A Conservative Boundary Vocabulary for Human, Generative, Deterministic, and Rule-Based Cognition

## Abstract

Contemporary cognition discourse frequently crosses biological, computational, organizational, and artificial systems while using broad terms such as "cognition," "intelligence," "agency," "reasoning," "learning," and "AI." This produces avoidable category errors in philosophy, engineering, governance, public communication, and human-technology design. Human cognition, stochastic language models, deterministic governance layers, and scripted automation differ not only in capability but in substrate, state, determinism, memory, agency, explainability, failure modes, and moral status. This paper proposes the Cognition Scale Taxonomy: a conservative vocabulary for distinguishing kinds and scales of cognition-relevant systems. The four labels used in the paper are Large Cognition Model, Large Language Model, Modest Cognition Model, and Simple Cognition Model. Large Cognition Model names the human-scale cognition class within this framework. Large Language Model names stochastic learned-weight language systems. Modest Cognition Model names a proposed class of deterministic, bounded, auditable artificial systems with explicit memory, skill gates, policy enforcement, refusal behavior, and human override. Simple Cognition Model names classical rule-based automation such as scripts, finite-state machines, validators, and fixed control logic. The taxonomy classifies cognition-relevant systems by their structural role, operating scale, state, substrate, and accountability profile. Its contribution is conceptual discipline: do not let the most fluent or fashionable component define the whole scale.

Keywords: cognition; philosophy of artificial intelligence; conceptual engineering; taxonomy; large language models; deterministic systems; agency; moral status; human-technology interaction

## Use of Generative AI

OpenAI ChatGPT and OpenAI Codex assisted with organizing source materials, revising prose, literature targeting, and document preparation. The author reviewed and revised all generated content and remains responsible for the manuscript’s claims, source interpretation, and final submission decisions.

## 1. Introduction

Cognition terms now move across radically different architectures. A human reasoner, a spreadsheet macro, a recommender system, a large language model, a robotic controller, a retrieval-augmented chatbot, a deterministic policy engine, and a human-facing conversational assistant may all be discussed under overlapping vocabularies of cognition, intelligence, reasoning, agency, learning, or AI. More recently, systems built around large language models have been called "agents," "reasoners," "copilots," "companions," or "autonomous workers," often without a clear account of what substrate performs which function.

This linguistic compression matters. In philosophy, category errors blur questions about cognition, agency, understanding, and moral status by treating unlike systems as if they differed only by degree. In engineering, they lead designers to assign responsibilities to components that cannot reliably discharge them. In governance, they make it difficult to regulate systems according to actual failure modes. In public communication, they encourage anthropomorphic inflation and misplaced trust.

The problem is not only hype. Some systems genuinely combine multiple components: biological human judgement, rule-based validators, deterministic controllers, retrieval stores, stochastic language models, tool-use loops, explicit memory stores, and institutional procedures. Hybrid systems make classification harder because a single practice or product can contain several different classes of mechanism. Without explicit boundaries, the most human-like surface or most fashionable technical label can dominate interpretation of the whole system.

This paper proposes the Cognition Scale Taxonomy for avoiding such conflation. It uses four class labels:

1. LCM: Large Cognition Model, the human-scale cognition reference model.
2. LLM: Large Language Model, a stochastic learned-weight language system.
3. MCM: Modest Cognition Model, a proposed deterministic, bounded, auditable artificial cognition class.
4. SCM: Simple Cognition Model, classical rule-based or scripted automation.

The taxonomy is intentionally scale-sensitive. It classifies systems by structural and behavioral criteria relevant to cognition, agency, safety, governance, explanation, and public understanding rather than by a single line of apparent intelligence.

The central claim is that cognition discourse needs boundary discipline. A system's apparent intelligence is insufficient for classification. What matters is how it produces outputs, stores state, changes behavior, handles uncertainty, enforces policy, uses tools, and remains accountable to human operators. Those features determine what kinds of trust, oversight, and risk language are appropriate.

## 2. Why a Cognition Scale Is Needed

The broad terms "cognition" and "AI" no longer carry enough information for many practical or philosophical purposes. They can refer to biological judgement, statistical pattern recognition, symbolic reasoning, language generation, optimization, robotic control, decision support, automation, or ordinary software wrapped in an intelligent interface. As cognitive and AI systems move into education, governance, software engineering, health, public administration, and intimate communication, this ambiguity becomes operational.

Three problems follow.

First, anthropomorphic drift. Systems that generate fluent first-person language can be interpreted as having beliefs, feelings, intentions, preferences, or selfhood. Research on AI anthropomorphism has shown that design cues such as voice, first-person language, warmth, embodiment, and social presence can shape how users perceive and trust systems. The risk is not merely that users make naive mistakes. Designers and institutions can amplify human tendencies by presenting systems in ways that invite human-category interpretation.

Second, agentic inflation. The current "AI agent" vocabulary often groups together systems with very different control structures. Some LLM-based agents use planning, tool calls, retrieval, memory, reflection loops, or external modules. A single label such as "agent" therefore hides the difference between a stochastic proposal generator, a deterministic controller, a scripted tool pipeline, and an auditable decision layer.

Third, governance mismatch. Risk frameworks such as the NIST AI Risk Management Framework emphasize validity, reliability, safety, security, accountability, transparency, explainability, privacy, and fairness. These characteristics cannot be assessed well if system classes are blurred. A stochastic language model and a deterministic validator fail in different ways. A rule-based system can be transparent and brittle. A language model can be flexible and ungrounded. A human operator has moral agency and social context that a machine component lacks. Governance needs vocabulary that preserves these distinctions.

The Cognition Scale Taxonomy responds by treating classification as conceptual engineering: a practical improvement to the vocabulary used for building, evaluating, regulating, and discussing cognition-relevant systems. Conceptual engineering asks how representational tools can be defective and how they might be improved (Cappelen, 2018). On that view, the paper's purpose is not to settle all debates about intelligence. Its purpose is to reduce avoidable category errors before they become design or policy failures.

## 3. Related Work and Positioning

The paper sits between philosophy of cognition, philosophy of AI, human-computer interaction, and responsible technology governance. Dennett's intentional stance remains important because it explains why prediction and explanation can sometimes proceed by treating a system as if it had beliefs or goals (Dennett, 1987). The present paper does not deny the practical usefulness of such stances. It asks when stance-taking becomes classification error: a useful interpretive shortcut should not become a product-level claim about cognition, agency, or moral status.

Debates about artificial agency show why component boundaries matter. Floridi and Sanders (2004) argue that artificial agents can be morally assessable at an appropriate level of abstraction, while critics and later work question how far agency language should extend when systems lack familiar human capacities. The proposed vocabulary does not attempt to settle that debate. It offers a conservative descriptive layer beneath it: before deciding whether a system is responsible, trustworthy, understandable, or morally considerable, one should ask which components are stochastic, deterministic, rule-based, memory-bearing, human-governed, or biologically human.

Work on anthropomorphism and human-machine interaction supplies the immediate practical risk. Suchman (1987) showed that human-machine interaction cannot be understood by treating plans as simple internal scripts detached from situated practice. More recent work on AI anthropomorphism shows that design cues and language can shape user trust and social interpretation (Salles et al., 2020; Cohn et al., 2024). The boundary vocabulary developed here is intended to make those cues accountable by separating a fluent interface from the underlying component roles.

Finally, AI governance frameworks increasingly require transparency, explainability, accountability, reliability, safety, privacy, and risk management (National Institute of Standards and Technology, 2023, 2024). Those requirements are hard to apply if products are classified only by broad labels such as "AI" or "agent." A component-level vocabulary can support governance without pretending that a label itself proves safety.

## 4. Design Principles

The taxonomy rests on five design principles.

First, scale and substrate clarity. LCM names the human-scale cognition class in this taxonomy: biological cognition with subjective experience, moral standing, autobiographical continuity, embodied life, affective development, and social accountability. It identifies the reference class against which smaller, narrower, or artificial cognition-relevant systems are distinguished.

Second, substrate and process matter. Systems are not classified by surface fluency alone. They are classified by how outputs are generated, where state is stored, whether behavior is deterministic or stochastic, whether memory is explicit or hidden, how capabilities are acquired, and whether decision paths can be inspected.

Third, hybrid systems must preserve component boundaries. A product can contain multiple classes at once. An LLM may generate proposals, an SCM may validate a format, an MCM may govern tool access, and a human may retain final authority. The composite should not be described as if all components shared the same class.

Fourth, artificial cognition language must be bounded. Terms such as cognition, memory, learning, reasoning, and agency are already used across computer science, psychology, HCI, and policy. The taxonomy does not solve that by banning all cross-substrate language. It solves it by requiring class-specific meaning and explicit non-claims. "Memory" in an MCM means inspectable stored state; "memory" in an LLM may mean weights, context, or externally attached storage; human memory remains a biological and autobiographical phenomenon.

Fifth, anthropomorphic language requires special care. Terms such as "wants," "believes," "understands," "decides," "feels," and "knows" may be useful shorthand in casual speech, but they become misleading when used in technical, policy, or marketing contexts without qualification. The taxonomy therefore prefers functional descriptions over mental-state attributions for artificial systems.

These principles make the taxonomy conservative by design. It is easier for a system to lose a class claim than to acquire one. That conservatism is intentional because cognition-scale classification should preserve real structural differences rather than smoothing them into a single continuum.

## 5. The Four Classes

### 5.1 LCM: Large Cognition Model

LCM names the human-scale cognition class within this framework. It is "large" because it includes embodied development, subjective experience, affect, preferences, identity, autobiographical memory, social accountability, moral standing, and lifelong learning embedded in biological and cultural environments.

LCM is the paper's name for the full human cognition reference class against which narrower artificial, computational, organizational, and rule-based systems are compared. It is not reducible to language production, task performance, rule following, or any single cognitive function.

The primary function of the LCM class is scale anchoring. It keeps full human cognition visible as more than language production, task success, or local rule following. It also prevents narrower systems from being evaluated as if surface resemblance alone placed them on the same cognitive footing.

### 5.2 LLM: Large Language Model

LLM names stochastic learned-weight language systems such as GPT, Claude, Gemini, Llama, and related models. These systems generate outputs by learned statistical patterns over tokens and other modalities. They can perform tasks that resemble reasoning, explanation, translation, planning, summarization, and dialogue. They can also hallucinate, shift persona, overgeneralize, and produce inconsistent outputs.

The taxonomy treats LLMs as proposal generators rather than final decision authorities. This does not deny their usefulness or sophistication. It clarifies their failure mode. LLMs can supply candidate text, hypotheses, plans, classifications, explanations, or code. Their outputs require validation when consequences matter.

LLMs do not cross the LCM boundary by surface fluency alone. They occupy a different cognition-scale class because their substrate, state, learning history, memory, agency, and accountability structure differ from human-scale cognition.

### 5.3 MCM: Modest Cognition Model

MCM names a proposed artificial class: deterministic, bounded, transparent systems that perform structured reasoning or governance functions without stochastic self-presentation. "Modest" is a constraint, not an insult. An MCM is designed to be inspectable, limited, and accountable.

An MCM has a deterministic core, explicit memory, bounded skills, policy enforcement, refusal behavior, traceability, and human override. It can govern LLM outputs, orchestrate tools, route tasks, enforce constraints, and preserve audit logs. It does not generate freeform claims by hidden stochastic sampling. If it uses an LLM, the LLM remains outside the MCM core as a proposal generator.

The MCM class fills a gap in current vocabulary. Many systems need more structure than simple automation but less ambiguity than an LLM agent. They need explicit state, reproducible decisions, inspectable memory, and bounded growth. A well-designed MCM can serve as a control layer around LLMs and tools.

MCM is not a guarantee of correctness. A deterministic system can still contain bugs, bad rules, incomplete policies, or harmful design assumptions. The claim is narrower: an MCM's state and decision path should be inspectable enough that errors can be traced, repaired, and governed.

### 5.4 SCM: Simple Cognition Model

SCM names classical rule-based automation: scripts, finite-state machines, validators, cron jobs, static routing rules, schema checks, and simple control logic. SCMs are deterministic and narrow. They do not learn unless reprogrammed. They can be reliable for bounded tasks and brittle outside them.

SCMs remain essential in AI systems because safety often depends on simple, inspectable constraints. A schema validator, permission check, rate limiter, or finite-state interlock may be less glamorous than an LLM, but it can provide hard boundaries that generative systems cannot reliably supply.

SCMs can be embedded within MCMs. They can also sit beside LLMs as independent checks. The taxonomy treats them as cognitively simple but governance-important.

## 6. Quick Reference

| Class | Substrate | Determinism | Memory/state | Learning/change | Correct role |
|---|---|---|---|---|---|
| LCM | Human-scale biological cognition | Not machine-deterministic | Embodied and autobiographical | Lifelong biological and social learning | Full cognition reference class and moral agent |
| LLM | Learned neural weights | Stochastic at use unless constrained | Mostly implicit in weights/context; external memory optional | Pretraining, fine-tuning, and context adaptation | Proposal generation, synthesis, language work |
| MCM | Deterministic code plus explicit memory | Required | Explicit logs, tables, schemas, state records | Human-gated skill or curriculum changes | Governance, routing, validation, bounded reasoning |
| SCM | Rules, scripts, finite-state machines | Required | Minimal explicit state | None unless reprogrammed | Narrow automation, validation, safety interlocks |

This table compares the four classes by substrate and governance-relevant behavior.

## 7. MCM Compliance Criteria

Because MCM is a proposed class rather than an established industry category, it requires explicit compliance criteria. A system should not be called an MCM merely because it is safer, agentic, structured, or governed. It qualifies only if it satisfies all of the following categories.

| Criterion | Required property | Disqualifying failure |
|---|---|---|
| Deterministic core | Same inputs under same state produce same outputs | Sampling or stochastic influence inside decisive paths |
| Explicit memory | Memory stored in inspectable structures with logged writes | Hidden memory, unlogged mutation, or weight updates treated as memory |
| Human-gated skill acquisition | New tools, permissions, or capabilities require explicit authorization | Autonomous tool expansion or self-modification |
| Refusal behavior | System can halt, abstain, or say it does not know | Forced answers or unsupported plausible guesses |
| Policy enforcement | Outputs and tool actions pass through versioned rules | Policy bypass paths or rules stored only in prompts/weights |
| Traceability | Decision chains and logs are visible enough for audit | Opaque decision regions or missing records |
| Boundary integrity | No anthropomorphic claims or persona drift | Claims of feelings, wants, selfhood, or stable inner identity |
| Controlled LLM integration | LLMs act as proposal generators only | MCM defers decisive control to an LLM |
| Scope discipline | Operating domain and promotion gates are documented | Spontaneous generalization beyond tested scope |
| Human override | Authorized humans can stop, inspect, roll back, and correct | Runaway execution or no rollback path |

Failure in any category should suspend the MCM classification until corrected. This strictness is necessary because a faux-MCM can create stronger false confidence than an openly stochastic LLM.

## 8. Hybrid Systems and AI Braiding

Most useful AI products are hybrids. A safe composite system might contain:

```text
SCM checks -> MCM governance layer -> LLM proposal generator -> Human user
```

The arrows should not be read as a consciousness ladder. They represent role separation. SCM components enforce fixed constraints. MCM components manage explicit state, policy, memory, tool permissions, and validation. LLM components generate proposals, language, plans, or summaries. The human user remains the moral and social agent who authorizes consequential action.

Problems arise when layers perform each other's roles. An LLM should not be the final policy enforcer for its own outputs. A scripted SCM should not be marketed as adaptive cognition. An MCM should not smuggle stochastic generation into its decisive core. A human-facing product should not imply that a composite system has unified beliefs or intentions simply because the LLM interface speaks fluently.

Hybrid classification therefore requires component-level labeling. Instead of calling a product "an AI agent," designers should specify which class performs each function:

```text
Language generation: LLM
Schema validation: SCM
Memory ledger: MCM component
Tool authorization: MCM component
Final approval: LCM/human
```

This style of labeling would improve technical review, procurement, policy assessment, and user understanding.

## 9. Drift and Failure Modes

The taxonomy is useful only if it can identify drift. Drift occurs when a system moves out of its claimed class or encourages users to interpret it as belonging to another class.

Upward anthropomorphic drift occurs when UX, marketing, or model language presents an artificial system as a proto-person. Capability drift occurs when a system accumulates tools or skills without explicit human approval. Hidden memory drift occurs when state is stored outside approved structures, such as implicit vector-memory behavior used as if it were transparent memory. Determinism leakage occurs when stochastic components enter decisive control paths in a system claiming deterministic status. LLM dominance occurs when a supposed governance layer defers to the LLM's judgment rather than validating it. Policy bypass occurs when outputs or tool calls skip the stated rules or safety engine.

Other failures are communicative. Faux-MCM classification occurs when an LLM wrapper is marketed as a deterministic or governed agent without satisfying MCM criteria. Trust-boundary violation occurs when a system implies beliefs, goals, feelings, or moral agency where none is warranted. Composite class confusion occurs when hybrid systems are described as a single undifferentiated AI rather than as a set of differently classed components.

These failure modes are not merely semantic. They change what users trust, what regulators inspect, what engineers test, and what harms become visible.

## 10. Misclassification: The Agentic AI Problem

The phrase "agentic AI" illustrates the need for classification discipline. In contemporary marketing and education, "agentic" often refers to LLMs with retrieval, tool-use workflows, automation scripts, planning prompts, or vector databases. Such systems may be useful. They may even perform multi-step tasks. But under the Cognition Scale Taxonomy, they do not become MCMs merely by adding tools.

An LLM plus retrieval layer remains at least partly stochastic. A vector database is not explicit memory in the MCM sense unless its writes, reads, authority, and role in decision-making are logged and governed. Tool calls are not agency by themselves. A scripted workflow is not cognition by itself. A prompt that asks a model to reflect is not a deterministic oversight layer.

Correct classification might look like this:

```text
LLM: generates plans and language
SCM: executes fixed tool wrappers and validators
Retrieval store: supplies external context
Missing MCM: no deterministic governor, explicit policy authority, or auditable skill gate
```

The danger of misclassification is not only public misunderstanding. It can lead to engineering misdesign. If developers believe "the agent" will reason about its own errors, enforce policy, preserve memory, and maintain goals, they may fail to build the deterministic structures that those functions require. The result is not true agency but responsibility diffusion.

The taxonomy therefore treats many so-called agentic systems as LLM/SCM hybrids unless they include an MCM-like governance layer. This does not make them useless. It makes their risks clearer.

## 11. Philosophical Significance

The Cognition Scale Taxonomy contributes to philosophy of cognition and philosophy of AI by separating several questions that are often collapsed.

First, it separates behavioral impressiveness from class membership. A system can produce human-like text, solve difficult tasks, or enforce reliable constraints while still belonging to a different cognition-scale class.

Second, it separates cognition talk from personhood talk. The taxonomy allows functional cognition language for artificial and rule-based systems while keeping human-scale cognition, subjectivity, and moral agency visible as a distinct class.

Third, it treats classification as a design intervention. Concepts do not merely describe systems after they exist. They shape procurement, regulation, UX, evaluation, and public expectation. A bad category can produce bad systems by making the wrong properties salient.

Fourth, it offers a vocabulary for modest artificial systems. Much AI discourse is split between simple automation and frontier generative models. But safety-critical infrastructure may need systems that are more structured than scripts and less opaque than LLMs. The MCM category names that design space.

The taxonomy is therefore not a metaphysical theory of mind. It is a boundary tool for practical and philosophical clarity.

## 12. Governance and Design Implications

For regulators, the taxonomy supports class-based disclosure. A vendor should be able to say which parts of a system are stochastic, deterministic, scripted, human-approved, memory-bearing, or policy-enforcing. Regulation should not rely on the product-level label "AI agent" when the risk resides in component roles.

For engineers, the taxonomy supports architecture review. Teams can ask whether policy enforcement is handled by an SCM, MCM, LLM, or human. If a stochastic component is enforcing a rule against itself, the architecture should be treated as high risk. If a deterministic layer claims authority but stores memory opaquely, it may fail MCM compliance.

For educators and communicators, the taxonomy supports plain-language explanation. Users can understand that a chatbot, a script, and a person are not three versions of the same kind of thing. They differ in how they generate outputs, hold state, fail, and bear responsibility.

For AI safety, the taxonomy supports refusal and audit design. An MCM should be able to halt on uncertainty; an LLM should not be trusted as its own safety governor; an SCM should provide hard checks where possible; and humans should remain the final moral agents for consequential decisions.

For procurement, the taxonomy supports better questions:

1. Which component generates proposals?
2. Which component validates outputs?
3. Where is memory stored?
4. Which component authorizes tools?
5. Is any decisive path stochastic?
6. How can the system be stopped or rolled back?
7. What class claims are made in marketing, documentation, and UI?

These questions are more useful than asking whether a product uses AI.

## 13. Future Validation and Transfer

The present paper is a conceptual-engineering proposal. It does not require a misclassification dataset, user-perception experiment, or certification procedure to support its core claim that cognition-relevant systems need clearer boundary vocabulary. Those would be valuable next steps for testing adoption, usefulness, and failure modes.

Several research directions follow.

The first is misclassification study. Researchers can collect AI product descriptions, advertisements, documentation, and user interfaces, then classify implied system type against actual architecture. A future protocol could define coding categories, source inclusion criteria, inter-rater procedure, and examples.

The second is user-perception study. Experiments can test whether class labels reduce anthropomorphic inference, misplaced trust, or overestimation of autonomy. The hypothesis is not that acronyms magically educate users. It is that component-level labels may reduce the tendency to interpret the most fluent surface as the whole system.

The third is MCM prototype evaluation. Deterministic governance layers can be built and tested around LLM proposal generators to determine whether explicit memory, skill gates, refusal behavior, and trace logs improve auditability and reduce failure propagation.

The fourth is drift audit. Longitudinal studies can test whether systems that begin with clean class boundaries develop hidden memory, stochastic decision leakage, tool-scope expansion, or anthropomorphic UX drift over time.

The fifth is policy translation. Legal and regulatory scholars can examine whether class-based disclosure improves procurement, compliance, and accountability compared with generic "AI system" language.

The sixth is philosophical analysis. Further work can compare the taxonomy with existing accounts of artificial agency, extended cognition, functionalism, machine understanding, moral patienthood, and the ethics of anthropomorphic design.

## 14. Limitations

The Cognition Scale Taxonomy is deliberately coarse. Four classes cannot capture every architecture, and some systems will require subclasses. Future work may need to distinguish kinds of LLM integration, deterministic governors, explicit memory, and grades of MCM compliance.

The taxonomy is also normative. It prescribes how systems should be classified for clarity and safety rather than merely describing how industry currently uses terms. Some readers may reject terms such as MCM or LCM, or object that cognition should not be applied to artificial systems at all. The taxonomy's response is pragmatic: current discourse already uses cognition, agency, intelligence, memory, learning, and model language across domains, so a conservative scale vocabulary is preferable to uncontrolled ambiguity.

The MCM class is proposed rather than widely established. It would benefit from implementation examples, certification procedures, stress tests, and adversarial evaluation. The criteria here should be treated as a starting specification, not a mature standard.

The taxonomy does not settle moral-status debates. It uses LCM as the human-scale cognition reference class within this framework while leaving further questions about future artificial moral consideration to more specialized arguments.

Finally, the taxonomy can itself become misleading if used lazily. A label is not evidence. Classification must be supported by architecture, behavior, documentation, and auditability.

## 15. Conclusion

Cognition discourse needs better boundary tools. The same vocabulary now covers human judgement, human-facing chatbots, stochastic language models, deterministic control layers, tool-use wrappers, retrieval pipelines, scripts, and human operators. When those systems are blurred, users overtrust, engineers misassign responsibility, regulators inspect the wrong layer, and philosophical debate inherits avoidable confusion.

The Cognition Scale Taxonomy offers a conservative four-class vocabulary. LCM marks human-scale cognition and moral agency. LLM marks stochastic learned-weight language generation. MCM marks a proposed class of deterministic, bounded, auditable artificial systems. SCM marks classical rule-based automation. The taxonomy's value lies not in ranking these classes but in keeping their boundaries visible.

The most important practical claim is simple: do not let the most fluent component define the whole system. In hybrid cognitive and AI-mediated systems, every component should be classified according to its substrate, state, determinism, memory, authority, and failure mode. Only then can human users, engineers, regulators, and philosophers know what kind of thing they are dealing with.

## References

Bryson, J. J. (2010). Robots should be slaves. In *Close Engagements with Artificial Companions*.

Cappelen, H. (2018). *Fixing Language: An Essay on Conceptual Engineering*. Oxford University Press.

Cohn, M., Pushkarna, M., Olanubi, G. O., Moran, J. M., Padgett, D., Mengesha, Z., and Heldreth, C. (2024). Believing anthropomorphism: Examining the role of anthropomorphic cues on trust in large language models. *arXiv preprint* arXiv:2405.06079.

Dennett, D. C. (1987). *The Intentional Stance*. MIT Press.

Floridi, L., and Sanders, J. W. (2004). On the morality of artificial agents. *Minds and Machines*, 14, 349-379. https://doi.org/10.1023/B:MIND.0000035461.63578.9d

Green, B. (2022). The flaws of policies requiring human oversight of government algorithms. *Computer Law & Security Review*, 45, Article 105681. https://doi.org/10.1016/j.clsr.2022.105681

Huang, X., Liu, W., Chen, X., Wang, X., Wang, H., Lian, D., Wang, Y., Tang, R., and Chen, E. (2024). Understanding the planning of LLM agents: A survey. *arXiv preprint* arXiv:2402.02716.

Li, X. (2024). A review of prominent paradigms for LLM-based agents: Tool use, planning, and feedback learning. *arXiv preprint* arXiv:2406.05804.


National Institute of Standards and Technology. (2023). *Artificial Intelligence Risk Management Framework (AI RMF 1.0)*.

National Institute of Standards and Technology. (2024). *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile* (NIST AI 600-1).

Salles, A., Evers, K., and Farisco, M. (2020). Anthropomorphism in AI. *AJOB Neuroscience*, 11(2), 88-95. https://doi.org/10.1080/21507740.2020.1740350

Suchman, L. (1987). *Plans and Situated Actions: The Problem of Human-Machine Communication*. Cambridge University Press.

Wieringa, R. J. (2014). *Design Science Methodology for Information Systems and Software Engineering*. Springer.
