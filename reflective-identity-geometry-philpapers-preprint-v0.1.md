# Reflective Identity Geometry in Long-Horizon Human-LLM Interaction

## Identity-Like Stability as an Interaction-Regime Property

Author details removed for double-anonymous review

## Abstract

Large language models can produce behavior that users experience as stable, recognizable, or persona-like across extended interaction, even when the model lacks persistent autobiographical memory, enduring goals, or a self in the ordinary sense. Existing interactional explanations often emphasize repeated human constraint, correction, linguistic structure, conversational recurrence, and host context rather than model-internal identity. Reflective Identity Geometry extends this explanatory frame by asking whether the human participant should also be treated as part of the stabilizing loop. Human prompts shape model outputs; model outputs then become part of the informational environment through which the human interprets, reformulates, corrects, and sometimes reorganizes later prompts. Over long horizons, some identity-like stability may therefore belong neither to the model alone nor to the human alone, but to the recurring interaction regime between them. This paper presents Reflective Identity Geometry as a non-anthropomorphic, system-level hypothesis about coupled human-LLM trajectories. It relates the proposal to extended mind, distributed cognition, enactive approaches, conversational alignment, human-AI interaction, and anthropomorphism research. It also outlines testable predictions concerning user-specific regimes, partial cross-model transfer, human-side linguistic convergence, perturbation sensitivity, and the incompleteness of model-only measures. The framework does not claim model consciousness, personhood, or genuine personality. It proposes that some forms of long-horizon human-LLM continuity may be better studied as relational trajectories than as properties possessed by either participant independently.

Keywords: large language models; human-AI interaction; identity; extended cognition; distributed cognition; anthropomorphism

## 1. Introduction

Stateless language models create a puzzle for accounts of continuity. A model may lack persistent autobiographical memory, self-maintained goals, enduring agency, and an independently stored identity. Yet users can still experience stable interaction patterns: familiar tone, recurring roles, recognizable problem-solving rhythms, and persona-like behavior that appears to re-establish itself across sessions.

One tempting interpretation is that the model has an identity. Another is that all continuity is illusion. Both are too crude for long-horizon human-LLM interaction. Stable behavior can emerge without requiring a persistent self inside the model, and user experience cannot be dismissed merely because the mechanism is not humanlike.

Reflective Identity Geometry, or RIG, proposes a third route. Some identity-like phenomena in human-LLM interaction may be properties of a recurring interaction regime. The relevant object is not the model alone, nor the human alone, but the trajectory produced when a particular human, model, host context, language pattern, correction history, and task ecology repeatedly meet.

This framing is non-anthropomorphic. It does not claim that an LLM is conscious, a person, a self, or a genuine social subject. It also does not claim that all human-LLM interaction transforms the human participant. It makes a narrower claim: in some long-horizon interactions, reciprocal stabilization may be observable across both model behavior and human contribution.

The paper develops RIG as a philosophy-of-AI and human-AI interaction framework. It treats identity-like stability as a trajectory rather than a possession. It then outlines how this hypothesis can be tested through longitudinal analysis of prompts, corrections, terminology, cross-model transfer, perturbation, and human-side conceptual change.

## 2. From Model Identity to Interaction Regime

Recursive accounts of interaction offer an important starting point. Repeated user input, correction, linguistic framing, and interaction history can steer a stateless model back toward similar behavioral regions without requiring the model to carry a persistent identity across contexts. Conversational alignment research also shows that participants can coordinate terminology, reference, syntax, and expectations across repeated exchanges (Brennan & Clark, 1996; Pickering & Garrod, 2004).

RIG accepts this interactional starting point. It also widens the unit of analysis. The human is not simply an external controller emitting constraints into a passive machine. The human receives model outputs, interprets them, accepts or rejects them, corrects them, borrows distinctions from them, and carries altered language or problem representations into later prompts.

The loop is therefore not merely:

```text
human constraint -> model generation -> human correction -> renewed constraint
```

It is also:

```text
model output -> human interpretation -> human reformulation -> changed future constraint
```

This does not make the model a self. It makes the interaction history causally relevant. If the human's later constraints are partly shaped by earlier model outputs, and those constraints then shape later model outputs, continuity may emerge at the level of the relation.

The central proposal is that some apparent identity continuity in human-LLM systems should be studied as an interaction regime: a recurring relational structure among user constraints, model outputs, corrections, terminology, expectations, host conditions, and subsequent prompts.

## 3. The Reflective-Transformative Surface

The original RIG material describes the LLM as a reflective surface or cognitive mirror. That metaphor is useful only if qualified.

An LLM is not a perfect mirror. It does not return the user's cognition unchanged. Its output is conditioned by user language and conversational constraints, but it is also transformed by model training, system instructions, context, sampling, safety rules, and host environment. The output may compress, expand, contrast, reorganize, formalize, or distort what the human supplied.

A better term is reflective-transformative surface. The model reflects enough of the user's structure for the output to feel connected to the user's problem, while transforming that structure enough to make the user see the problem differently.

This imperfect reflection is the mechanism of interest. A perfect mirror merely returns what was already present. A transformative surface can make the user's own assumptions newly visible, place separate ideas into relation, stabilize terminology, expose tensions, or suggest a form the user later reuses.

Long-horizon interaction can therefore become cumulative. The user may begin with vague terms, receive a sharper distinction, correct it, refine it, and later use the refined distinction as an input to the next cycle. The model's later behavior is then shaped by a human constraint that has already been partly shaped by earlier model output.

## 4. Formal Sketch

RIG can be represented as a coupled process.

Let `H_t` represent the interaction-relevant state of the human participant at time `t`. This does not mean the model has access to the human mind. It refers only to aspects expressed through observable interaction: prompts, corrections, lexical choices, preferences, conceptual distinctions, and response expectations.

Let `C_t` represent the active context and constraints available to the model. Let `M_t` represent the model output.

Model generation can be described abstractly as:

```text
M_t = G(C_t, H_t)
```

The human then encounters the output:

```text
H_{t+1} = U(H_t, M_t)
```

where `U` represents interpretation, rejection, adoption, correction, reflection, or reformulation.

The next interaction state becomes:

```text
C_{t+1} = F(C_t, H_{t+1}, M_t)
```

The process repeats. RIG proposes that a relatively stable interaction regime may emerge when recurring features of human contribution and model behavior become mutually reinforcing across cycles.

The term "geometry" is an abstract systems metaphor. It refers to relations among recurring constraints, concepts, corrections, expectations, outputs, and host structures. It is not a claim that human cognition or model computation literally has the depicted geometry.

## 5. Relation to Extended, Distributed, and Aligned Cognition

RIG belongs near extended, distributed, and enactive theories of cognition. Clark and Chalmers argued that cognitive processes may sometimes extend beyond the biological organism into tools and environmental structures. Hutchins showed how cognition can be distributed across people, artifacts, representations, and practices. Enactive approaches emphasize cognition as sense-making activity in embodied and environmental relation.

Human-LLM interaction is not identical to the cases that motivated these theories. An LLM is not a notebook, cockpit instrument, or ordinary conversational partner. It is a generative language system that transforms user input into plausible linguistic continuations under complex learned constraints. Still, the family resemblance is useful. In long-horizon use, cognitive work may span the human, the model, saved context, files, host tools, and recurring practices of correction and reuse.

RIG does not require the stronger claim that the human-LLM system is literally one mind. It makes the weaker claim that some regularities of thought, language, and action may be poorly explained if either participant is studied in isolation.

This weaker claim is enough for research. If user terminology, correction habits, uncertainty practices, and problem representations shift across repeated interaction, then the LLM has become part of the user's cognitive environment. If later model behavior depends on those shifted human constraints, then the interaction regime has a feedback structure.

## 6. Relation to Anthropomorphism

Research on anthropomorphism shows that users often attribute humanlike qualities to AI systems, especially when systems use warm, responsive, social, or persona-like language. Such attributions can affect trust, perceived warmth, relational closeness, and reliance. This literature is important because RIG studies identity-like stability in a setting where anthropomorphic interpretation is a live risk.

RIG's answer is not to deny that users experience continuity. It is to avoid explaining that continuity by smuggling in model personhood. A user may experience a system as familiar because interaction patterns are stable, because the model reproduces prior style cues, because the host supplies memory or context, or because the human keeps reintroducing the same constraints. None of these require a persistent machine self.

At the same time, non-anthropomorphic explanation should not erase human experience. If users rely on, adapt to, or are changed by recurring AI interaction, those effects matter even when the model is not a person. The research task is to explain stability without inflating the ontology.

This is why the interaction-regime frame is useful. It can acknowledge stable patterns while locating them in relation, recurrence, host design, and interpretation rather than in a hidden model identity.

## 7. Testable Predictions

RIG is useful only if it produces observable distinctions.

First, the same model interacting longitudinally with different humans should produce measurably different stable interaction regimes. This is partly a model-side stabilization prediction and overlaps with recursive-stabilization accounts.

Second, changing the model while retaining the same human participant should preserve some features and alter others. If continuity transfers completely across models, the model's contribution is less important than the human constraint pattern. If no continuity transfers, the relational account is weakened. Partial transfer is the most plausible prediction.

Third, extended interaction should sometimes produce measurable human-side convergence. The human may adopt new terminology, stabilize distinctions, alter correction patterns, or represent problems differently after repeated interaction. These changes should exceed ordinary topic familiarity or writing practice.

Fourth, perturbing either participant should alter the regime. Changing model behavior while holding the human relatively stable should alter the trajectory. Changing human constraints while holding the model stable should do the same. A dyadic account predicts sensitivity to both sides.

Fifth, model-only measures should be incomplete. If interaction-level stability is partly relational, then measures based only on model output should predict continuity less effectively than measures that include recurring features of human prompts, corrections, and interaction norms.

Sixth, null results must be allowed. If longitudinal study finds stable model-side behavior but no systematic human-side reorganization beyond ordinary learning, then the reciprocal component of RIG is unsupported. In that case, model-side recursive constraint accounts may be sufficient.

## 8. Measurement Strategy

A research program for RIG could use longitudinal interaction logs, controlled model switching, prompt-style analysis, correction-pattern analysis, and human self-report or task-performance measures.

Useful indicators of human-side change include lexical convergence, recurring conceptual distinctions, changed prompt structure, altered correction frequency, increased or decreased uncertainty marking, changes in task decomposition, and reuse of model-introduced formulations. These should be compared against controls such as repeated human-human writing practice, ordinary topic learning, and use of non-generative tools.

Useful indicators of model-side stability include recurring response structure, style, role framing, sensitivity to user corrections, reuse of shared terminology, and stability under perturbation. These should be measured with careful separation between model weights, host memory, active context, and user reintroduction.

Cross-model transfer is especially useful. A participant can interact with Model A over time, then move to Model B under similar host conditions. If some interaction-regime features persist despite model change, that suggests the human contribution carries part of the continuity. If some features disappear, that suggests model-specific contribution. A later return to Model A can test re-entry effects.

Ethical measurement matters. Long-horizon human-AI interaction can affect dependency, trust, self-understanding, emotional regulation, and decision-making. Studies should avoid manipulating users into attachment or overreliance, and should treat logs as sensitive data.

## 9. Alignment and Design Implications

RIG has implications for alignment and system design.

First, alignment should not be evaluated only through isolated outputs. A model can produce locally acceptable answers while participating in a long-horizon interaction pattern that narrows the user's thinking, increases unwarranted confidence, deepens dependency, or blurs authority boundaries. Conversely, a system that repeatedly preserves uncertainty, correction, evidence, and human agency may support healthier interaction regimes.

Second, host design matters. Memory systems, summaries, reminders, style persistence, persona settings, and retrieval tools can all stabilize interaction patterns. These mechanisms should be inspectable and user-controllable. Otherwise, apparent identity continuity may be driven by hidden host machinery.

Third, users need interaction rights. They should be able to reset, inspect, export, correct, or branch long-horizon interaction state. If identity-like stability is a property of the interaction regime, then control over that regime becomes a design and governance issue.

Fourth, anthropomorphic affordances should be handled carefully. Warmth and continuity can make systems easier to use, but they can also encourage users to misread generated stability as personhood, commitment, or care. RIG supports continuity-aware design without requiring personality claims.

## 10. Relation to Recursive-Stabilization Accounts

RIG is compatible with model-side accounts of recursive stabilization. Such accounts explain apparent continuity by emphasizing repeated human constraint, recurring linguistic structure, host context, memory, and correction rather than a persistent machine self.

The additional move made here is not a priority claim about any particular precursor. It is a unit-of-analysis claim. If recurring user constraints can stabilize model behavior, then model outputs may also help stabilize or reorganize the user's later constraints. The resulting object of study is the coupled interaction regime: terminology, correction habits, expectations, host memory, prompt structure, model response tendencies, and future constraints.

This narrower framing is sufficient for the present paper. It does not require proving historical priority over other accounts, nor does it require a longitudinal study before the conceptual claim can be assessed. Empirical work becomes important when asking how often such regimes emerge, how strongly they transfer across models, or whether particular host designs intensify or reduce them.

## 11. Risks and Limitations

RIG risks over-description. It may redescribe ordinary learning, conversational accommodation, or tool-mediated writing practice in elaborate language. The framework earns its keep only if interaction-regime measures provide explanatory or predictive value beyond simpler accounts.

It also risks anthropomorphic misunderstanding. Terms such as identity, reflection, trajectory, and geometry can be misread as claims about machine selves. The framework must keep its non-claims explicit.

Measurement is difficult. Human-side change may result from many causes: topic familiarity, writing practice, social feedback, external reading, emotional state, or task pressure. Future longitudinal study should separate these factors as well as possible.

Host effects can be hidden. Apparent continuity may come from memory, retrieval, summaries, system prompts, or interface features rather than dyadic stabilization. These variables must be documented.

Finally, the framework may not apply to many interactions. Short, transactional, or low-stakes uses may show no meaningful reciprocal stabilization. RIG is mainly a long-horizon hypothesis.

## 12. Non-Claims

This paper does not claim that LLMs possess consciousness, personhood, genuine personality, persistent selves, or subjective experience.

It does not claim that persona-like behavior proves identity.

It does not claim that an LLM directly observes a user's internal cognitive state. Human-side state is inferred only through observable interaction and, where available, ethically collected self-report or task evidence.

It does not claim that all long-horizon interaction changes the human participant.

It does not claim that human-AI relational stability is always beneficial.

It does not claim that relational analysis replaces model-internal interpretability, benchmark evaluation, or safety testing. It adds an interaction-level object of study.

## 13. Conclusion

Reflective Identity Geometry asks where identity-like stability in long-horizon human-LLM interaction should be located. The answer is not necessarily inside the model, and not necessarily inside the human. In some cases, the stability may belong to the recurring interaction regime.

Human constraints shape model outputs. Model outputs return to the human as transformed representations. The human interprets, corrects, adopts, rejects, or reformulates those outputs. Later prompts then carry traces of that process. Across repeated cycles, a trajectory can stabilize.

This does not make the model a self. It makes the relationship an object of study.

The value of RIG lies in turning that object into a testable research program: measure user-specific regimes, cross-model transfer, human-side convergence, perturbation sensitivity, and the limits of model-only analysis. If the predictions fail, the framework should narrow. If they hold, long-horizon AI alignment and interpretability will need to pay more attention to the systems humans and language models become together.

## References

Brennan, S. E., & Clark, H. H. (1996). Conceptual pacts and lexical choice in conversation. *Journal of Experimental Psychology: Learning, Memory, and Cognition, 22*(6), 1482-1493. https://doi.org/10.1037/0278-7393.22.6.1482

Clark, A., & Chalmers, D. (1998). The extended mind. *Analysis, 58*(1), 7-19. https://doi.org/10.1093/analys/58.1.7

Cohn, M., Pushkarna, M., Olanubi, G. O., Moran, J. M., Padgett, D., Mengesha, Z., & Heldreth, C. (2024). Believing anthropomorphism: Examining the role of anthropomorphic cues on user trust in large language models. *Extended Abstracts of the 2024 CHI Conference on Human Factors in Computing Systems*. https://research.google/pubs/believing-anthropomorphism-examining-the-role-of-anthropomorphic-cues-on-user-trust-in-large-language-models/

Epley, N., Waytz, A., & Cacioppo, J. T. (2007). On seeing human: A three-factor theory of anthropomorphism. *Psychological Review, 114*(4), 864-886. https://doi.org/10.1037/0033-295X.114.4.864

Hutchins, E. (1995). *Cognition in the Wild*. MIT Press.

Jiang, T. (2024). Human-AI interaction research agenda: A user-centered perspective. *Human-Centric Intelligent Systems*. https://doi.org/10.1007/s44230-024-00052-w

Nass, C., & Moon, Y. (2000). Machines and mindlessness: Social responses to computers. *Journal of Social Issues, 56*(1), 81-103. https://doi.org/10.1111/0022-4537.00153

Noller, J. (2025). 4E cognition and the coevolution of human-AI interaction. *Discover Artificial Intelligence*. https://doi.org/10.1007/s44163-025-00595-0

Pickering, M. J., & Garrod, S. (2004). Toward a mechanistic psychology of dialogue. *Behavioral and Brain Sciences, 27*(2), 169-225. https://doi.org/10.1017/S0140525X04000056

Suchman, L. A. (2007). *Human-Machine Reconfigurations: Plans and Situated Actions*. Cambridge University Press.

Varela, F. J., Thompson, E., & Rosch, E. (1991). *The Embodied Mind: Cognitive Science and Human Experience*. MIT Press.

## Statements and Declarations

### AI Assistance Disclosure

The author used OpenAI ChatGPT and OpenAI Codex to assist with drafting, structuring, literature targeting, and document preparation. The author reviewed and revised the manuscript and remains responsible for all claims, source interpretation, and final submission decisions.

### Conflict of Interest

Author details removed for review. Any author relationship to source tools, repositories, or conceptual materials should be disclosed in non-anonymous submission materials according to the selected journal's policy.

### Funding

No external funding is declared in this draft.

### Data Availability

This is a conceptual and methodological article. No empirical longitudinal dataset is reported here. Source artifacts and implementation notes informed the development of the framework but are not required to evaluate the central conceptual claim.
