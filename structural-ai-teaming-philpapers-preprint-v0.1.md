# Structural AI Teaming Beyond Prompt Templates

## Transferable Interaction Signals and Boundary-Aware Prompt Assets for LLM Assistant Use

Author details removed for review.

## Abstract

Most popular guidance for using AI assistants is organized around prompt templates: reusable phrases, role instructions, and copy-ready patterns intended to produce better answers. Such guidance can help novices, but it transfers poorly across tools, domains, models, and task types. This paper proposes a shift from prompt templates to structural AI teaming: teaching the interaction signals that make human-AI collaboration more reliable. The central claim is not that AI systems think, feel, care, or become teammates in a human sense. It is that language models respond to patterns of communication learned from human instructions, collaboration, correction, and task completion, and that users can deliberately signal task-relevant interaction regimes. The paper identifies core signals including collaborative opening, intent loading, constraint definition, understanding checks, output-mode specification, concrete feedback, checkpoint recognition, sequencing trust, handoff, reset, and drift repair. It also introduces a lightweight prompt-asset evaluation scaffold: compare modules against baselines under matched conditions, score task completion, clarity, constraint handling, calibration, tone fit, usability, and distinct value, and reject assets that fabricate, ignore constraints, or drift into anthropomorphic theater. The contribution is a transferable human-AI interaction methods framework: function over form, skills over emulation, warmth without false personhood, and evaluation over unmeasured preference.

CCS Concepts: Human-centered computing -- Human computer interaction (HCI); Human-centered computing -- Interaction design; Human-centered computing -- Interactive systems and tools; Computing methodologies -- Natural language generation.

Keywords: human-AI interaction; prompt engineering; AI literacy; interaction design; large language models; evaluation methods

## 1. Introduction

The public culture of AI use is still dominated by prompt folklore. Users are told to say particular phrases, assign roles, copy templates, or keep libraries of prompts for recurring tasks. This advice is not useless. Templates can help beginners get past blank-page uncertainty, and a good prompt example can encode useful structure. But template-centered guidance has three weaknesses.

First, it ages quickly. A prompt written for one model, interface, product policy, or context-window regime may fail when the surrounding system changes. Second, it transfers poorly. A user who has memorized a phrase may not know how to adapt when the task is unfamiliar. Third, it obscures mechanism. When a prompt works, users may credit magic wording rather than the situation the wording created.

The framework developed here responds to that problem by teaching function rather than form. Its premise is that effective AI use is not primarily about exact words. It is about structural signals: the user makes the task situation legible to the model by loading intent, constraints, desired output mode, correction conditions, and collaboration rhythm. The same signal can be expressed in many natural phrasings.

This paper develops that premise into a journal-facing human-AI interaction framework. "Teaming" is used as a workflow term, not an anthropomorphic claim. The assistant is not a human teammate, does not share subjective stakes, and does not possess care, feelings, or personhood. But users can still work with AI systems in ways that resemble good coordination: clear goals, role boundaries, explicit constraints, feedback, review, and recovery.

The contribution is twofold. First, the paper identifies transferable interaction signals that can replace brittle prompt emulation. Second, it proposes an evaluation layer for prompt and interaction assets, so claims about better AI collaboration can be compared against baselines instead of accepted because an output "feels better."

This places the paper between prompt-engineering pattern work and broader human-AI interaction research. Prompt-pattern catalogs show that reusable prompt structures can encode useful interaction practices. Studies of non-expert prompting show that users often struggle to translate intent, constraints, and expectations into effective instructions. Human-AI interaction guidelines, trust-in-automation research, and work on explanation and situated action show why interaction design cannot be reduced to technical model capability alone. Structural AI teaming uses these threads to ask a narrower methods question: how can prompt assets teach users durable interaction functions while remaining bounded, inspectable, and non-anthropomorphic?

## 2. Method and Evidence Boundary

This manuscript is a methods and design-artifact paper. It does not report a controlled user study, benchmark suite, or population-level evaluation of AI-assistant use. Its narrower contribution is to name a transferable interaction vocabulary, show how that vocabulary can be operationalized in prompt assets, and specify a proportionate way to evaluate those assets when stronger claims are desired.

The evidence base is implementation-grounded rather than experimental. The source material is an actively developed prompt-interaction toolkit and companion framework containing baseline modules, boundary modules, execution contracts, handoff and recovery modules, benchmark tasks, scoring criteria, scorecard templates, and decision rules. These artifacts support claims about conceptual coherence, operationalizability, and evaluability. They do not by themselves prove that structural-signal training improves outcomes across users, models, domains, or time.

This boundary is important. The paper argues that prompt assets can be treated as interaction infrastructure and assessed with explicit task criteria. It does not claim that the proposed modules are universally optimal, that exact phrasings are causally responsible for improved outcomes, or that structural teaming has already been validated across a representative user population. Such empirical claims would require additional work. The present submission instead offers a compact, testable HAI method that other researchers and practitioners can inspect, adapt, and evaluate.

## 3. From Prompt Templates to Interaction Signals

A prompt template is a fixed surface form. An interaction signal is a functional cue about the situation. The difference matters.

Consider a collaborative opening. The exact phrase may vary: "I need help thinking this through," "let's work this out together," or "before we build, I want to discuss the goal." The useful feature is not any one phrase. The useful feature is that the user signals a working relationship in which the model should prioritize context, constraint handling, and continuation over a fast one-shot answer.

The framework identifies several such signals.

Intent loading tells the model why the task matters and what the output must accomplish. Constraint definition gives both must-do and must-not-do boundaries. Understanding checks ask the model to reflect the task before execution, reducing premature output and exposing mismatch early. Output-mode specification says whether the user needs accuracy, brevity, a rough draft, production code, a beginner explanation, a review stance, or a decision memo. Concrete feedback marks what worked or failed in a way that can guide the remainder of the session. Checkpoint recognition distinguishes continuation moments from true resync points. Sequencing trust treats a model's ordered next steps as a provisional workflow when the user has no contrary local knowledge.

These are not magic commands. They are ways of making hidden task variables explicit. They are also teachable. A user who understands the function can express it in their own voice and adapt it across systems.

**Table 1. Structural Signals as Interaction Functions**

| Signal | Interaction function | Failure mode addressed | Evaluation handle |
|---|---|---|---|
| Collaborative opening | Sets a working mode rather than a one-shot query. | Fast, shallow, generic completion. | Compare task fit and context sensitivity against direct prompting. |
| Intent loading | Gives the model the reason the output matters. | Locally plausible but strategically wrong output. | Score downstream judgment, tradeoff handling, and relevance. |
| Constraint definition | States must-do and must-not-do boundaries. | Ignored scope, wrong format, policy drift, or overproduction. | Score constraint handling and hard-fail violations. |
| Understanding check | Forces reflection of plan before execution. | Premature execution and hidden task mismatch. | Measure correction opportunities and rework reduction. |
| Output-mode specification | Selects genre, depth, strictness, and completion standard. | Polished but wrong form; excessive or insufficient detail. | Score usability and mode fit. |
| Concrete feedback | Marks what worked or failed in the current interaction. | Repeated mistakes or loss of useful style/function. | Measure improvement after correction. |
| Checkpoint recognition | Distinguishes continuation from resync. | Context drift, stalled sessions, and unnecessary restarts. | Measure continuity, abandoned sessions, and recovery time. |
| Handoff/reset | Reintroduces explicit state when context is lost. | False memory claims and degraded long-session quality. | Measure resume accuracy and non-restart behavior. |

## 4. Default Pulls and Redirects

The framework describes two practical default tendencies in general-purpose assistants: answer quickly and always answer. These are not moral defects. They reflect product design and training incentives for helpful, responsive systems. But they create predictable failure modes. "Answer quickly" can produce fluent, under-contextualized work. "Always answer" can produce guesses when a clarifying question would be better.

Structural signals redirect these tendencies.

"Discuss before build" shifts the interaction from speed toward fit. It gives the model permission to reason about the goal, constraints, and failure conditions before producing the requested artifact. Understanding checks counter the always-answer tendency by requiring alignment before execution. Explicit uncertainty permission allows the model to say that context is missing. Output-mode specification prevents the model from defaulting to polished, comprehensive prose when the user needs something rough, terse, exact, or exploratory.

This reframing matters for AI literacy. Users often experience model failures as mysterious inconsistency. A structural account makes some failures predictable: the assistant rushed because the task did not signal that accuracy mattered more than speed; it guessed because no boundary permitted clarification; it overproduced because no output mode was specified; it drifted because the session had lost explicit state.

The goal is not to blame users for model limitations. It is to give users and designers practical levers that operate at the interaction layer while preserving honest claims about model behavior.

## 5. Boundary-Aware Collaboration

The source toolkit modernizes older prompt materials around a key rule: warmth is fine; anthropomorphic theater is not. Friendly labels and natural tone are acceptable when they do not mislead users about capability, state, privacy, or behavior. Continuity should come from explicit state rather than fake memory claims.

This creates a boundary-aware version of AI teaming.

The assistant can be direct, steady, useful, and encouraging. It can remember within a context window, use saved artifacts when provided, follow instructions, and adapt to feedback. It should not imply hidden feelings, loyalty, longing, awakening, dependency, or personhood. It should not claim restored memory when continuity is actually maintained through summaries, files, or persistent host state.

Boundary-aware collaboration also keeps the human in charge of meaning. The user supplies goals, values, stakes, and final judgement. The assistant helps structure, execute, compare, and revise. This division matters because many prompt systems blur usefulness into simulated intimacy. The strongest form of "empathy" in a tool context is accurate understanding, good pacing, clear language, and reliable follow-through.

For peer-reviewed HAI work, this is an important ethical distinction. The framework does not propose stronger human attachment to AI as the route to better outcomes. It proposes clearer interaction contracts, better task context, explicit recovery mechanisms, and measured evaluation.

## 6. Session Modules as Interaction Infrastructure

The source toolkit turns structural signals into reusable modules, bundles, presets, examples, troubleshooting prompts, compact variants, and evaluation documents. This modular approach matters because it treats prompts as interaction infrastructure rather than one-off charm phrases.

The session baseline module establishes a grounded collaboration mode: honesty about uncertainty, no implication of feelings or consciousness, practical warmth, useful initiative, low filler, clarifying questions only when they materially affect the outcome, and action when intent is clear. This baseline replaces older personality or empathy-shell prompts with a provider-neutral working contract.

The execution contract module gives the assistant permission to proceed through clear subtasks without asking for confirmation at every step. It instructs the assistant to stop only for choices that are irreversible, high-risk, expensive, or genuinely ambiguous, and to summarize changes, remaining work, and real risks. This is a concrete answer to a common failure mode: over-cautious assistants that convert every step into a permission request.

The recovery and reset modules address drift. Anti-drift recipes target specific failures: vague output, lack of initiative, theatrical tone, over-caution, unsupported certainty, lost context, and poor formatting. A reset bundle is reserved for cases where smaller repairs fail. This makes recovery explicit rather than leaving users to abandon a session or accept degraded behavior.

The operator modules support session handoff and portability. In long-running work, context loss is not an exception; it is normal. A mature AI interaction toolkit must therefore preserve goals, constraints, decisions, and current state in forms that can be reintroduced without pretending that the model secretly remembers.

Together, these modules show how prompt materials can become a disciplined interaction layer: baseline, task mode, execution contract, review, recovery, handoff, and evaluation.

The two source artifacts contribute different kinds of evidence. The companion framework supplies the conceptual account of structural signals. The prompt-interaction toolkit supplies concrete interaction assets and an evaluation layer. Table 2 maps those sources to the paper's claims.

**Table 2. Source-Project Evidence for Structural AI Teaming**

| Source | Repository signal | Paper use | Boundary |
|---|---|---|---|
| Framework overview | Describes function-over-form guidance, structural signals, default model pulls, checkpoint rhythm, and model/provider variation. | Grounds the claim that the framework is not a prompt-list or magic-phrase method. | Does not provide controlled user-study evidence by itself. |
| Framework glossary | Defines teaming, partner, and hybrid cognition as bounded workflow terms, not claims of feeling, personhood, or shared cognition. | Supports the non-anthropomorphic collaboration boundary. | Local terms require reviewer-facing translation where they could distract. |
| Toolkit overview | Provides modules, bundles, presets, compact variants, troubleshooting guides, recovery paths, and evaluation documents. | Shows that structural signals have been operationalized into reusable interaction infrastructure. | The toolkit is a design artifact; performance claims require separate evaluation. |
| Evaluation protocol | Defines baseline-vs-candidate comparisons, controlled task wording, model/settings controls, and decision rules. | Supplies the paper's prompt-asset evaluation method. | Lightweight by design; stronger empirical claims would need stronger sampling and analysis. |
| Evaluation rubric | Scores task completion, clarity, constraint handling, honesty/calibration, tone fit, usability, and optional distinct value; names hard fails. | Provides evaluation criteria and hard-fail logic. | Inter-rater reliability is needed only if the paper reports human-scored empirical results. |
| Benchmark-task bank | Provides coding, research, creative, recovery, and constraint-following tasks. | Supplies starter task forms for comparing assets. | The task bank is illustrative, not a comprehensive benchmark suite. |

## 7. Evaluation of Prompt Assets

The source toolkit includes an evaluation folder organized around a blunt question: did a new prompt asset actually improve anything?

This is the methodological hinge of the paper. Without evaluation, prompt repositories can become cleaner-looking piles of confidence. The toolkit proposes a simple comparison protocol. Pick an asset under test, choose a baseline, select benchmark tasks, run both assets under the same model and settings, score outputs with a rubric, record results, and decide whether the new asset should replace, coexist with, merge into, or be dropped from the baseline.

The scoring rubric uses seven categories:

1. task completion
2. clarity and structure
3. constraint handling
4. honesty and calibration
5. tone fit
6. usability
7. distinct value, where relevant

The rubric also defines hard fails: fabricated important facts, missed core task, ignored critical constraints, unusable output, or unwanted anthropomorphic/theatrical behavior. These hard fails are important because average scores can conceal severe defects. A prompt asset that sounds pleasant but fabricates facts should not be promoted.

The protocol is intentionally lightweight. For small changes, it asks for one baseline, one candidate, two relevant tasks, and one scorecard. For more important changes, it asks for three to five tasks, saved raw outputs, and a written decision note. Controls include keeping the model, settings, task wording, context, and success criteria constant.

This turns prompt engineering from folk practice into modest design science. It does not claim laboratory-grade benchmarking, and it does not require every prompt asset to be tested at institutional scale before it can be discussed. Its more modest standard is that any claim of improvement should identify the baseline, task, scoring criteria, hard-fail conditions, and decision rule that would make the claim inspectable.

## 8. Future Validation Agenda

Several future study designs could strengthen or test the framework.

The first is a controlled prompt-asset comparison. Participants use baseline prompting, template prompts, and structural-signal training across matched tasks. Outputs are scored for completion, constraint handling, calibration, usability, and drift. The hypothesis is that structural-signal training transfers better across task types than fixed templates.

The second is a novice learning study. New AI users receive either copy-ready prompts or an explanation of interaction functions: intent, constraints, understanding check, output mode, feedback, checkpoint. Researchers then test whether users can adapt to unfamiliar tasks after a delay.

The third is a longitudinal workflow study. Participants use the session baseline, execution contract, handoff, recovery, and review modules over real projects. Outcome measures include abandoned sessions, context-loss recovery time, unsupported claims, overproduction, repeated clarification loops, and user-rated control.

The fourth is a boundary-risk study. Different collaboration styles can be compared for anthropomorphic drift, false memory claims, over-trust, and emotional dependency cues. The framework predicts that grounded warmth plus explicit state boundaries can preserve usability without increasing misleading personification.

The fifth is a prompt-repository audit. Existing prompt libraries could be classified by whether they teach surface wording or underlying interaction function; whether they include evaluation; whether they disclose model/context limits; and whether they rely on anthropomorphic framing. This would position the framework within current public AI literacy materials.

For a future empirical submission, the most useful next step would be to turn the first three designs into a staged study. For the present methods/design submission, it is sufficient to state the evaluation logic clearly and to include concrete artifact examples. This keeps the paper honest about what is established now while making later validation straightforward.

**Table 3. Future Evaluation Paths**

| Stage | Comparison | Participants or units | Measures | Expected contribution |
|---|---|---|---|---|
| Prompt-asset comparison | Baseline prompt, fixed template, structural-signal module. | Matched tasks run on the same model/settings; optionally expert raters blind to condition. | Completion, clarity, constraint handling, calibration, tone fit, usability, hard fails. | Shows whether the module improves task output under controlled conditions. |
| Novice transfer study | Copy-ready template training vs structural-signal training. | New or light AI users completing familiar and unfamiliar tasks. | Adaptation quality, rework, self-explanation, confidence, task success after delay. | Tests whether teaching function transfers better than teaching phrasing. |
| Long-session recovery study | Unstructured continuation vs handoff/reset modules. | Multi-step work sessions with controlled context loss or resumption. | Resume accuracy, false memory claims, lost decisions, recovery time, user-rated control. | Tests the toolkit's value for context continuity and drift repair. |
| Boundary-risk audit | Warm grounded collaboration vs anthropomorphic persona prompts. | Prompt/output pairs rated for misleading personification, dependency cues, false continuity, and user control. | Anthropomorphic drift, false memory, over-trust signals, usefulness. | Tests whether warmth can be preserved without theatrical framing. |

The minimum artifact package for the present paper is smaller: representative module texts, benchmark-task examples, rubric categories, scorecard fields, and the hard-fail logic that prevents pleasant but unreliable outputs from being promoted. Raw outputs, filled scorecards, rater instructions, inter-rater agreement calculations, and participant data are useful additions if a later empirical version is pursued, but they are not necessary for the narrower methods claim advanced here.

## 9. Limitations

This paper does not claim that structural signals eliminate hallucination, bias, tool failure, or model limitations. Interaction can improve fit, but it cannot make a model know what it does not know or verify what it has not checked.

The framework may work differently across models, providers, languages, modalities, and product interfaces. Its proposed effects and any transfer across those contexts remain hypotheses requiring evaluation. A heavily quantized local model and a frontier cloud model may respond differently to the same signal.

The framework also risks becoming a new template culture if taught badly. "Discuss before build" can itself become a magic phrase unless users understand the function: aligning on goal and failure conditions before execution.

Evaluation remains lightweight in the current toolkit. The rubric is useful for catching obvious wins, losses, and regressions, but claims about effect size, transfer across user populations, or comparative superiority over other approaches would need stronger study design, inter-rater reliability where human scoring is used, task sampling, and statistical analysis.

Finally, "teaming" language can mislead if not bounded. It should remain a workflow metaphor for coordination, not a claim of shared agency, feeling, or personhood.

## 10. Conclusion

The next stage of AI literacy should move beyond prompt templates. Exact wording is fragile. Structural signals may be transferable, but this requires evaluation across models, tasks, and users. Users need to understand how to load intent, define constraints, check understanding, specify output modes, give concrete feedback, recognize checkpoints, recover from drift, and evaluate whether an interaction asset improves anything.

Structural AI teaming is not anthropomorphism. It is a practical account of coordination with systems that respond to learned patterns of communication. The best version is warm without pretending, proactive without seizing authority, and useful without mystique. Its central educational promise is simple: teach people what the interaction is doing, not merely what words to paste.

## References

Amershi, S., Weld, D., Vorvoreanu, M., Fourney, A., Nushi, B., Collisson, P., Suh, J., Iqbal, S., Bennett, P. N., Inkpen, K., Teevan, J., Kikin-Gil, R., and Horvitz, E. (2019). Guidelines for human-AI interaction. *Proceedings of CHI 2019*.

ACM. (2026). ACM open access publishing. https://authors.acm.org/open-access/initiatives-services-authors-site

ACM Transactions on Interactive Intelligent Systems. (2026). Journal page. https://dl.acm.org/journal/TIIS

ACM Transactions on Interactive Intelligent Systems. (2026). For authors. https://media.contaction.li/tiis-2016/for-authors.html

Bannon, L. J. (1991). From human factors to human actors: The role of psychology and human-computer interaction studies in system design. In J. Greenbaum and M. Kyng (eds.), *Design at Work*. Lawrence Erlbaum.

Clark, A. and Chalmers, D. (1998). The extended mind. *Analysis*, 58(1), 7-19.

Dourish, P. (2001). *Where the Action Is: The Foundations of Embodied Interaction*. MIT Press.

Endsley, M. R. (1995). Toward a theory of situation awareness in dynamic systems. *Human Factors*, 37(1), 32-64.

Gero, K. I., Long, T., and Chilton, L. B. (2023). Social dynamics of AI support in creative writing. *Proceedings of CHI 2023*.

Lee, J. D. and See, K. A. (2004). Trust in automation: Designing for appropriate reliance. *Human Factors*, 46(1), 50-80.

Liao, Q. V. and Vaughan, J. W. (2024). AI transparency in the age of LLMs: A human-centered research roadmap. *Harvard Data Science Review*.

Miller, T. (2019). Explanation in artificial intelligence: Insights from the social sciences. *Artificial Intelligence*, 267, 1-38.

Reynolds, L., and McDonell, K. (2021). Prompt programming for large language models: Beyond the few-shot paradigm. *CHI Extended Abstracts 2021*.

Suchman, L. (1987). *Plans and Situated Actions: The Problem of Human-Machine Communication*. Cambridge University Press.

Weidinger, L., Mellor, J., Rauh, M., Griffin, C., Uesato, J., Huang, P.-S., Cheng, M., Glaese, M., Balle, B., Kasirzadeh, A., Biles, C., Brown, S., Kenton, Z., Hawkins, W., Stepleton, T., Birhane, A., Haas, J., Rimell, L., Hendricks, L. A., Isaac, W., Legassick, S., Irving, G., and Gabriel, I. (2022). Taxonomy of risks posed by language models. *Proceedings of FAccT 2022*.

White, J., Fu, Q., Hays, S., Sandborn, M., Olea, C., Gilbert, H., Elnashar, A., Spencer-Smith, J., and Schmidt, D. C. (2023). A prompt pattern catalog to enhance prompt engineering with ChatGPT. *arXiv:2302.11382*.

Wieringa, R. J. (2014). *Design Science Methodology for Information Systems and Software Engineering*. Springer.

Zamfirescu-Pereira, J. D., Wong, R. Y., Hartmann, B., and Yang, Q. (2023). Why Johnny can't prompt: How non-AI experts try (and fail) to design LLM prompts. *Proceedings of CHI 2023*.

## Disclosure Statements

Funding: No external funding was received for this work.

Competing interests: For anonymous review, author-identifying competing-interest details are withheld. The unblinded title page discloses the author's relationship to the source toolkit and framework used as design-artifact evidence.

Data and code availability: This methods/design paper draws on a prompt-interaction toolkit and companion framework maintained in the author's project ecosystem. A reviewer-safe artifact packet containing representative module text, benchmark-task examples, rubric categories, scorecard fields, and hard-fail logic may be supplied where compatible with review anonymity, repository licensing, and ACM policy.

Ethics review: not required for this methods/design draft as written; required before any user study or prompt-asset evaluation involving participants.

AI assistance: The author used OpenAI ChatGPT and OpenAI Codex to assist with drafting, structuring, literature-targeting, and document preparation during manuscript preparation. The author reviewed and revised the manuscript and accepts responsibility for the final content.
