# Nine Core Questions Paper Review

Structured, rigorous analysis of academic papers using the **Nine Core Questions** framework. This skill produces critical reviews that distinguish between what the paper states, what can be inferred, and what requires further verification.

## Core Principle: Epistemic Rigor

Every substantive claim in your analysis must have a clear epistemic status:

| Status | Meaning | Formatting |
|--------|---------|------------|
| **Explicit** | Directly stated in the paper, with a section, figure, table, or equation anchor when available | No label required; cite the paper location |
| **[Inferred]** | Deduced from paper content but not directly stated | Mark with `[Inferred]` |
| **[Needs Verification]** | Cannot be confirmed from the paper alone | Mark with `[Needs Verification]` |

When in doubt, prefer the more cautious status. Never present inferences or external facts as paper-grounded statements.

**External verification rule:** External facts not directly supported by the paper require verification. If not verified, mark them `[Needs Verification]`.

---

## Workflow: Analyzing a Paper

```
Paper Review Progress:
- [ ] Step 0: Obtain and read the paper
- [ ] Step 1: Problem — What problem does the paper aim to solve?
- [ ] Step 2: Hypotheses — What scientific hypotheses does this paper intend to test?
- [ ] Step 3: Related Work — What existing relevant studies are there?
- [ ] Step 4: Solution — What are the key points of the proposed solution?
- [ ] Step 5: Experiments — How are the experiments designed?
- [ ] Step 6: Datasets & Code — What datasets are used? Is code publicly available?
- [ ] Step 7: Evidence — Do experiments strongly support the hypotheses?
- [ ] Step 8: Contributions — What are the core contributions?
- [ ] Step 9: Future Work — What deeper follow-up research could be conducted?
- [ ] Step 10: Compile final structured review
```

---

## Step 0: Obtain and Read the Paper

Before analysis, ensure you have access to the full paper content.

**Supported input methods:**
- User provides a PDF file path → read with available PDF extraction or document-reading tools
- User provides an arXiv ID, DOI, or URL → fetch via web/search tools when available
- User pastes paper text directly into conversation
- User provides a local `.tex` or `.md` file

**First pass — skim for structure:**
- Read title, abstract, introduction, and conclusion first
- Identify the number of sections, figures, and tables
- Note the reference count and key cited works as reported in the paper

**Second pass — detailed reading:**
- Read each section carefully
- Note key claims, equations, algorithms, and results
- Track where evidence is presented vs. where claims are made without support
- Record evidence anchors such as section numbers, table numbers, figures, equations, or quoted phrases

---

## The Nine Core Questions

### Q1: What problem does the paper aim to solve?

Identify and articulate:
- The specific problem or challenge addressed
- Why this problem matters (motivation)
- The gap in existing solutions that this paper fills
- The scope and boundaries of the problem as defined by the authors

**Output format:**
```
## Q1: Problem Definition

**Problem**: [One-sentence problem statement]

**Motivation**: [Why this problem matters — practical or theoretical significance]

**Gap**: [What existing approaches fail to address]

**Scope**: [Boundaries and constraints the authors set]

**Epistemic notes**:
- [Inferred] ...any inferences about unstated motivations...
- [Needs Verification] ...any claims that need external confirmation...
```

### Q2: What scientific hypotheses does this paper intend to test?

Extract the hypotheses — both explicit and implicit:
- Explicitly stated hypotheses or research questions
- Implicit hypotheses embedded in the experimental design
- The relationship between hypotheses and the proposed solution

**Key distinction**: Many papers do not state formal hypotheses. In such cases, reconstruct the implicit hypotheses from the experimental design and claims, and mark them clearly as `[Inferred]`.

**Output format:**
```
## Q2: Scientific Hypotheses

**Explicit hypotheses:**
1. H1: [hypothesis as stated in paper]
2. H2: ...

**Implicit hypotheses** [Inferred]:
1. H3: [reconstructed from experimental design]
2. H4: ...

**Hypothesis-method mapping:**
| Hypothesis | Method/Experiment that tests it |
|------------|-------------------------------|
| H1         | Experiment in Section X       |
| H2         | Ablation study in Table Y     |
```

### Q3: What existing relevant studies are there?

Analyze the related work landscape without inventing external field facts:
- How the authors categorize prior work
- Key research groups and researchers named or cited by the paper
- Which works are emphasized, compared against, or built upon
- Notable omissions in the related work section

**Output format:**
```
## Q3: Related Work Landscape

**Categorization by the authors:**
1. Category A: [description] — key works: [refs]
2. Category B: ...

**Key researchers or groups named by the paper:**
- [Name or group] — connected work or contribution as described by the paper
- ...

**Most emphasized cited works:**
1. [Paper] — used as [baseline/foundation/comparison]
2. ...

**Notable omissions** [Inferred]:
- [Area or paper that seems relevant but is not discussed]

**Needs verification:**
- [Any external claims not directly supported by the paper]
```

### Q4: What are the key points of the proposed solution?

Dissect the technical approach:
- Core idea or insight (in one sentence)
- Technical components and how they interact
- Key design decisions and their justifications
- Novelty — what is genuinely new vs. combining existing techniques
- Theoretical guarantees (if any)

**Output format:**
```
## Q4: Proposed Solution

**Core insight**: [One sentence capturing the key idea]

**Technical components:**
1. [Component A]: [description and role]
2. [Component B]: ...

**Key design decisions:**
| Decision | Justification given | Alternative considered |
|----------|--------------------|-----------------------|
| ...      | ...                | ...                   |

**Novelty assessment:**
- Genuinely new: [what is original]
- Combined from existing work: [what is assembled from prior art]
- [Inferred] [any unstated design rationale]

**Theoretical properties:**
- [Any formal guarantees, complexity bounds, convergence proofs]

**Evidence anchors:**
- [Sections, equations, figures, or algorithms supporting the analysis]
```

### Q5: How are the experiments designed?

Evaluate experimental methodology:
- What is being measured and why
- Baselines and comparisons chosen
- Experimental controls and variables
- Statistical methodology (error bars, significance tests, number of runs)
- Potential confounds or methodological weaknesses

**Output format:**
```
## Q5: Experimental Design

**Experiments overview:**
| Experiment | Tests hypothesis | Metric | Baselines |
|-----------|-----------------|--------|-----------|
| Exp 1     | H1              | ...    | ...       |
| Exp 2     | H2              | ...    | ...       |

**Controls and variables:**
- Independent variables: ...
- Dependent variables: ...
- Controlled variables: ...

**Statistical rigor:**
- Error bars: [present/absent, type]
- Number of runs: [N]
- Significance tests: [present/absent, type]

**Methodological concerns** [Inferred]:
- [Any potential confounds or weaknesses]

**Evidence anchors:**
- [Tables, figures, appendices, or experiment sections used]
```

### Q6: What datasets are used? Is source code publicly available?

Document reproducibility:
- Datasets used (name, size, source, preprocessing)
- Whether datasets are public or proprietary
- Code availability and completeness
- Compute requirements
- Sufficient detail for reproduction

**Output format:**
```
## Q6: Datasets and Reproducibility

**Datasets:**
| Dataset | Size | Public | Preprocessing | Used for |
|---------|------|--------|---------------|----------|
| ...     | ...  | Yes/No | ...           | ...      |

**Code availability:**
- Publicly available: [Yes/No/Partial]
- Repository: [URL if provided]
- Includes: [training code / eval code / pretrained models / configs]

**Compute requirements:**
- Hardware: [GPU type, count]
- Training time: [hours/days]
- [Needs Verification] [if compute details are incomplete]

**Reproducibility assessment:**
- [Sufficient / Partially sufficient / Insufficient] for independent reproduction
- Missing details: [list any gaps]
```

### Q7: Do experiments and results strongly support the hypotheses?

Critical evaluation of evidence:
- For each hypothesis, assess whether the evidence is convincing
- Identify results that support vs. contradict the claims
- Evaluate the strength of evidence (strong, moderate, weak)
- Note any cherry-picking, unfair comparisons, or missing experiments

**Output format:**
```
## Q7: Evidence Assessment

**Hypothesis-evidence mapping:**
| Hypothesis | Supporting evidence | Contradicting evidence | Strength |
|-----------|--------------------|-----------------------|----------|
| H1        | Table 2, Fig 3     | None observed         | Strong   |
| H2        | Table 4            | Partial — see Sec 5.3 | Moderate |

**Strongest results:**
- [Result that most convincingly supports the main claim]

**Weakest points:**
- [Result that is least convincing or potentially problematic]

**Missing experiments** [Inferred]:
- [Experiments that would strengthen or weaken the claims]

**Overall verdict**: [Do the experiments convincingly support the paper's claims?]

**Evidence anchors:**
- [Primary result tables, figures, ablations, or appendix sections]
```

### Q8: What are the core contributions of this paper?

Summarize the lasting impact:
- Technical contributions (methods, algorithms, architectures)
- Empirical contributions (benchmarks, datasets, findings)
- Theoretical contributions (proofs, bounds, frameworks)
- Practical contributions (tools, systems, applications)

**Output format:**
```
## Q8: Core Contributions

**Primary contribution**: [The single most important contribution]

**Secondary contributions:**
1. [Contribution 2]
2. [Contribution 3]

**Contribution type breakdown:**
| Contribution | Type | Evidence anchor | Significance |
|-------------|------|-----------------|-------------|
| ...         | Technical / Empirical / Theoretical / Practical | Section/Table/Figure | High / Medium / Low |

**[Inferred] Understated contributions:**
- [Contributions the authors don't emphasize but are valuable]
```

### Q9: What deeper follow-up research could be conducted?

Identify research directions:
- Future work explicitly suggested by the authors
- Extensions and improvements inferred from limitations
- New research questions raised by the findings
- Potential applications in other domains

**Output format:**
```
## Q9: Future Work Directions

**Suggested by authors:**
1. [Direction as stated in paper]
2. ...

**Inferred from limitations** [Inferred]:
1. [Direction based on identified weaknesses]
2. ...

**New research questions** [Inferred]:
1. [Question raised by the findings]
2. ...

**Cross-domain applications** [Inferred]:
- [Potential applications the authors don't discuss]
```

---

## Step 10: Compile Final Review

After completing all nine questions, produce a structured summary:

```
## Paper Review Summary

**Paper**: [Title]
**Authors**: [Author list]
**Venue/Year**: [Where published or preprint]
**Source reviewed**: [PDF/arXiv/URL/local file and access date if relevant]

### One-Paragraph Summary
[3-5 sentences capturing problem, approach, key result, and significance]

### Strengths
1. [Major strength]
2. ...

### Weaknesses
1. [Major weakness]
2. ...

### Epistemic Summary
- Explicit paper-grounded claims: [count]
- Inferences made: [count]
- Items needing verification: [count]

### Verification Gaps
1. [External fact or missing paper detail that still needs checking]
2. ...

### Verdict
[Overall assessment: significance, soundness, clarity, novelty — 2-3 sentences]
```

---

## Guidelines for Different Paper Types

| Paper Type | Emphasis | Watch For |
|-----------|----------|-----------|
| **Empirical** | Q5-Q7 (experiments, evidence) | Cherry-picked results, missing baselines |
| **Theoretical** | Q2, Q4 (hypotheses, proofs) | Assumption validity, proof gaps |
| **Systems** | Q4, Q6 (design, reproducibility) | Scalability claims, deployment details |
| **Survey** | Q3 (related work landscape) | Coverage completeness, taxonomy quality |
| **Benchmark** | Q6, Q7 (datasets, evaluation) | Metric selection bias, dataset leakage |

---

## Language

- Produce the review in the same language the user uses when invoking this skill
- Technical terms, method names, and dataset names remain in their original form regardless of output language
- When the user provides a paper in a different language than their request, follow the user's language for the review

---

## Common Pitfalls to Avoid

| Pitfall | Why It's Bad | Instead |
|---------|-------------|---------|
| Summarizing without evaluating | Review ≠ summary | Always assess strength of evidence |
| Treating all claims as explicit | Misrepresents epistemic status | Tag inferences and unverified claims |
| Inventing external context | Creates unsupported authority | Verify externally or mark `[Needs Verification]` |
| Ignoring negative results | Misses important signals | Note what didn't work and why |
| Overlooking methodology details | Misses reproducibility issues | Check statistical rigor, compute, data |
| Accepting author framing uncritically | May miss alternative interpretations | Consider what the results could also mean |
