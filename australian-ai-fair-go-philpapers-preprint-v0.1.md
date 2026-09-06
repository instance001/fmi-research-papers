# An Australian AI Fair-Go

## Broad Capability Sovereignty and Proportionate Governance for Local, Open, and Hybrid AI

Anthony Paterson  
Fractal Media Infrastructure  
5 Benjamin Drive, Gracemere, Queensland 4702, Australia  
Corresponding author: fractalmediainfrastructure@gmail.com  
ORCID: https://orcid.org/0009-0007-5750-5236

## Abstract

National artificial intelligence policy is often framed around two necessary but incomplete forms of sovereignty: domestic infrastructure and institutional capability. This paper argues for a third layer, broad national capability sovereignty: the practical ability of ordinary people, schools, disabled users, researchers, small businesses, regional communities, and independent builders to learn, inspect, run, adapt, evaluate, and govern lawful AI tools without first passing through a major platform or institutional gatekeeper. Using the Australian policy context as a case, the paper develops an "AI Fair-Go" position: protect people from harmful, high-impact, coercive, deceptive, or large-scale AI deployments while preserving lawful local, open, commercial, and hybrid AI options for ordinary users. The operating principle is: fit the tool to the job, give it only what that job requires, and keep the human in charge. The paper distinguishes hosting sovereignty, institutional sovereignty, and broad capability sovereignty; critiques enclosure-by-compliance; and proposes proportionate governance based on model, host, task, population, reach, and power over others. It uses local-first and cloud-optional tool patterns from an Australian project ecosystem as an implementation-oriented case, including BYO API-key lanes, model-agnostic local workflows, bounded school assistants, and model-host-task suitability testing. The paper concludes that AI safety and AI agency need not be opposites. A resilient national AI ecosystem should regulate harmful conduct and high-impact deployment without making concentrated platforms the only practical route to lawful participation.

Keywords: AI governance; AI sovereignty; local-first AI; public-interest technology; proportionate regulation

## Policy Significance Statement

Australia's AI policy already seeks to capture opportunity, spread benefits, and keep people safe. This paper adds a missing policy layer: broad national capability sovereignty. AI policy should protect people from high-impact, coercive, deceptive, and large-scale harmful systems without making major platforms the only practical route to lawful participation. The proposed AI Fair-Go framework helps policymakers distinguish personal tools, classroom tools, assistive technologies, research prototypes, small-business systems, public services, and automated decision systems. It recommends obligations that scale with model capability, host permissions, data sensitivity, affected population, reach, and power over others, while preserving lawful local, open, commercial, and hybrid AI options. This helps align safety, inclusion, innovation, and public trust without enclosing ordinary lawful experimentation.

## 1. Introduction

Australia's AI policy problem is not simply how to obtain more powerful AI systems. It is how to build a society in which AI capability is useful, safe, inspectable, widely distributed, and governed without narrowing practical participation to a few large vendors or already-resourced institutions.

This paper proposes an Australian AI Fair-Go position. The core principle is plain:

Fit the tool to the job. Give it only what that job requires. Keep the human in charge.

This principle supports strong safeguards for high-impact systems, deceptive uses, coercive deployments, children's settings, privacy-sensitive contexts, and large-scale automated decision-making. It also supports preserving lawful local, open, commercial, and hybrid AI options for ordinary users and independent builders. These commitments are not in tension. A local school assistant, a disability-support workflow, a small-business automation tool, a frontier research model, and a national automated-decision system do not have the same risk profile. They should not be forced into the same regulatory or technical shape.

The policy wedge is:

Do not solve concentrated technological power by concentrating technological permission.

If rules designed to restrain large AI platforms can only be satisfied by large AI platforms, the result may be dependency with paperwork. A country can host data centres, procure enterprise systems, and fund institutional AI programs while still leaving broad national capability underdeveloped. Sovereignty must include more than infrastructure and institutions. It must include the ability of people across the country to understand, choose, run, adapt, test, and govern AI tools at the level appropriate to their needs.

The paper is conceptual and policy-oriented. It does not claim that local or open AI systems are risk-free. It does not argue against regulation. It argues for proportionate governance that preserves agency while addressing real harms.

## 2. Policy Method and Evidence Boundary

This article is a policy commentary. It does not report a survey, formal legal analysis, national adoption study, or empirical evaluation of AI outcomes. Its method is interpretive and design-informed: it reads current Australian AI policy against a bounded set of grassroots implementation patterns, then asks whether existing sovereignty language adequately protects practical participation outside major platforms and already-resourced institutions.

The evidence base has three parts. First, official Australian Government policy materials establish the current policy direction: opportunity, benefit-spreading, safety, public-sector governance, AI adoption guidance, the Office of AI, data-centre expectations, and the AI Safety Institute. Second, comparative policy frames supply pressure points around risk-tiered regulation, sectoral governance, market-led innovation, and platform concentration. Third, a local Australian project ecosystem supplies bounded existence-proof material: local-first tools, configurable model choice, hybrid provider lanes, offline classroom workflows, and model-host-task suitability testing.

The project evidence is not treated as national-scale validation. It supports a narrower claim: such grassroots capability exists and should remain practically lawful, inspectable, and governable. Claims about broad adoption, policy influence, classroom outcomes, accessibility outcomes, market impact, or legal compliance would require further evidence and are outside the scope of this commentary.

## 3. Current Australian Policy Context

The Australian Government's National AI Plan was released on 2 December 2025. It frames policy around three goals: capturing the opportunities of AI, spreading the benefits, and keeping Australians safe. The plan emphasizes smart infrastructure, domestic capability, global investment, widespread AI adoption, workforce skills, public services, legislative and regulatory frameworks, responsible practices, and international engagement.

Australia has also developed voluntary AI safety guidance and adoption guidance. The Voluntary AI Safety Standard sets out guardrails for organisations across the AI supply chain. The newer Guidance for AI Adoption, published through the National AI Centre, presents six essential practices for responsible AI governance and emphasizes accountability, impact understanding, risk management, information sharing, testing, monitoring, human oversight, and supply-chain controls. The Voluntary AI Safety Standard remains useful context, but the adoption guidance now provides a simplified implementation pathway for organisations.

The Australian Public Service also has a dedicated policy for the responsible use of AI in government. Version 2.0 is effective from 15 December 2025 and applies to non-corporate Commonwealth entities, with mandatory requirements for accountable officials, transparency statements, strategic AI adoption, responsible-use operations, use-case accountability, internal use-case registers, staff training, and AI use-case impact assessment.

Australia's institutional AI governance capacity is also changing. The Office of AI was established in the Department of the Prime Minister and Cabinet on 15 July 2026 to coordinate across Australian Government agencies, design and legislate a new Australian AI standard, address AI training in Australia, set mandatory requirements for large AI data centres, and support copyright protections for Australian creators. Australia's AI Safety Institute, part of the Department of Industry, Science and Resources, analyses emerging AI capabilities, risks, harms, and trends; tests new models and applications; supports regulators and agencies; and contributes to international AI governance.

This context matters because Australian policy is already trying to balance opportunity, safety, infrastructure, adoption, government use, copyright, and inclusion. The Fair-Go argument is not external to that effort. It is a proposed refinement: inclusion should not mean only access to systems chosen by major providers or institutions. Responsible AI should include the practical ability to use smaller, local, inspectable, and fit-for-purpose systems when they are sufficient.

## 3.1 Policy Gap: Capability for Whom?

The National AI Plan explicitly aims to ensure that everyone in Australia benefits from AI, across regions, industries, and communities. That goal raises a distributional question: what counts as participation?

Participation can mean being served by AI-enabled public services. It can mean being employed in an AI-enabled economy. It can mean using approved enterprise tools. But participation can also mean the practical ability to learn how systems work, run local models, test alternatives, build small tools, adapt workflows, inspect failures, and choose a host/model arrangement appropriate to one's own risk and purpose.

The Fair-Go position focuses on this latter form of participation. It treats capability as civic infrastructure, not only as a procurement or investment outcome.

## 4. Three Layers of Sovereignty

AI sovereignty is often discussed in terms of national hosting, compute, data centres, security, procurement, and domestic industry. These are important, but incomplete.

Hosting sovereignty means domestic infrastructure, compute, cloud, connectivity, energy, and data-centre capacity. A country that lacks infrastructure may depend on foreign systems for essential AI capability.

Institutional sovereignty means Australian agencies, universities, companies, standards bodies, and recognised organisations can research, procure, deploy, evaluate, and govern AI systems. A country without institutional capacity may lack expertise, coordination, and public-interest leverage.

Broad national capability sovereignty means Australians across the whole innovation spectrum can learn, inspect, run, adapt, evaluate, and build lawful AI systems. This includes independent builders, regional communities, disabled innovators, teachers, students, open-source maintainers, sole traders, small businesses, artists, researchers, and ordinary users.

The first two layers matter. The third is under-recognised. A nation is not fully sovereign in AI merely because large facilities exist on its soil or recognised institutions have procurement pathways. National capacity is national only if capability is distributed widely enough for people to participate, contest, adapt, and learn.

Broad capability sovereignty is also a safety issue. People who cannot inspect, compare, or choose tools are more dependent on provider claims. People who cannot run or test lawful alternatives are less able to verify whether a system is fit for their setting. Capability centralization can therefore reduce resilience even when framed as governance.

## 4.1 A Comparative Policy Frame

The Fair-Go framework does not require Australia to reject international AI governance. It requires Australia to translate international governance into a policy design that preserves proportionality and participation.

**Table 1. Comparative Policy Pressure Points**

| Policy frame | Main strength | Risk if imported too bluntly | Fair-Go adjustment |
|---|---|---|---|
| EU-style risk-tiered AI regulation | Clearer obligations for high-risk uses and providers. | Compliance burden may become hard for small actors, local tools, and open-source maintainers if categories are not carefully bounded. | Keep high-impact obligations strong, but preserve light-touch pathways for personal, local, research, educational, and small-scale lawful use. |
| UK-style pro-innovation sectoral governance | Flexibility and regulator-led adaptation. | Fragmentation or uncertainty can leave ordinary users unclear about rights, duties, and remedies. | Pair sectoral flexibility with plain user rights: transparency, contestability, portability, and scoped delegation. |
| US-style market and agency-led governance | Fast innovation and varied sectoral experimentation. | Platform power, procurement dependence, and uneven protections can grow if public-interest capacity is weak. | Build grassroots, public-interest, and local-first capability as part of national resilience. |
| Australian current trajectory | National AI Plan, AI Safety Institute, Office of AI, public-sector AI policy, adoption guidance, and data-centre/copyright work. | Sovereignty may be interpreted too narrowly as infrastructure, investment, institutional adoption, or large-platform partnership. | Add broad capability sovereignty as an explicit policy layer alongside hosting and institutional sovereignty. |

## 5. Enclosure-by-Compliance

AI regulation can accidentally create enclosure. This happens when compliance requirements, certification costs, infrastructure assumptions, vendor documentation burdens, or legal ambiguity make lawful participation practical only for the largest organisations.

The problem is not compliance itself. High-impact systems should carry serious obligations. Systems that affect rights, access, livelihood, education, health, safety, policing, migration, credit, or essential services should be accountable. The problem arises when all AI use is treated as though it were a high-impact institutional deployment.

A local personal assistant used by one person on their own device does not have the same social power as a platform-mediated hiring system. A teacher-controlled offline classroom support tool does not have the same risk profile as a cloud service profiling children at scale. A small model used for private note sorting does not have the same impact as automated eligibility assessment for public benefits.

If policy fails to preserve such distinctions, the likely outcome is not less AI. It is more dependence on major vendors that can absorb compliance costs, negotiate with government, and set defaults for everyone else. That is not sovereignty. It is regulated dependency.

## 6. Fit-for-Purpose Capability

The Fair-Go position begins with fit-for-purpose capability.

More capable is not always more appropriate. A frontier cloud model may be justified for advanced research, complex synthesis, or tasks requiring strong general reasoning. But a school spelling helper, local drafting tool, personal memory aid, or offline classroom assistant may be better served by a smaller model with limited permissions, no external connectivity, and clear human oversight.

Fit-for-purpose governance asks:

- What task is the system doing?
- Who is affected?
- What data is involved?
- What model capability is necessary?
- What host permissions are required?
- Can the task be done locally?
- When is cloud escalation justified?
- What evidence, audit, and appeal rights are needed?
- What happens if the system fails?

This approach aligns safety with restraint. A system should not collect more data, use more powerful models, connect to more services, or automate more decisions than the job requires. Capability should scale with need, and obligations should scale with power over others.

## 7. Local, Cloud, and Hybrid AI

The Fair-Go position does not treat local AI and cloud AI as ideological opponents. It treats them as different tools.

Local AI is valuable when privacy, offline access, cost control, inspectability, latency, experimentation, or limited capability is sufficient. It can support schools, personal tools, creative workflows, local research, small-business automation, and grassroots technical education.

Cloud AI is valuable when stronger capability, maintained infrastructure, specialized models, scalability, reliability, or collaboration justifies external processing and provider dependence.

Hybrid AI is valuable when users can deliberately escalate from local to cloud only when the task calls for it. A local assistant may use a small model for routine notes but route a difficult reasoning task to a cloud model after explicit user choice. An art tool may generate locally by default but offer optional cloud image lanes. A dataset tool may keep sensitive material local while allowing non-sensitive helper prompts through a configured provider.

The key is visibility and control. Users should know when data leaves the machine, which provider receives it, which model is used, what permissions are granted, and how to change or revoke that path.

## 8. BYO API-Key Lanes as User-Controlled Delegation

BYO API-key lanes are a practical pattern for hybrid sovereignty. The idea is simple: a tool remains local-first, but the user can add explicit cloud model entries through a host-owned settings surface. The user supplies provider details, model names, base URLs where relevant, and credentials. The application stores and verifies those settings, labels local and cloud lanes clearly, and routes only selected tasks through the selected provider.

This pattern is not a complete legal or security solution. Storage details matter: a system should say whether keys are encrypted, stored in an OS keychain, obscured, or plain text. The point is not to hide complexity. The point is to give users practical control without forcing them to edit configuration files or accept one vendor's default model.

The API-key lane materials in the local project ecosystem use a consistent stance: local first, cloud optional, user sovereignty over model choice. In one assistant stack, cloud lanes may support orchestration, logging functions, embeddings, or higher-capability fallback while day-to-day use remains local-first. In dataset and training-preparation tools, cloud helper lanes may assist captioning, tagging, prompt cleanup, or dataset QA while training and dataset ownership remain local. In media tools, optional cloud media models may supplement local generation without replacing the local-first identity of the tool.

The governance value is that capability escalation becomes explicit. The system can show what data leaves the machine when cloud is selected, provide clear failure messages, avoid silent provider lock-in, and let users change models without manual file editing.

## 9. Evidence from Grassroots Infrastructure

The local project corpus is not national-scale proof. It does not demonstrate adoption, classroom outcomes, policy influence, or platform-level delegated access. It is better understood as an existence proof: independent Australian builders can produce meaningful AI infrastructure that reflects public-interest design values.

Relevant demonstrated patterns include:

- Model-agnostic local tools that allow user-supplied or configurable models.
- Local/cloud hybrid choice in assistant tools.
- Local-only educational design in a classroom assistant, where offline operation and teacher authority are proportionate restraints.
- Model-host-task suitability testing through a dedicated test chamber.
- Local semantic dataset sorting with auditable outputs.
- Accessible local builder workflows for corpus preparation, tokenizer work, training, and checkpoint testing.
- Human-directed collaboration patterns with explicit approvals, sandbox boundaries, and local storage.

These examples should not be overstated. Some are working software, some are partial implementations, some are design directions, and some are policy proposals. The important claim is narrower: grassroots capability exists, and policy should avoid regulating it out of practical reach.

The internal evidence base should be read as a structured existence proof, not as national-scale evaluation. The supporting evidence materials explicitly separate demonstrated claims from partial, directional, and proposed claims. Table 2 preserves that evidence boundary.

**Table 2. Evidence Signals for Broad Capability Sovereignty**

| Evidence category | Repository signal | Policy relevance | Boundary |
|---|---|---|---|
| Demonstrated | Configurable local assistant, education, dataset, and suitability-testing tools use user-supplied or configurable models. | Model choice can be made practical outside a single vendor default. | Does not prove broad public adoption. |
| Demonstrated | Assistant tools show local-first or hybrid local/cloud model selection. | Hybrid choice can be explicit rather than hidden behind platform defaults. | Requires careful key storage, routing disclosure, and failure handling. |
| Demonstrated | A classroom assistant uses local-only school workflows, teacher-authored homework, teacher locks, revision boundaries, and local evidence artifacts. | Some sensitive settings may need less connectivity and more human authority, not more automation. | Does not establish classroom learning outcomes. |
| Demonstrated | A model-host-task suitability test chamber evaluates suitability by model, host, task, and failure mode. | Governance should assess context fit rather than rank models abstractly. | Needs expansion before becoming a public standard. |
| Partly demonstrated | Training-preparation, dataset, and curriculum-scaffold tools support learning, local experimentation, and telemetry discipline. | Technical literacy and experimentation are sovereignty infrastructure. | Educational impact and public uptake remain future claims. |
| Policy proposal | Vendor-neutral assistive delegation across external platforms. | Disabled users and ordinary users need scoped, revocable, auditable delegation rights. | The local ecosystem demonstrates adjacent patterns, not full platform-level implementation. |

## 10. Assistive Delegation and Accessibility

Broad capability sovereignty has special importance for disabled users and people with uneven access to institutional support. AI tools can function as assistive infrastructure: reading support, writing support, memory support, planning support, interface mediation, document navigation, communication support, and routine administrative help.

But assistive usefulness depends on control. A user should be able to authorise a tool to access information they are already entitled to access, within scoped, revocable, auditable boundaries. They should be able to choose a local model for private work, a cloud model for hard tasks, or a hybrid arrangement that fits their needs.

The unresolved ecosystem gap is platform-level, vendor-neutral assistive delegation. Many platforms do not provide a clean way for users to delegate narrowly scoped access to third-party AI assistants under user control. As a result, users may be pushed toward either manual friction or all-or-nothing platform ecosystems.

This paper treats user-selected assistive delegation as a policy proposal, not as a capability already solved by current platforms. It should be developed through standards, interoperability requirements, consent mechanisms, audit trails, and revocation rights.

## 11. Proportionate Governance Model

A Fair-Go governance model should scale obligations according to actual use, power, and impact. Relevant variables include:

- Model capability.
- Host permissions.
- Connectivity.
- Data sensitivity.
- Population affected.
- Scale and reach.
- Degree of automation.
- Whether decisions affect rights or essential services.
- Whether humans can review, appeal, or override.
- Whether the system is personal, organisational, or public-facing.
- Whether the user is experimenting, assisting themselves, serving others, or exercising power over others.

This model supports strong duties for high-impact systems. It also preserves space for personal local tools, educational experiments, assistive workflows, open-source development, and small-business use where risks are bounded.

The regulatory aim should be to control harmful conduct and high-impact deployment, not to make ordinary lawful AI tinkering impossible. A useful distinction is between systems used by people and systems used on people. Personal tools still need safety and privacy discipline, but systems that affect others at scale should carry heavier obligations.

**Table 3. Proportionate Governance Variables**

| Variable | Lower-obligation indicators | Higher-obligation indicators |
|---|---|---|
| User relationship | Personal use, self-assistance, local experimentation. | System used on other people or populations. |
| Domain impact | Low-stakes drafting, learning, sorting, personal organization. | Rights, access, livelihood, education, health, safety, policing, migration, credit, or essential services. |
| Scale and reach | Single user, local device, small bounded group. | Large population, public service, market-wide platform, or automated public-facing service. |
| Data sensitivity | Non-sensitive or user-controlled data. | Children, health, disability, biometrics, financial, legal, workplace, or protected-characteristic data. |
| Host permissions | No external network, no autonomous action, explicit user approval. | Tool access, account access, autonomous action, external publication, or irreversible transactions. |
| Model and system capability | Narrow task support, small model, limited context, local host. | General-purpose, frontier, agentic, multimodal, tool-using, or self-extending systems. |
| Contestability | User can review, edit, delete, refuse, or override. | Affected person cannot see, challenge, appeal, or correct the decision. |

## 12. Policy Recommendations

Australia should preserve lawful access to local, open-weight, commercial, and hybrid AI systems while applying stronger obligations where systems exercise power over other people.

It should distinguish personal tools, classroom tools, assistive technologies, research prototypes, internal business tools, public-facing services, and automated decision systems.

It should support interoperability and portability for AI workflows, memory, settings, model choice, and assistive configurations where safe and lawful.

It should encourage user-controlled model selection, including local-first and BYO-provider patterns, rather than assuming one approved model family or cloud provider can fit every context.

It should include grassroots builders, disabled users, educators, small businesses, regional communities, and open-source maintainers in AI policy formation.

It should treat AI literacy and technical education as sovereignty infrastructure, not merely workforce training.

It should require transparency about when data leaves a user's device, which provider receives it, what model is used, what permissions are granted, and how those permissions can be revoked.

It should develop standards for scoped assistive delegation so users can authorise tools to act on information they are already entitled to access without surrendering broad control to platform defaults.

It should preserve proportionality: strong accountability for high-impact deployment, light-touch pathways for bounded personal and local use, and clear escalation rules for hybrid systems.

**Table 4. Policy Recommendation Matrix**

| Recommendation | Policy action | Why it matters |
|---|---|---|
| Name broad capability sovereignty. | Add grassroots, regional, disability, education, small-business, and open-source capability to national AI policy language. | Prevents sovereignty from being reduced to data centres, procurement, and enterprise adoption. |
| Preserve lawful model/host choice. | Protect access to local, open-weight, commercial, and hybrid systems subject to proportionate duties. | Keeps policy from making one provider or architecture the practical default for everyone. |
| Scale duties by use and power. | Distinguish personal tools, assistive tools, classroom tools, prototypes, internal business systems, public services, and automated decisions. | Targets harms without enclosing ordinary lawful use. |
| Require data-path transparency. | Require clear disclosure when data leaves a device, which provider receives it, and what model or system is used. | Makes hybrid escalation visible and contestable. |
| Support scoped assistive delegation. | Develop standards for revocable, auditable, user-controlled delegation across services. | Helps disabled users and ordinary users delegate safely without surrendering broad platform control. |
| Fund practical AI literacy. | Treat local model use, evaluation, failure inspection, and workflow design as civic and workforce skills. | Builds resilience outside already-resourced institutions. |
| Include grassroots evidence in consultation. | Create low-friction consultation channels for independent builders, disabled users, educators, small businesses, and regional communities. | Reduces policy capture by those already able to attend the table. |
| Preserve open/public-interest infrastructure. | Support open-source, commons-oriented, and public-interest AI tooling where lawful and safe. | Strengthens contestability, learning, and non-platform pathways. |

## 13. Risks and Limitations

The Fair-Go position has risks.

First, local and open systems can be misused. Preserving access does not mean ignoring harmful conduct, malware, abuse material, fraud, harassment, privacy invasion, or unsafe deployment.

Second, "user choice" can become a slogan if users lack real understanding or if interfaces hide consequences. Model selection, cloud routing, and data-sharing choices must be legible.

Third, compliance proportionality is hard. Too little obligation can leave people exposed. Too much obligation can enclose the field. Policy must iterate.

Fourth, grassroots capability is uneven. Not every user can safely configure models, manage keys, or evaluate outputs. Education, defaults, and tool design matter.

Fifth, local-first design is not automatically private or secure. Storage, telemetry, key handling, sandboxing, and update mechanisms must be specified.

Sixth, the evidence base here is partial. The project examples demonstrate design patterns and working prototypes, not national outcomes.

## 14. What This Paper Is Not Claiming

This paper is not anti-regulation. It supports strong governance for high-impact, coercive, deceptive, privacy-sensitive, safety-critical, and large-scale systems.

It is not anti-business. Commercial AI services are part of a healthy ecosystem.

It is not a demand for unbounded autonomous agents.

It is not a claim that local, open, or hybrid systems carry no risk.

It is not a claim that the project examples prove national adoption, classroom outcomes, platform-level delegation, or policy influence.

It is not a legal opinion.

It is a call for AI policy to match obligations to actual use, power, and impact while preserving practical participation.

## 15. Conclusion

Australia's AI future should not be reduced to a choice between platform dependency and blanket control. A better path is proportionate, plural, and capability-building.

Hosting sovereignty matters. Institutional sovereignty matters. But broad national capability sovereignty matters too. Australians should be able to learn, inspect, run, adapt, evaluate, and build lawful AI tools without needing permission from a platform, accelerator, university, vendor, or agency before they can participate.

The Fair-Go position is simple: fit the tool to the job, give it only what that job requires, and keep the human in charge. That principle supports both safety and agency. It just refuses to solve concentration by concentrating permission.

## Disclosure Statements

Acknowledgments: The author used OpenAI ChatGPT and OpenAI Codex to assist with drafting, structuring, policy-source checking, reference checking, and document preparation. The author reviewed and revised the manuscript and accepts responsibility for the final content.

Data availability: This commentary relies on public Australian Government policy materials, public journal author-instruction pages, and a bounded local project evidence map. No empirical dataset, participant data, classroom deployment data, or legal case dataset is reported.

Funding: This work received no specific grant from any funding agency, commercial, or not-for-profit sectors.

Competing interests: The author developed and maintains the local project ecosystem used as implementation evidence. No financial competing interests are declared.

## References

Australian Government Department of Industry, Science and Resources. (2025). National AI Plan. Released 2 December 2025. https://www.industry.gov.au/publications/national-ai-plan

Australian Government Department of Industry, Science and Resources. (2025). Voluntary AI Safety Standard. Updated 2 December 2025. https://www.industry.gov.au/publications/voluntary-ai-safety-standard

Australian Government. (2026). Guidance for AI adoption: implementation guidance. https://www.ai.gov.au/staying-safe-and-responsible/essential-ai-practices/guidance-ai-adoption-implementation-guidance

Australian Government Department of Industry, Science and Resources. (2026). Australia's AI Safety Institute. https://www.industry.gov.au/science-technology-and-innovation/technology/artificial-intelligence/ai-safety-institute

Australian Government Department of Industry, Science and Resources. (2026). Expectations of data centres and AI infrastructure developers. https://www.industry.gov.au/publications/expectations-data-centres-and-ai-infrastructure-developers

Australian Government Department of Industry, Science and Resources. (2024). Introducing mandatory guardrails for AI in high-risk settings. Consultation opened 5 September 2024 and closed 4 October 2024. https://consult.industry.gov.au/ai-mandatory-guardrails

Australian Government Department of Industry, Science and Resources. (2025). Australia to establish new institute to strengthen AI safety. https://www.industry.gov.au/news/australia-establish-new-institute-strengthen-ai-safety

Australian Government Department of Industry, Science and Resources. (2026). Artificial intelligence. https://www.industry.gov.au/science-technology-and-innovation/technology/artificial-intelligence

Australian Government. (2026). Australian Government response to the Senate Select Committee on Adopting Artificial Intelligence report. Published 1 April 2026. https://www.industry.gov.au/publications/australian-government-response-senate-select-committee-adopting-artificial-intelligence-ai-report

Cambridge University Press. (2026). Data & Policy: Preparing your materials. https://www.cambridge.org/core/journals/data-and-policy/information/author-instructions/preparing-your-materials

Cambridge University Press. (2026). Data & Policy: Open access options. https://www.cambridge.org/core/journals/data-and-policy/information/journal-policies/open-access-options

Department of the Prime Minister and Cabinet. (2026). Office of AI. https://www.pmc.gov.au/domestic-policy/office-ai

Digital Transformation Agency. (2025). Policy for the responsible use of AI in government: Version 2.0. https://www.digital.gov.au/ai/ai-in-government-policy

Parliament of Australia. (2026). Senate Environment and Communications References Committee: Artificial intelligence and data centres. Submissions listed as closing 1 September 2026. https://www.aph.gov.au/Parliamentary_Business/Committees/Senate/Environment_and_Communications/AIdatacentres48P
