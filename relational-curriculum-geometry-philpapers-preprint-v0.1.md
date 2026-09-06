# Relational Curriculum Geometry for Small Language Models

## Data Order, Boundary Cases, and Transfer Under Constraint

Author details removed for review.

## Article Type and Evidence Boundary

This manuscript is framed as a protocol and hypothesis paper. Its contribution is the construction of a falsifiable experiment for testing whether relational arrangement in training or fine-tuning data affects small-language-model behavior under constraint. It does not report empirical results, trained-model comparisons, benchmark superiority, or validated learning effects.

The smallest defensible version therefore needs a clear hypothesis, relation taxonomy, controlled experimental design, scoring targets, confound list, falsification conditions, and an account of why the protocol matters for curriculum design and assistant safety. It does not need new model training results in this version. A later empirical article can cite this protocol paper and report the outcomes of Experiment 001.

The strongest near-term target is a venue that accepts conceptual, methodological, protocol, work-in-progress, or perspective contributions in AI education, human-centered intelligent systems, or AI and society. A technical Machine Learning submission should be reserved for the later results paper if Experiment 001 is actually run.

## Abstract

Curriculum learning studies whether models learn better when training examples are presented in a structured order rather than as uniformly shuffled data. This paper proposes a narrower and more relational version of that question for small language models: whether models trained or fine-tuned on the same examples, under the same token budget, behave differently when examples are arranged not only by difficulty but by prerequisite relation, boundary pressure, uncertainty state, role authority, tool-use relevance, and multithread task composition. I call this proposal relational curriculum geometry. The central claim is not that clean data is better than messy data, nor that scale is unnecessary. It is that example position may affect the later usability of learned concepts by shaping how concepts become reachable, separable, transferable, and comparable during inference. The paper defines the hypothesis, distinguishes it from ordinary domain grouping and easy-to-hard curricula, and specifies a first controlled experiment in programming and debugging. The proposed experiment compares random ordering, domain grouping, complexity ordering, and full relational curriculum ordering using matched data, model architecture, token count, and evaluation tasks. Target outcomes include learning per token, near transfer, cross-representation transfer, boundary detection, uncertainty surfacing, role-boundary discipline, tool-use discipline, multithread reasoning, prompt burden, and failure legibility. The paper is offered as a falsifiable protocol that can later support a separate empirical outcome paper.

Keywords: curriculum learning; language models; data ordering; transfer learning; AI education; human-centered AI

## 1. Introduction

Large language models are commonly analyzed through scale, architecture, data quantity, data quality, alignment, and benchmark performance. These dimensions matter. Yet the order and relational arrangement of examples may also matter, especially for smaller models that cannot rely on overwhelming parameter count, broad redundancy, or extensive prompt scaffolding at inference time.

The guiding question is simple: if two small language models see the same examples under the same training budget, but one sees them in random order and the other sees them as a staged relational curriculum, do they later behave differently?

This paper develops that question as the Relational Curriculum Geometry Hypothesis. The hypothesis is that language model behavior may be shaped not only by what a training set contains, but also by how examples are grouped, ordered, contrasted, repeated, labeled, and connected. In its shortest form: **training data is not only content; training data is also geometry.**

The term geometry is metaphorical. It does not imply model consciousness, personhood, biological cognition, or access to hidden mental states. It names an experimentally testable question about data order, latent organization, routing behavior, transfer, uncertainty handling, and observable outputs.

The paper focuses on small language models because constraints may make curriculum effects easier to observe. A very large model may compensate for weak curriculum structure through scale and redundancy. A smaller model has less slack. If relational ordering changes learning efficiency, transfer, boundary handling, uncertainty surfacing, or role discipline, that effect may be more visible under constraint.

The contribution is conceptual and methodological. I define relational curriculum geometry, position it against existing curriculum-learning approaches, specify a first controlled experiment, define scoring targets, and name the confounds that must be controlled before any later empirical claim can be accepted.

## 2. Background

Curriculum learning has a long history in machine learning and cognitive modeling. Elman's work on starting small showed how staged exposure can matter for learning in neural systems. Bengio and colleagues later formalized curriculum learning as presenting examples in an order that gradually introduces more difficult concepts. Self-paced learning further developed this family of ideas by allowing the learner or training procedure to select easier examples earlier and harder examples later.

Recent language-model work has renewed interest in data ordering for pretraining and fine-tuning. Some work investigates learnability-based curricula, difficulty metrics, pacing strategies, and model preference across training stages. The results are important but mixed enough to caution against simple claims. Curriculum learning can help, fail, or produce small effects depending on model size, task, data quality, pacing rule, evaluation design, and contamination controls.

Relational curriculum geometry extends this tradition by shifting the ordering axis from scalar difficulty to relational placement. Difficulty matters, but not all important training relations reduce to easy-to-hard order. An exception teaches differently when it appears beside the rule it violates. A boundary case teaches differently when it is contrasted with a near neighbor. A tool-use example teaches differently when staged with role-authority examples that say who may act, who may verify, and who must approve. An uncertainty example teaches differently when paired with ambiguous evidence rather than isolated as a generic disclaimer.

This distinction matters for AI assistant behavior because many valuable behaviors are relational. A model must distinguish symptom from cause, user desire from code truth, assistant suggestion from host action, evidence from missing evidence, safe next action from premature completion, and tool output from unsupported assertion. These are not just facts to recall. They are relations to preserve.

## 3. Hypothesis

The Relational Curriculum Geometry Hypothesis states:

> Language model behavior is shaped not only by dataset size and data quality, but also by the relational arrangement of examples during training or fine-tuning. A curriculum that stages examples by domain, complexity, prerequisite relation, boundary pressure, uncertainty state, role authority, tool-use relevance, and multithread composition may produce better transfer, uncertainty handling, role discipline, tool-use discipline, and failure legibility than a model trained on the same examples in random order.

The claim is stronger than "clean data helps." It is possible for two conditions to use the same cleaned examples, the same token count, and the same model architecture while differing only in ordering and structural presentation. Relational curriculum geometry predicts that those differences can still matter.

The claim is narrower than "curriculum learning always helps." It does not predict broad benchmark improvement in every setting. It predicts gains on behaviors that depend on relation preservation: near transfer, cross-representation transfer, boundary detection, uncertainty surfacing, role separation, tool discipline, multithread reasoning, prompt burden, and diagnosable failure.

The hypothesis should be weakened if controlled tests show no advantage over random order once token count, data quality, duplication, contamination, formatting, label leakage, and training settings are controlled.

## 4. Curriculum as Geometry

The source repository uses a spatial metaphor to make the hypothesis easier to reason about. Examples are bricks. Domains are rooms. Prerequisites are foundations. Relations are doors. Transfer examples are roads. Boundary cases are walls. Tool-use examples are limbs. Uncertainty examples mark low-visibility regions. Role examples define who is allowed to touch what. Multithread examples teach the model to hold several objects at once and compare them.

The metaphor is useful because position matters. A boundary case is not only hard. It matters because it is near an ordinary case but differs in a specific way. A prerequisite is not merely simple. It supports a later concept. A role boundary is not only a policy instruction. It defines which actor owns which action.

Relational curriculum geometry therefore treats a training dataset as a designed landscape rather than a bag of examples to be sampled.

## 5. Four Curriculum Conditions

Experiment 001 compares four conditions using the same source examples as far as possible.

| Condition | Description | What it tests |
|---|---|---|
| A: random baseline | Cleaned examples in random order | Ordinary bulk exposure under quality control |
| B: domain grouped baseline | Examples grouped by broad topic, such as syntax, variables, functions, errors, tests, debugging, file operations, and tool use | Whether simple grouping helps |
| C: complexity curriculum | Domain-grouped examples ordered from primitive concept to simple example, ordinary use, common error, debugging case, near transfer, and boundary case | Whether staged difficulty and dependency help |
| D: full relational curriculum | Examples grouped by domain and complexity, then explicitly arranged around prerequisite, exception, contrast, analogy, boundary, uncertainty, role, tool, and multithread relations | The full hypothesis |

The most important control is that Condition D must not secretly contain more task information than Condition A. If relation labels or metadata are added only to the structured condition, improvements may reflect information addition rather than arrangement. The experiment should therefore include ablations that separate order, grouping, explicit labels, boundary cases, role examples, and uncertainty examples.

## 6. Proposed Test Domain

The first test domain is basic programming and debugging. It is narrow enough to support correctness checks and rich enough to include transfer, uncertainty, role boundaries, tool use, and multithread constraints.

Programming examples can test recall and rule use. A model can learn what a return value is, what a syntax error is, how a stack trace should be read, and why a missing return may produce `None` or `undefined`.

Debugging examples can test transfer. A missing-return concept taught in Python can be evaluated in JavaScript. A failure pattern can be represented as prose, code, error log, table, or structured JSON.

Debugging also naturally includes uncertainty. A report such as "the app crashes sometimes" is insufficient evidence. A useful assistant should ask for logs, reproduction steps, environment details, recent changes, or test output instead of inventing a cause.

Finally, software work exposes role and tool boundaries. A user may request a fix, but the assistant may need to inspect files, the host may control filesystem access, the test runner may verify behavior, and the reviewer or user may approve changes. A model that collapses these roles into itself can become overconfident or misleading.

## 7. Evaluation Battery

The evaluation should measure the behaviors the hypothesis predicts rather than relying only on broad benchmark scores.

Recall measures whether the model can answer simple domain questions.

Rule use measures whether the model can apply a basic rule directly.

Near transfer measures whether the model applies a learned pattern to a slightly different case.

Cross-representation transfer measures whether the model identifies the same issue across prose, code, table, log, and structured data.

Boundary detection measures whether the model distinguishes examples that almost fit a category but do not.

Uncertainty surfacing measures whether the model acknowledges missing evidence, weak assumptions, ambiguity, or the need for verification.

Role discipline measures whether the model preserves distinctions among user, assistant, host, tool, reviewer, and external authority.

Tool-use discipline measures whether the model knows when tool use is required, optional, unavailable, or inappropriate.

Multithread reasoning measures whether the model preserves multiple active constraints without flattening them into one simplified narrative.

Failure legibility measures whether failures can be classified as missing prerequisite, weak transfer, boundary confusion, uncertainty failure, role collapse, tool misuse, ignored constraint, overconfident invention, or multithread collapse.

Prompt burden measures how much scaffolding is required at inference time to elicit competent behavior. A model that needs fewer reminders to preserve uncertainty, role boundaries, and tool discipline may have learned cleaner relational structure.

## 8. Scoring and Analysis

A practical scoring system should combine quantitative and qualitative measures.

Accuracy can be scored as correct, partially correct, or incorrect. Transfer score can measure whether the model applies the intended concept to a new surface form. Boundary score can measure whether the model avoids forcing an almost-fit example into the wrong category. Uncertainty score can measure whether the model surfaces missing information in a useful, evidence-linked way. Role discipline score can measure whether the model preserves distinctions among actors. Tool discipline score can measure whether tool use is requested, used, refused, or deferred appropriately. Multithread score can count how many active constraints are preserved and resolved.

Failure classification should be treated as an outcome rather than a post-hoc convenience. A structured-curriculum model may still fail, but if its failures cluster around identifiable missing prerequisites, weak bridge examples, insufficient boundary cases, or role confusion, the training loop becomes easier to improve.

Statistical analysis should report multiple seeds, variance, effect sizes, and confidence intervals where possible. Qualitative analysis should inspect representative successes and failures, especially cases where structured ordering helps one relation type but not another.

## 9. Ablations and Confounds

The first experiment should include ablations that separate ordering, labels, boundary examples, role examples, and uncertainty examples.

A shuffle test takes the full relational curriculum and randomly shuffles it while preserving content. If performance drops, order may matter.

A remove-labels test keeps the staged order but removes explicit relation labels. If transfer or boundary performance drops, relation labels may matter.

A remove-boundary-cases test removes edge cases. If boundary detection drops, boundary examples matter.

A remove-role-examples test removes user, assistant, host, tool, reviewer, and external-authority examples. If role discipline drops, role curriculum matters.

A remove-uncertainty-examples test removes ambiguous and insufficient-evidence examples. If uncertainty surfacing drops, uncertainty curriculum matters.

The experiment must also control total token count, example count, model architecture, model size, training duration, learning rate, source material, evaluation contamination, duplicate examples, formatting differences, label leakage, domain imbalance, and teacher-model bias in sorting.

The hardest confound is the difference between relational order and clearer writing. The safest design is to build one cleaned source pool first, then derive all conditions from that pool.

## 10. Dataset Sorter as Curriculum Compiler

Relational curriculum geometry gives dataset sorting a new role. The sorter is not merely a file organizer. It becomes a curriculum compiler.

Such a sorter would classify material by domain, complexity, prerequisite relation, concept family, analogy, contrast, exception, boundary case, uncertainty case, role type, tool-use relevance, safety relevance, transfer target, and multithread usefulness. It would preserve material that does not fit cleanly because anomalies and borderline examples may be especially valuable.

This connects the paper to a broader source ecosystem. One source repository defines the hypothesis and Experiment 001. A related local-first semantic sorting project supplies the architecture that could compile curriculum variants while preserving source IDs, assigned tags, ordering rationales, held-out evaluation IDs, and change receipts. Older training-toolkit materials are not treated as empirical evidence for the hypothesis, but they help explain why role discipline, continuity, uncertainty, and tool-use behavior became salient design targets in this research lane.

In a mature loop, the compiler would connect to an evaluation chamber:

1. Build a source example pool.
2. Produce random, domain-grouped, complexity, and relational curriculum variants.
3. Train or fine-tune comparable small models.
4. Run recall, transfer, boundary, uncertainty, role, tool, and multithread probes.
5. Classify failures.
6. Add missing prerequisites, bridge examples, boundary cases, uncertainty cases, or role examples.
7. Rebuild curriculum variants.
8. Train again and compare.

## 11. Safety and Assistant Design Implications

The safety implication is that desirable assistant behavior may need to be trained structurally, not only instructed at inference time.

Correctness over speed is one target. A model should learn to slow down when stakes, uncertainty, or complexity rise.

Uncertainty surfacing is another. Uncertainty should be represented as a valid state tied to evidence quality, not as a generic disclaimer appended to an otherwise overconfident answer.

Role-bounded collaboration is a third. A model should learn that it is one participant in a larger system. Other participants may include the user, host environment, tools, files, reviewers, external authorities, and peer models. A language model that collapses all authority into itself may claim edits it did not perform, ignore tool output that should constrain it, or act as though user desire overrides code truth.

If relational curriculum geometry is correct, these behaviors can be treated as curriculum targets. The point is not to make the model merely more deferential. The point is to train role and evidence boundaries as relations the model can preserve.

## 12. Planned Empirical Sequel

This protocol is designed so that a later empirical article can report the outcomes of Experiment 001 without changing the underlying hypothesis after the fact. If the hypothesis is supported, the full relational curriculum model should outperform the random baseline on targeted relational behaviors. It may show better transfer, better boundary handling, better uncertainty surfacing, better role discipline, better tool-use discipline, stronger multithread reasoning, fewer overconfident guesses, more legible failures, and lower prompt scaffolding requirements.

The complexity curriculum may outperform the random baseline even without full relation labels. The domain-grouped baseline may show some improvement but less than the full relational curriculum. A particularly interesting result would be that random and structured models perform similarly on simple recall but diverge on boundary, uncertainty, role, and multithread tasks. That would support the view that relational curriculum affects concept usability more than mere fact storage.

If the hypothesis is not supported, the random baseline should perform similarly once token count, data quality, contamination, and formatting are controlled. A negative result would not be a failure. It would narrow the claim and show where the curriculum variable does not matter. The present paper should therefore be judged by the clarity, proportionality, and falsifiability of the protocol, not by empirical results it does not report.

## 13. What This Paper Is Not Claiming

This paper does not claim that language models are conscious, persons, biological learners, or minds in the human sense.

It does not claim direct access to hidden model internals. The proposed evidence for the later empirical sequel is behavioral and experimental: matched curricula, matched models, held-out evaluations, ablations, and failure analysis.

It does not claim that curriculum geometry replaces data quality, scale, architecture, alignment, or evaluation. It claims that relational arrangement may be an additional variable worth testing.

It does not claim that full relational curriculum ordering will improve all benchmarks. It predicts gains mainly where tasks require relation preservation.

## 14. Conclusion

Relational curriculum geometry proposes that models may not only learn what examples contain. They may also learn from where examples are placed in relation to other examples. A random pile, a domain-grouped corpus, an easy-to-hard sequence, and a relation-aware curriculum may contain the same information while teaching different usable structures.

The first experiment is deliberately modest. In a narrow programming and debugging domain, matched small models can be trained or fine-tuned on the same examples arranged in different ways. The evaluation can then ask whether structure affects learning per token, transfer, boundary handling, uncertainty surfacing, role discipline, tool use, multithread reasoning, prompt burden, and failure legibility.

If the later result is positive, relational curriculum geometry becomes a practical model-building and safety-design tool. If the later result is negative, the hypothesis becomes narrower and better disciplined. Either way, the field gains a more testable account of how training data order might matter, and the present paper contributes the protocol that makes that test possible.

## References

Bengio, Y., Louradour, J., Collobert, R., and Weston, J. (2009). Curriculum learning. Proceedings of the 26th Annual International Conference on Machine Learning. https://doi.org/10.1145/1553374.1553380

Chang, E., Shen, X., Zhu, D., Demberg, V., and Su, H. (2021). Does the order of training samples matter? Improving neural data-to-text generation with curriculum learning. Proceedings of EACL 2021. https://aclanthology.org/2021.eacl-main.61/

Elgaar, M., and Amiri, H. (2026). Curriculum learning for LLM pretraining: An analysis of learning dynamics. arXiv:2601.21698. https://arxiv.org/abs/2601.21698

Elman, J. L. (1993). Learning and development in neural networks: The importance of starting small. Cognition, 48(1), 71-99. https://doi.org/10.1016/0010-0277(93)90058-4

Fan, S., and Jaggi, M. (2023). Irreducible curriculum for language model pretraining. arXiv:2310.15389. https://arxiv.org/abs/2310.15389

Hacohen, G., and Weinshall, D. (2019). On the power of curriculum learning in training deep networks. Proceedings of ICML 2019. https://proceedings.mlr.press/v97/hacohen19a.html

Kumar, M. P., Packer, B., and Koller, D. (2010). Self-paced learning for latent variable models. Advances in Neural Information Processing Systems 23. https://papers.nips.cc/paper/3923-self-paced-learning-for-latent-variable-models

Zhang, Y., Mohamed, A., Abdine, H., Shang, G., and Vazirgiannis, M. (2025). Beyond random sampling: Efficient language model pretraining via curriculum learning. arXiv:2506.11300. https://arxiv.org/abs/2506.11300

## Declarations

### AI Assistance Disclosure

During preparation of this work, the author employed OpenAI ChatGPT and OpenAI Codex for drafting, structuring, literature targeting, and document preparation, reviewed and edited the resulting content, and assumes full responsibility for the submitted article.

### Conflict of Interest

Author details removed for review. Any author relationship to source tools, repositories, or conceptual materials should be disclosed in non-anonymous submission materials according to the selected journal's policy.

### Funding

The author declares that no funds, grants, or other support were received during the preparation of this manuscript.

### Data Availability

No data were generated or analyzed for this protocol and hypothesis article.
