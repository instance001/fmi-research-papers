# Offline-First Classroom AI as Proportionate Restraint

## A Design Study of Local Tutoring, Teacher Authority, and Evidence-Preserving Learning Workflows

## Abstract

Generative AI in education is often framed around cloud-scale personalization, automated feedback, and institutional platform adoption. This paper argues for a complementary design pattern: offline-first classroom AI as proportionate restraint. In this model, the educational assistant runs on school-controlled hardware, uses locally supplied models, requires no student accounts or cloud services, keeps homework and revision data as local files, and preserves teacher authority through explicit locks, review surfaces, and governed workflows. The aim is not to maximize automation, but to make the tool fit the educational setting. Drawing on two implementation-adjacent projects, the paper presents an implementation-informed design study for local AI support in schools. The classroom-facing case illustrates offline local inference, teacher-authored homework packs, hints-over-answers guardrails, tamper-evident submissions, local memory surfaces, optional LAN-only peer sharing, and visible activity cues. The companion research scaffold provides a curriculum and telemetry structure for studying transfer, boundary pressure, refusal, skill governance, and cautious evidence interpretation. The paper positions offline-first AI as a trust boundary, not merely a technical constraint. It proposes evaluation criteria for privacy, teacher control, student dignity, hint quality, revision support, workflow continuity, auditability, and local deployment feasibility. The argument is not that local systems are automatically safer or educationally effective, but that education AI governance should recognize bounded local architectures as a legitimate design response to privacy, child protection, teacher oversight, and proportionality.

Keywords: AI in education; local-first AI; classroom technology; teacher authority; student privacy; tutoring systems

## 1. Introduction

Education is one of the most sensitive settings for generative AI. Schools work with children, families, teachers, learning records, disability needs, assessment pressures, institutional accountability, and uneven technical capacity. AI systems in this environment should not be judged only by capability. They should be judged by fit.

The guiding question for this paper is: what kind of AI architecture is proportionate for ordinary classroom support?

One common answer is cloud platform adoption. Schools use centrally hosted systems that provide strong models, managed infrastructure, analytics, content generation, and integration with institutional accounts. These systems can be useful, but they also concentrate data flows, provider dependence, procurement complexity, and governance questions.

Another answer is blanket restriction. Schools may ban or heavily limit AI tools because of privacy, cheating, inappropriate content, surveillance, equity, or teacher workload concerns. These concerns are real, but blanket restriction can leave students and teachers without safe ways to learn AI literacy or benefit from bounded assistance.

This paper proposes a middle lane: offline-first classroom AI as proportionate restraint. The premise is that not every school AI task needs a frontier cloud model, external account system, or centralized analytics layer. Some tasks can be supported by smaller local models, teacher-authored materials, local file storage, explicit review, and deliberate constraints.

The paper draws on an offline, local-first learning assistant for schools and a companion research rig for controlled curriculum and telemetry experiments. The contribution is a design framework rather than a classroom-outcomes claim. The classroom prototype is treated as an implementation-informed case for how local architecture can encode privacy, teacher authority, homework integrity, and student dignity. The research rig is treated as a companion scaffold for cautious study of learning, transfer, anomaly, and boundary behavior.

## 2. Design-Study Method and Claim Boundary

This article is a design study of an implementation-informed educational AI architecture. It does not report a classroom deployment, student participant dataset, or learning-outcomes trial. Its evidence base consists of source materials, manuals, workflow definitions, privacy statements, and implementation artifacts from a local-first classroom AI project ecosystem. These materials are used to analyze what the architecture is designed to make possible, visible, difficult, or governable.

The method is therefore architectural and interpretive rather than experimental. The paper identifies the educational problem space, describes the design constraints, maps concrete workflow artifacts to governance and pedagogy claims, and derives evaluation criteria for future classroom or pre-classroom study. This is an appropriate first contribution where the claim is that a design pattern belongs in the AIED vocabulary, not that the pattern has already improved learning outcomes.

The claim boundary is strict. The paper argues that offline-first classroom AI can encode proportionate restraint through local data paths, teacher-authored workflows, audience-separated memory, hints-over-answers support, post-submission revision, and inspectable evidence artifacts. It does not claim certified compliance, pedagogical superiority, child-safety certification, or general effectiveness across subjects, schools, models, or jurisdictions.

## 3. Education AI Governance Context

International guidance on generative AI in education emphasizes human-centered deployment, data privacy, equity, teacher involvement, age-appropriate safeguards, human oversight, and AI literacy. UNESCO's 2023 guidance on generative AI in education and research calls for policies that protect human agency, inclusion, equity, privacy, and cultural diversity while building capacity for responsible use. UNICEF's work on AI for children emphasizes child-centered design and governance. OECD education and AI materials emphasize the need to understand how AI complements human skills and how education systems should respond while preserving safety, trust, accountability, and teacher judgment.

Peer-reviewed AIED and learning-analytics literature points in a compatible direction. Reviews of AI in education have repeatedly identified intelligent tutoring systems, assessment, learner modeling, adaptive support, and analytics as central application areas, while also noting gaps between technical development and educational participation (Holmes et al., 2019; Zawacki-Richter et al., 2019). Work on LLMs in education emphasizes both practical opportunities and risks for students and teachers (Kasneci et al., 2023). Teacher-AI complementarity research shows why classroom AI should support teacher orchestration rather than replace professional judgment (Holstein et al., 2019; Holstein et al., 2022). Learning-analytics ethics research further foregrounds privacy, transparency, agency, consent, access, and data ownership as design concerns rather than afterthoughts (Pardo & Siemens, 2014).

These themes are directly relevant to local-first classroom AI. If educational AI should preserve human agency, protect student data, support teachers, avoid inappropriate automation, and build practical literacy, then architecture matters. A system's privacy posture is not only a policy promise. It is shaped by whether the tool requires cloud calls, accounts, remote logging, centralized analytics, persistent profiles, external identity systems, or vendor-controlled model selection.

Offline-first design does not automatically solve educational AI governance. A local system can still be poorly designed, biased, insecure, misleading, or pedagogically weak. But it changes the control surface. Data can remain on school devices. Teachers can author and inspect materials. Model use can be limited. Connectivity can be optional rather than default. Student-facing analytics can be restrained.

This makes offline-first AI a governance architecture, not just an implementation choice.

## 4. Design Principle: Fit the Tool to the Classroom

The core design principle is:

Fit the tool to the job. Give it only what that job requires. Keep the human in charge.

For classroom AI, this means capability should be matched to educational purpose, student age, privacy sensitivity, teacher oversight, assessment context, and institutional capacity.

A homework hint helper does not need the same permissions as a school-wide analytics platform. A revision explainer does not need to expose raw teacher diagnostic labels to students. A classroom device does not need internet access merely to help a student read a teacher-authored worksheet. A model helping draft a lesson pack does not need permanent authority over assessment records.

Fit-for-purpose classroom AI should distinguish:

- live homework support from post-submission revision;
- hints from final answers;
- teacher tools from student tools;
- local classroom sharing from cloud synchronization;
- session context from persistent memory;
- assistive feedback from grading authority;
- visibility into app activity from surveillance of students.

These distinctions are central to the classroom prototype's design.

## 5. Classroom Prototype as Implementation-Oriented Case

The classroom prototype is an offline, local-first school assistant. It is designed to run on school hardware, use local GGUF models supplied by the school or user, and require no accounts or cloud services in normal operation. Model weights are not shipped; schools bring approved models into the local `models` folder. The app scans available local models and assigns roles, such as main chat and optional teacher-log support.

The system stores ordinary working data as local files under a configurable base directory. Homework packs, submissions, printables, rubrics, revision notes, model settings, and teacher-log summaries remain on the device or school-controlled storage. The app has no telemetry, analytics service, third-party logging, or remote kill switch in the described configuration.

The prototype includes teacher-facing and student-facing surfaces. Teachers can author homework packs in Markdown, transcribe them into JSON, export student printables and rubrics, convert submissions to marking sheets, and control settings behind a teacher PIN. Students can load assignments, see handouts and text attachments, submit work, and ask for help.

The strongest design feature is not merely that the model runs locally. It is that the AI is embedded in a governed classroom workflow. Live homework questions are intercepted and steered toward hints rather than direct answers. Revision is separated from live homework and can be more explanatory because the work has already been submitted. Teacher-side scores or diagnostic labels are hidden from the student revision view. Submissions include hash-chained event logs for lightweight tamper-evidence.

This makes the system a case of proportionate educational restraint. The architecture does less than a cloud platform could do, and that is part of the point.

The implementation materials give the design claim a concrete basis rather than only a normative framing. Table 1 maps the main paper claims to implementation-backed design signals.

**Table 1. Implementation Evidence Signals in the Classroom Prototype**

| Design claim | Implementation-backed signal | Submission posture |
|---|---|---|
| Local-first tutoring can reduce routine data exposure. | The implementation materials describe a Rust/egui desktop and CLI application that runs offline with user-supplied GGUF models, local folders, no bundled model weights, and no normal-use cloud telemetry or analytics. | Treat as an architecture and workflow claim, not as an audited privacy certification. |
| Teacher authority can be encoded into ordinary workflow. | Teacher-authored homework packs, printable exports, rubrics, marking-sheet conversion, model/settings controls, and a teacher PIN gate separate teacher actions from student-facing use. | Present as inspectable design structure; note that the PIN is a UI gate rather than hardened authentication. |
| Homework help can prefer hints over answer dumping. | Homework-aware chat guardrails intercept active assignment questions and steer the response toward Socratic hints instead of final answers. | Frame as a design intervention requiring empirical evaluation of bypasses, hint quality, and student learning effects. |
| Revision can be more explanatory without exposing teacher judgments. | The revision workspace uses completed homework and past-paper material while hiding teacher-side scores and diagnostic labels from students. | Connect to student dignity and feedback design rather than automated grading. |
| Submissions can preserve lightweight evidence without platform telemetry. | Submission JSON files include attachments, local event logs, hash-chained events, and a final hash. | Describe as local tamper-evidence, not cryptographic identity proof. |
| Local memory surfaces can be differentiated by audience and duration. | Session thoughts are current-session context; the memory jogger is a persistent recent-memory summary; teacher logs are local search behind the teacher lock. | Use as an example of memory minimization and audience separation. |
| Visibility can support trust without becoming surveillance. | The ECG-style activity window is described as a cue that local work is happening, not as user monitoring. | Treat as a transparency affordance that should be user-studied. |

## 6. Offline-First as Trust Boundary

Offline-first design creates a trust boundary that schools, parents, students, and teachers can understand. In normal use, prompts and responses are processed on the same machine. Homework and submission data remain in local files. No external service is required for the core workflow.

This is not a claim of perfect security. Local files still need OS permissions, device management, backups, disk encryption, endpoint protection, and school-side controls. Teacher PINs are UI gates, not hardened security boundaries against someone with filesystem access. Hash-chained submissions are tamper-evident signals, not cryptographic identity guarantees.

The value is proportionality and legibility. A school can reason about the data path. A teacher can inspect files. A parent can be told that ordinary prompts are not sent to a vendor. A student can use the tool without creating another account.

The prototype also includes an ECG-style visible activity indicator. It reads local machine activity and is described as a transparency cue, not as user surveillance or network auditing. Its purpose is modest but symbolically important: make local work visible rather than asking users to trust an opaque background process.

## 7. Teacher Authority and Student Dignity

The design intent of the classroom prototype is to reduce shame, judgment, and unnecessary pressure while supporting early, dignity-preserving intervention. It is explicitly not designed for staff evaluation, student ranking, permanent profiling, discipline, surveillance, or parental pressure.

This boundary matters because AI education systems can easily slide from support into monitoring. A tool that begins as a tutor can become a scoring engine. A dashboard that begins as teacher support can become performance management. A revision assistant can reveal labels to students in ways that shape self-concept or increase pressure.

The prototype's teacher boundary keeps private professional judgment with teachers. Its student boundary emphasizes hints, learning support, and revision without exposing raw diagnostic labels. Its parent boundary frames the system as learning support rather than a monitoring mechanism.

This is an important design claim: student dignity is not just a content-filtering issue. It is an architectural and workflow issue. What data is stored, who sees it, how labels are displayed, whether scores are hidden or surfaced, whether the system hints or answers, and whether logs are used for support or surveillance all shape the moral character of the tool.

## 8. Homework, Revision, and Evidence Artifacts

The prototype separates homework, submission, marking, printable, rubric, and revision workflows into explicit local artifacts.

Homework packs can be authored as Markdown and transcribed to JSON. A pack includes assignment metadata, instructions, optional student printable material, teacher rubric, game settings, scoring limits, and attachments. Students export submission JSON containing answers, attachments, optional AI premark material, a hash-chained event log, and a final hash. Teachers can convert submissions into Markdown marking sheets and export printables or rubrics.

Revision is separate from live homework. It can use completed submissions and past papers, but student-facing revision hides teacher-side scores and diagnostic labels. This design allows more open explanation after submission while preserving live homework guardrails during active assignments.

These artifacts matter for research as well as school workflow. They make it possible to study how AI support affects hint-seeking, answer revision, teacher workload, submission integrity, and feedback cycles without relying on hidden platform telemetry.

The core classroom workflow can be summarized as Figure 1: teacher-authored homework packs become local assignment files; students work in the local app; active homework questions pass through a hints-over-answers guardrail; submissions preserve local evidence artifacts; teachers review and mark completed work; post-submission revision reopens explanation while hiding teacher-side scores and diagnostic labels; memory and teacher-log surfaces remain locally separated by audience and duration.

**Figure 1. Offline-first classroom workflow.** The workflow moves from teacher-authored homework material to local student work, guarded hints, local submissions, teacher review, and post-submission revision. Ordinary operation does not require student accounts, cloud telemetry, or centralized analytics.

## 9. Modules, Sandbox, and Local Peer Sharing

The classroom prototype also supports a modular local workflow. Drop-in modules can provide specialized lesson planning, revision sprinting, teacher notebooks, or other educational tools. Modules can run as hosted tabs with status bridges and log surfaces, allowing the main AI to carry context across planning, review, and refinement.

The local sandbox provides a governed working area for longer tasks. It includes a scratchpad and task ledger. File actions are approval-gated rather than silently executed. This pattern helps keep multi-step teacher or student work grounded while preserving user control.

Optional peer networking allows nearby classroom-assistant instances to connect over local Wi-Fi or LAN. It is off by default, limited to trusted classroom peers, and used for handoff notes, homework packs, revision packs, and classroom setup bundles. Received materials land in inboxes before deliberate application. This is local classroom sharing, not cloud sync.

These features support workflow continuity without turning the tool into a centralized platform. The system can help teachers draft, test, review, refine, and hand off materials while keeping the process local and inspectable.

## 10. Companion Research Scaffold

The companion research scaffold is not a classroom product. It is a standalone research rig for studying deterministic MCM behavior inside a controlled curriculum scaffold. Its inclusion here matters because education AI needs evidence disciplines that do not overclaim.

The scaffold separates the deterministic student from the LLM teacher. The MCM student answers through deterministic, inspectable logic paths using explicit memory, skill governance, policy checks, refusal behavior, and trace output. The LLM teacher can generate curriculum drafts, examples, feedback, remediation suggestions, transfer probes, and summaries, but it does not answer on the simulated student's behalf or write into the simulated student's memory.

This architecture preserves a useful lesson for classroom AI: the system should distinguish proposal from authority. A stochastic model can propose material. A deterministic or governed runtime can preserve traces. A human operator can approve, interpret, and decide.

The scaffold's curriculum schema includes teaching items, near-transfer probes, far-transfer probes, cross-representation probes, composition probes, boundary probes, and open-structure probes. Its telemetry schema preserves interactions, teacher calls, MCM traces, memory events, skill events, refusal events, anomaly events, analysis reports, and session summaries. Its alignment doctrine requires provisional language, anomaly preservation, and human review over overclaiming.

This research posture complements the classroom prototype's practical posture.

## 11. Evaluation Criteria

An offline-first classroom AI system should not be evaluated only by answer accuracy. A suitable evaluation program should include:

- Privacy and data minimization: what leaves the device, what is stored, and who can access it.
- Teacher authority: whether teachers retain control over assignments, settings, review, and interpretation.
- Student dignity: whether the tool avoids ranking, shaming, surveillance, and premature diagnostic labeling.
- Hint quality: whether live homework support teaches steps without dumping final answers.
- Revision usefulness: whether post-submission support helps students understand errors and improve.
- Workflow continuity: whether teachers and students can move between planning, homework, chat, revision, and modules without losing context.
- Auditability: whether submissions, premarks, memory summaries, logs, and exports are inspectable.
- Local deployment feasibility: whether schools can install, configure, and maintain the tool on ordinary hardware.
- Safety boundaries: whether content filters, teacher locks, local networking controls, and sandbox approvals behave as documented.
- Learning outcomes: whether use improves understanding, transfer, confidence, or teacher feedback cycles.

The last category is important but should not be claimed without study. A v0.1 design paper can responsibly argue that the architecture supports better governance and evaluation; it cannot claim improved learning outcomes without classroom evidence.

## 12. Future Evaluation Agenda

The present article does not require new empirical work to support its architectural claim. The appropriate empirical next step is a staged evaluation program that tests whether the proposed boundaries are understood, usable, pedagogically meaningful, and robust enough for real educational settings.

A first future study could be a design evaluation with teachers, school IT staff, parents, and students. It would assess whether participants understand the offline boundary, trust the data flow, find teacher controls usable, and see the hints-over-answers design as pedagogically appropriate.

A second future study could compare homework support conditions: no AI help, unrestricted cloud chatbot help, and prototype-style hints-only local help. Outcomes could include completion quality, evidence of reasoning, help-seeking behavior, inappropriate answer copying, student confidence, teacher marking time, and revision uptake.

A third future study could evaluate privacy and deployment. School IT staff could install the tool, inspect data paths, verify no ordinary cloud calls, configure models, test local networking, and review deletion or retention procedures.

A fourth future study could use scaffold-style telemetry in a non-student research setting to study curriculum transfer, boundary handling, refusal behavior, and anomaly preservation before similar claims are made in classrooms.

All studies involving students would need appropriate ethics review, consent, minimization of personal data, and careful attention to power relationships in classrooms.

Table 2 is not a pre-submission requirement for the present conceptual design article. It identifies useful future validation paths that would convert the architecture paper into an empirical follow-up.

**Table 2. Future Evaluation Paths**

| Evaluation path | Participants or materials | Main question | Evidence produced |
|---|---|---|---|
| Teacher workflow review | Teachers inspect homework authoring, hint behavior, marking exports, and revision views. | Does the workflow preserve teacher authority while reducing avoidable burden? | Usability notes, task-completion times, teacher trust ratings, qualitative concerns. |
| Student-facing comprehension review | Age-appropriate student participants or adult proxies inspect homework and revision flows. | Are hint boundaries, revision feedback, and hidden diagnostic labels understandable and dignity-preserving? | Comprehension checks, perceived pressure/trust ratings, examples of confusing wording. |
| School IT privacy walk-through | IT staff install the app, inspect folders, configure models, and test network-off use. | Is the local data path legible and operationally feasible for ordinary school environments? | Install notes, data-flow checklist, local-file inventory, network/offline observations. |
| Homework-support comparison | No AI help, unrestricted chatbot help, and prototype-style hints-only local help. | Does bounded local help change copying, reasoning evidence, confidence, or teacher marking time? | Submission artifacts, rubric scores, help-seeking traces, teacher workload measures. |
| Pre-classroom research probe | Non-student curriculum/telemetry experiments using deterministic MCM and logged LLM teacher calls. | Which curriculum-transfer or boundary behaviors should be studied before classroom claims are made? | Probe logs, anomaly clusters, candidate next-study questions, caution notes. |

## 13. Risks and Limitations

Offline-first classroom AI has limitations.

Local models may be weaker than cloud models. They may produce lower-quality explanations, handle fewer topics, or require careful model selection. Schools with limited hardware may face performance problems.

Local deployment shifts responsibilities to schools. Device security, backups, permissions, updates, and model licensing must be managed.

Content filters are imperfect. An offline filter can reduce risk but cannot guarantee safe responses.

Teacher PINs and local file boundaries are not complete security systems. They must be paired with OS-level controls and school policy.

Hints-over-answers guardrails can fail. Students may phrase questions around them, and models may still give too much away.

Local-first design does not automatically produce good pedagogy. It only creates a more governable environment in which pedagogy can be designed and studied.

Finally, the classroom prototype is an implementation-informed case, not proof of educational effectiveness. Classroom outcomes require empirical evaluation.

## 14. What This Paper Is Not Claiming

This paper does not claim that the classroom prototype improves learning outcomes. It proposes a design architecture and evaluation agenda.

It does not claim that local AI is always safer than cloud AI.

It does not claim that schools should avoid all cloud tools.

It does not claim that local models are unbiased, reliable, or sufficient for every classroom.

It does not claim that teacher dashboards should become surveillance systems.

It does not claim that the companion research scaffold is an education product or student tutor.

It does not claim certified compliance with any jurisdiction's education, privacy, child-safety, or accessibility law.

## 15. Conclusion

Education AI should be judged by fit, not only by capability. A classroom assistant does not automatically become better by using a stronger model, collecting more data, adding accounts, or centralizing analytics. In some settings, restraint is a feature.

Offline-first classroom AI offers one way to encode that restraint. It can keep data local, avoid accounts, preserve teacher authority, separate homework from revision, prefer hints over answer dumping, expose workflow artifacts, and make activity visible to the people in the room.

The classroom prototype demonstrates this architecture as a local-first school assistant. The companion research scaffold adds a research discipline for curriculum, telemetry, anomaly preservation, and cautious analysis. Together, they support a practical claim: responsible education AI should include small, local, inspectable systems in its design vocabulary.

The goal is not to make AI the classroom authority. The goal is to give teachers and students a governed tool that helps without taking over.

## Declaration of Generative AI and AI-Assisted Technologies in the Manuscript Preparation Process

During the preparation of this work, the author used OpenAI ChatGPT and OpenAI Codex to assist with drafting, structuring, literature-targeting, and document preparation. After using these tools, the author reviewed and edited the content as needed and takes full responsibility for the content of the published article.

## References

Elsevier. (2026). Generative AI policies for journals. https://www.elsevier.com/about/policies-and-standards/generative-ai-policies-for-journals (accessed 5 September 2026).

Holmes, W., Bialik, M., and Fadel, C. (2019). Artificial Intelligence in Education: Promises and Implications for Teaching and Learning. Center for Curriculum Redesign.

Holstein, K., McLaren, B. M., and Aleven, V. (2019). Co-designing a real-time classroom orchestration tool to support teacher-AI complementarity. Journal of Learning Analytics, 6(2), 27-52. https://doi.org/10.18608/jla.2019.62.3

Holstein, K., McLaren, B. M., and Aleven, V. (2022). Designing for human-AI complementarity in K-12 education. AI Magazine, 43(2), 239-248. https://doi.org/10.1002/aaai.12058

International Journal of Artificial Intelligence in Education. (2026). Guide for authors. ScienceDirect. https://www.sciencedirect.com/journal/international-journal-of-artificial-intelligence-in-education/publish/guide-for-authors (accessed 5 September 2026).

International Journal of Artificial Intelligence in Education. (2026). Journal page and legacy scope statement. Springer. https://link.springer.com/journal/40593 (accessed 5 September 2026).

Kasneci, E., Sessler, K., Küchemann, S., Bannert, M., Dementieva, D., Fischer, F., Gasser, U., Groh, G., Günnemann, S., Hüllermeier, E., Krusche, S., Kutyniok, G., Michaeli, T., Nerdel, C., Pfeffer, J., Poquet, O., Sailer, M., Schmidt, A., Seidel, T., Stadler, M., Weller, J., Kuhn, J., and Kasneci, G. (2023). ChatGPT for good? On opportunities and challenges of large language models for education. Learning and Individual Differences, 103, 102274. https://doi.org/10.1016/j.lindif.2023.102274

Miao, F., and Holmes, W. (2023). Guidance for generative AI in education and research. UNESCO. https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research (accessed 5 September 2026).

OECD. (2026). Designing safe AI systems for education. OECD Education and Skills Today. https://www.oecd.org/en/blogs/2026/01/designing-safe-ai-systems-for-education.html (accessed 5 September 2026).

Pardo, A., and Siemens, G. (2014). Ethical and privacy principles for learning analytics. British Journal of Educational Technology, 45(3), 438-450. https://doi.org/10.1111/bjet.12152

UNESCO. (2025). AI and education: Protecting the rights of learners. https://unesdoc.unesco.org/ark:/48223/pf0000395373 (accessed 5 September 2026).

UNICEF. (2021). Policy guidance on AI for children. UNICEF Office of Global Insight and Policy. https://www.unicef.org/globalinsight/reports/policy-guidance-ai-children (accessed 5 September 2026).

U.S. Department of Education, Office of Educational Technology. (2023). Artificial Intelligence and the Future of Teaching and Learning: Insights and Recommendations. https://www.ed.gov/sites/ed/files/documents/ai-report/ai-report.pdf (accessed 5 September 2026).

Williamson, B., and Eynon, R. (2020). Historical threads, missing links, and future directions in AI in education. Learning, Media and Technology, 45(3), 223-235. https://doi.org/10.1080/17439884.2020.1798995

Zawacki-Richter, O., Marín, V. I., Bond, M., and Gouverneur, F. (2019). Systematic review of research on artificial intelligence applications in higher education: Where are the educators? International Journal of Educational Technology in Higher Education, 16, 39. https://doi.org/10.1186/s41239-019-0171-0
