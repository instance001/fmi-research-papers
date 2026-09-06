# Local-First AI as Public-Interest Infrastructure

## Governed Hosts, Model Choice, and Evidence-Carrying Workflows

Author details removed for review.

## Abstract

Generative AI access is often mediated through cloud platforms that centralize model choice, data flow, workflow design, and user dependency. This paper argues for local-first AI tooling as a form of public-interest infrastructure: software that lets ordinary users run, inspect, adapt, and govern AI workflows without treating platform dependence as the default condition of participation. Drawing on a public local-first AI project ecosystem, the paper presents a design-study account of local-first and cloud-optional AI systems. The main case is a desktop host shell that combines local model selection, optional user-supplied cloud lanes, bounded file work, memory governance, module hosting, local networking, and evidence-carrying logs. Supporting cases show related patterns in mobile, education, creative media, model-building, and governed build workflows. The shared pattern is not anti-cloud. It is local by default, cloud when deliberately selected, with model choice, permissions, data paths, and artifacts kept visible to the operator. The paper identifies six design commitments: user-owned model selection, host-owned capability routing, bounded workspaces, explicit approval and handoff surfaces, local evidence artifacts, and graceful escalation to cloud or stronger tooling only when the task requires it. The paper does not claim that local systems are automatically safe, private, usable, or sufficient. It argues that responsible AI governance should include small, inspectable, user-controlled tools as part of the AI ecosystem rather than treating cloud platform access as the normal form of AI capability.

Keywords: local-first AI; public-interest technology; responsible technology; AI governance; user agency; platform dependency

## 1. Introduction

Most people encounter generative AI through cloud platforms. The platform hosts the model, controls the interface, stores or routes the data, decides which capabilities are exposed, and often determines how memory, tools, safety filters, accounts, model selection, and billing work. This model has advantages. It can provide strong models, reliability, centralized maintenance, and immediate access without local setup. But it also makes platform dependence feel inevitable.

Local-first AI tooling challenges that default. It asks what AI use looks like when the user's device, files, models, settings, workflows, and artifacts remain the starting point. In this view, cloud systems are useful lanes, not the whole road. A user may choose a hosted model when a task needs it, but ordinary AI work does not have to begin by surrendering the workflow to a remote service.

This paper argues that local-first AI tooling should be understood as public-interest infrastructure. It is not only a technical preference or hobbyist aesthetic. It is a way to preserve agency, learning, portability, inspectability, and pluralism in an AI ecosystem that otherwise tends toward concentration.

The argument is developed through a design-study synthesis with one central case and several supporting pattern cases. The central case is a local-first desktop AI host shell, because it combines local model choice, optional bring-your-own cloud lanes, memory governance, sandbox work, module hosting, local peer handoff, and evidence-carrying logs in one desktop environment.

The supporting cases are used only where they clarify a pattern that the desktop host cannot show alone: small-phone local AI, school-specific offline restraint, local creative generation, dataset and training preparation, and governed build attempts.

These projects are not presented as finished proof of national-scale impact. They are treated as a concrete design corpus showing how local-first AI infrastructure can be built around user control and auditability.

## 2. Method and Evidence Boundary

This manuscript is a responsible-technology architecture/design paper. It does not report a user study, adoption study, security audit, benchmark suite, or public-sector impact evaluation. Its narrower contribution is to identify a public-interest design pattern for local-first and cloud-optional AI: governed hosts that make model choice, data paths, workspace scope, memory evidence, permission boundaries, handoffs, and escalation visible to the operator.

The evidence base is implementation-grounded. It uses one actively developed desktop host as the main case and a small set of sibling tools as supporting pattern evidence. Source manuals, architecture notes, module and networking documentation, sandbox behavior, memory-governance descriptions, and build-workflow doctrine support claims about what the design pattern contains and how it can be operationalized. They do not prove that local-first systems are safer, more private, easier to use, or more socially beneficial in general.

This distinction keeps the paper proportionate. Existing artifacts are necessary evidence for the stated architecture claim. Inspection studies, usability studies, public-interest evaluations, and security audits would be valuable future validation, but they are not required unless the paper is revised to claim measured user outcomes, security outcomes, or public adoption effects.

**Figure 1. Governed local-first AI host pattern.** A user works through a local host shell. The host selects either a local model lane or an explicit user-supplied cloud lane, labels the active route, constrains file work to bounded workspaces, records evidence artifacts, manages memory through active context, rolling summaries, cold logs, and deliberate recall, and exchanges handoff bundles with modules or trusted local peers through inbox-style review. The model supplies capability within this host-governed envelope; the host carries routing, permissions, memory evidence, and escalation boundaries.

## 3. Background

The local-first software movement argues that applications should preserve user ownership, offline function, long-term accessibility, privacy, and control while still supporting collaboration where needed. Kleppmann, Wiggins, van Hardenberg, and McGranaghan framed local-first software as a response to cloud applications in which servers often become the authoritative site of user data and capability.

AI intensifies the same issue. The cloud platform may not only store user data. It may also own the model, the tool surface, the memory layer, the safety layer, the account identity, and the interaction history. This creates a deeper dependency than ordinary cloud storage.

Public-interest technology provides another frame. It asks how technology expertise can advance public benefit, dignity, accountability, and responsible use. Design justice and data feminism add a power analysis: who gets to build, who is served, whose labor is hidden, who is made dependent, and whose needs are treated as edge cases.

Local-first AI tooling belongs at the intersection of these traditions. It asks whether AI systems can be designed so that ordinary users, independent builders, teachers, disabled users, artists, small businesses, and local communities retain practical control over the tools shaping their work.

## 4. Public-Interest Infrastructure

Infrastructure is often noticed only when it fails. In AI, the visible product is the chat response, image, code patch, or generated training plan. The infrastructure underneath decides more quietly who can participate.

Public-interest AI infrastructure should support:

- meaningful user choice;
- transparent data paths;
- local operation where sufficient;
- portability of files, settings, and workflows;
- inspectable logs and artifacts;
- explicit permission boundaries;
- interoperability rather than lock-in;
- accessible setup for non-expert users;
- and escalation to stronger capability only when justified.

The local-first tooling described here does not reject cloud capability. It rejects cloud inevitability. A user should be able to stay local when local is enough, bring a cloud model when useful, and understand the difference.

This matters especially for people and groups who are not well served by enterprise procurement. A school may need offline operation. A disabled user may need assistive workflows that do not route every private thought through a platform. An artist may need local media generation and dataset control. A small builder may need a way to learn model training without buying into a full hosted stack.

## 5. Shared Design Commitments

The project cluster expresses six shared design commitments.

First, model choice belongs to the operator. Tools should not assume one mandatory model family or provider. Local GGUF models, helper models, provider-specific cloud models, and API-compatible endpoints can sit in the same selection philosophy when the host labels them clearly.

Second, the host owns capability routing. A tool should know which model, provider, lane, module, or runtime is active; what capabilities are available; and what limitations apply. The model should not be left to improvise authority.

Third, workspaces are bounded. The main host uses a named sandbox. The classroom tool uses a school data folder. The training-support tool curates material into local input folders. The governed build tool produces artifacts under controlled output and runtime areas. These boundaries make action reviewable.

Fourth, permissions are explicit. File writes, module handoffs, training runs, cloud lanes, local networking, and source fixes should be visible actions with preview, approval, or review where appropriate.

Fifth, artifacts carry evidence. Runs, logs, plans, prompts, summaries, sidecars, hash chains, manifests, receipts, and reports make it possible to inspect what happened later.

Sixth, escalation is deliberate. A stronger cloud model, web source, training backend, hosted module, or patch lane should be selected because the task calls for it, not because the tool silently collapsed into a provider default.

**Table 1. Responsible-Technology Commitments and Architectural Signals**

| Commitment | Architectural signal | Main case evidence | Responsible-technology purpose |
|---|---|---|---|
| User-owned model choice | Unified selector for local GGUF and optional BYO cloud entries. | Main host model picker and provider entries. | Prevents silent provider lock-in and makes capability selection inspectable. |
| Host-owned routing | The app records which local/cloud lane, module, runtime, or helper role is active. | Main host orchestrator and memory-helper model targets. | Keeps authority with the host/tool boundary rather than model improvisation. |
| Bounded workspaces | File work stays inside named local areas with visible task modes. | Sandbox, scratchpad, task ledger, sandbox task mode. | Reduces unbounded file access and preserves reviewable scope. |
| Explicit permissions | File writes, cloud lanes, module handoffs, and peer sharing are visible actions. | Sandbox create/edit modes, module bridge, local networking handoffs. | Makes action and delegation inspectable by the operator. |
| Evidence-carrying artifacts | Logs, summaries, sidecars, run outputs, task ledgers, and receipts remain local. | Cold logs, rolling summaries, module rundowns, sandbox notes. | Enables later review without depending on opaque platform telemetry. |
| Deliberate escalation | Cloud and stronger tools are chosen when the task calls for them. | BYO API-key lane pattern and provider health checks. | Treats cloud capability as an explicit route, not an unavoidable baseline. |

## 6. Main Case: Host Shell and Memory Governance

The main case is the central desktop shell in this design family. Its architecture treats local-first as the baseline, cloud as optional and user-supplied, hybrid workflows as first-class, and model choice as an operator decision.

The application includes a tabbed local UI, unified chat model selection, local GGUF runtime support, BYO cloud lanes, module hosting, sandbox tools, networking surfaces, and layered memory/context panels. The orchestrator and memory-helper lane can target local or cloud models according to saved preferences and provider capability.

The main case's memory design is particularly important. It distinguishes active context, rolling summaries, cold logs, semantic indexes, and deliberate recall attachments. Cold-log recall is user-triggered: search proposes bounded historical candidates; the user selects; the host injects exact selected transcript blocks into the next turn; and attachments clear after prompt construction. Semantic indexes store references and metadata over cold evidence rather than replacing the evidence source.

This architecture treats memory as host-governed evidence, not mystical model recollection. It also shows how local tools can become richer without becoming opaque.

The desktop host is therefore the main case because it concentrates the responsible-technology problem in one place. It is not simply a chatbot. It is a host shell that decides where model capability sits, what context is visible, what memory is summarized, what exact evidence can be recalled, what file actions are bounded, and which module or peer handoff is allowed.

**Table 2. Desktop Host as Main Case**

| Layer | What the user sees | What the host controls | Governance issue |
|---|---|---|---|
| Model lane | Local GGUFs beside configured cloud entries. | Provider settings, model names, health checks, role assignment. | Model choice and data-path visibility. |
| Memory/context | Hot Memory, Luke Warm summary, logs view. | Active context, rolling summary, append-only cold log, Bookkeeper search. | Continuity without fake model memory. |
| Sandbox | Browse, edit, and save files in a named local sandbox. | Scoped file area, task mode, structured file-action intent. | Bounded local action and review. |
| Modules | Hosted tabs and module menus. | Module manifests, status rundowns, bridge files, shared-state lanes. | Interoperability without collapsing tools into one opaque monolith. |
| Networking | Nearby same-family peers and handoff bundles. | Local-only peer discovery and explicit send/receive workflows. | Local collaboration without cloud sync as default. |
| Receipts | Logs, rundowns, task ledgers, saved artifacts. | Local evidence trail and summaries. | Accountability through artifacts rather than provider analytics. |

## 7. Supporting Pattern Cases

A mobile assistant translates the local-first pattern to small phones. It supports local inference by default, GGUF import through the Android document picker, private app storage, model role assignment, character prompt profiles, active context, rolling summary, sandbox files, and optional user-configured cloud providers where hosted capability is the better fit. This matters because public-interest infrastructure cannot live only on developer desktops. Mobile is where many users actually are.

A classroom assistant shows the same pattern under stronger domain constraints: offline school use, teacher authority, homework and revision boundaries, sandboxed work, and deliberate handoff rather than ordinary cloud dependency. Sensitive domains need more than general model choice; they need restraint that is visible in the workflow.

Creative and training-support tools extend the pattern to media generation, dataset curation, concept stacks, local outputs, sidecars, and training handoffs. These cases matter because creative AI governance includes source material, generated outputs, local datasets, model files, training plans, and explicit transfer between tools.

An accessible local model-building dashboard shows that model sovereignty is not only model selection. It is also model literacy: inspecting corpora, training a tokenizer, running a small checkpoint, and testing outputs.

A governed build tool explores local AI-assisted software construction. Its doctrine is:

```text
the user carries the intent
the LLM carries the method
the host carries the funnel
the output carries the artifact
```

The factory freezes a plain-language request into a bounded, checkable attempt. The host routes permissions, work order, mechanical steps, and verification. The model contributes method within those boundaries. The output carries the generated or patched artifact. If the attempt fails, the system classifies the failure, preserves receipts, and uses evidence to decide whether to decompose, retry, triangulate, or escalate.

This is relevant to public-interest AI because it resists two common problems: invisible automation and unbounded agentic drift. The host does not simply let a model roam. It records what was attempted, what failed, why the next attempt changed, and where verification occurred.

Governed build loops show how local AI tooling can support creation while preserving accountability.

The supporting cases should be used as pattern evidence, not as equal co-cases. Table 3 keeps their role narrow.

**Table 3. Supporting Pattern Cases**

| Supporting case | Pattern shown | Why the main desktop host alone is insufficient |
|---|---|---|
| Mobile assistant | Local-first and cloud-optional AI on small phones, including GGUF import and locally stored provider settings. | Public-interest infrastructure must reach mobile users, not only desktop builders. |
| Classroom assistant | Offline classroom AI with teacher authority, homework/revision boundaries, and no ordinary cloud dependency. | Sensitive domains need domain-specific restraint beyond general model choice. |
| Creative and training-support tools | Local creative generation, dataset handling, concept stacks, and training handoffs. | Creative AI governance includes source material, outputs, sidecars, datasets, and model-training preparation. |
| Local model-building dashboard | Approachable local corpus, tokenizer, training, and checkpoint workflows. | Model literacy is part of public-interest infrastructure, not only model selection. |
| Governed build tool | Governed build attempts with frozen intent, bounded work orders, failure receipts, and retry logic. | Local-first action needs attempt governance, not only a chat surface. |

## 8. Future Validation Agenda

The design-study claim can be evaluated through both technical and social criteria. A responsible-technology paper should ask not only whether local-first tools work, but whether their architecture actually makes control, evidence, and escalation more legible to users.

Technical evaluation should ask whether the tools work offline as documented, preserve data locally, label cloud routes clearly, enforce sandbox boundaries, store usable artifacts, recover from failures, and allow model changes without breaking workflows.

Human-computer interaction evaluation should ask whether non-expert users understand local versus cloud lanes, can inspect what data leaves the device, can manage models and keys, can recover outputs, and can use artifacts for review.

Governance evaluation should ask whether permission prompts, receipts, logs, and handoff previews actually support accountability rather than merely adding friction.

Equity evaluation should ask whether local-first tools help people outside institutional and enterprise settings participate more meaningfully in AI work.

Comparative evaluation could test local-first, cloud-only, and hybrid versions of the same workflow across privacy understanding, task success, setup burden, user confidence, reviewability, and repair after failure.

**Table 4. Future Validation Paths**

| Evaluation question | Method | Evidence produced |
|---|---|---|
| Can users distinguish local and cloud lanes? | Scenario tasks using local-only, cloud-selected, and failed-cloud conditions. | Correct lane identification, data-path comprehension, confidence ratings. |
| Are workspaces meaningfully bounded? | File-task exercises in sandbox and non-sandbox contexts. | Action success, refusal/permission behavior, user understanding of scope. |
| Do artifacts support later review? | Ask participants to reconstruct a completed workflow from logs, ledgers, rundowns, and outputs. | Reconstruction accuracy, missing evidence notes, perceived auditability. |
| Does local-first impose unacceptable burden? | Install/configuration walkthroughs across user skill levels. | Setup time, failure points, support needs, abandonment risk. |
| Does deliberate escalation improve fit? | Compare local-only, cloud-only, and explicit hybrid routes on matched tasks. | Task success, privacy comfort, model fit, switching friction, user control. |
| Do supporting cases show transferable commitments? | Cross-case artifact analysis across supporting mobile, classroom, creative, model-building, and governed-build tools. | Pattern matrix, divergences, domain-specific constraints. |

These studies would strengthen the paper, but they are not prerequisites for the present architecture/design claim. The current manuscript should not report user comprehension, trust, privacy, or adoption outcomes unless those studies are actually performed.

## 9. Risks and Limitations

Local-first AI has serious limits.

Local models may be weaker, slower, harder to install, or incompatible with user hardware. Local storage may be poorly secured. Users may misunderstand model limitations. Open tools can be misused. Optional cloud lanes can still leak sensitive data if the interface is unclear. Logs and artifacts can themselves become privacy risks.

The design corpus is also partial. These projects demonstrate working patterns and implementation directions, not broad public adoption. They do not prove that local-first tools are always more trustworthy or effective.

Another risk is romanticizing independence. Most users still need usable defaults, documentation, safe update paths, dependency management, and support. Public-interest infrastructure must be maintainable, not just principled.

Finally, local-first should not become anti-cloud dogma. The right answer is often hybrid. The policy and design claim is that the choice should be deliberate and visible.

## 10. What This Paper Is Not Claiming

This paper does not claim that cloud AI is bad or unnecessary.

It does not claim that local AI is automatically private, safe, ethical, or capable.

It does not claim that the listed tools are finished products or proof of population-scale impact.

It does not claim that ordinary users should be forced to manage every technical detail themselves.

It does not claim that user agency eliminates the need for regulation, platform responsibility, or institutional governance.

It claims that local-first and cloud-optional tools are an important part of the responsible AI design landscape.

## 11. Conclusion

AI capability should not be synonymous with platform dependency. Cloud systems will remain important, but they should not be the only practical route through which people can use, inspect, adapt, and build AI tools.

The project corpus shows one possible design vocabulary: local by default, cloud by explicit choice, model selection owned by the operator, capabilities routed by the host, workspaces bounded, actions reviewable, and artifacts preserved.

This is public-interest infrastructure in a grounded sense. It helps people keep a hand on the systems shaping their work. It treats AI not as a distant service to consume, but as a tool ecology that can be owned, examined, modified, and governed closer to where people live and create.

## References

Costanza-Chock, S. (2020). Design Justice: Community-Led Practices to Build the Worlds We Need. MIT Press. https://doi.org/10.7551/mitpress/12255.001.0001

D'Ignazio, C., and Klein, L. F. (2020). Data Feminism. MIT Press. https://data-feminism.mitpress.mit.edu/

Elsevier. (2026). Generative AI policies for journals. https://www.elsevier.com/about/policies-and-standards/generative-ai-policies-for-journals

Journal of Responsible Technology. (2026). Guide for authors. ScienceDirect. https://www.sciencedirect.com/journal/journal-of-responsible-technology/publish/guide-for-authors

Journal of Responsible Technology. (2026). Open access options. ScienceDirect. https://www.sciencedirect.com/journal/journal-of-responsible-technology/publish/open-access-options

Kleppmann, M., Wiggins, A., van Hardenberg, P., and McGranaghan, M. (2019). Local-first software: You own your data, in spite of the cloud. Proceedings of the 2019 ACM SIGPLAN International Symposium on New Ideas, New Paradigms, and Reflections on Programming and Software. https://doi.org/10.1145/3359591.3359737

McNealy, J. E. (2026). Policy for public interest technology. Journal of Internet Governance and Society. https://doi.org/10.1515/jigs-2026-0001

New America. (n.d.). Defining Public Interest Technology. https://www.newamerica.org/insights/defining-public-interest-technology/

Sambasivan, N., Kapania, S., Highfill, H., Akrong, D., Paritosh, P., and Aroyo, L. M. (2021). Everyone wants to do the model work, not the data work: Data cascades in high-stakes AI. Proceedings of CHI 2021. https://doi.org/10.1145/3411764.3445518

Suchman, L. A. (2007). Human-Machine Reconfigurations: Plans and Situated Actions. Cambridge University Press.

## Declaration of Generative AI and AI-assisted Technologies in the Manuscript Preparation Process

During the preparation of this work, the author used OpenAI ChatGPT and OpenAI Codex to assist with drafting, structuring, literature targeting, and document preparation. After using these tools, the author reviewed and edited the content as needed and takes full responsibility for the content of the submitted work.

## Declarations

### Conflict of Interest

The author declares no financial competing interests. The author developed and maintains the source repository ecosystem used as design-artifact evidence. This relationship should be disclosed because the manuscript analyzes tools and documentation from that ecosystem.

### Funding

No external funding was received for this work.

### Data Availability

No empirical dataset is reported. This design-study manuscript relies on local project documentation and implementation artifacts from the author's project ecosystem. A reviewer-safe source snapshot or artifact packet should be supplied where compatible with review anonymity, repository licensing, and journal policy. A future empirical version should define the exact project snapshots, user tasks, comparison systems, evaluation rubrics, interview or usability protocols, and artifact-analysis methods.
