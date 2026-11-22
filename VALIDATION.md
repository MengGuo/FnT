# Validation of the audit corrections

Date: 22 November 2026. The manuscript and response sources were edited directly.
The mathematical corrections are recorded below. Numerical experiment results were
not recomputed; the implementation and provenance checks remain in
`AUTHOR_QUESTIONS.md`.

## Build and consistency checks

- `tex/root.tex`: successful PDF build, 164 physical pages.
- `1st_response/author_response.tex`: successful PDF build, 24 pages.
- Final logs contain no undefined citations/references, duplicate labels, overfull
  boxes, or LaTeX errors. BibTeX reports no warnings. The manuscript retains the
  unrelated unused table-caption setup warning.
- All 24 quoted question blocks are unchanged up to whitespace.
- All 23 actual-change lists have the required lead-in and use `itemize`.
- The response has no starred subsection headings and no line exceeds 90 characters.
- All 142 substantive blue excerpt spans normalize to the manuscript source. The
  other 18 blue spans are location references, including the Eq. (3.19) locator.
- Excerpt locations were checked against compiled source positions and page labels,
  with manual checks for multi-location sentences, the abstract's roman page number,
  and the Wolff/Maity bibliography pages.
- The editor's full answer now fits on the opening page, followed by the requested
  page break. The opening and corrected probability page were visually inspected.
- No newly added visible source text was found outside revision treatment relative
  to the first-draft commit. Bibliographic author changes are accompanied by blue
  complete citing sentences and blue bibliography entries.
- Display punctuation and following `where` explanations pass the source check;
  a label and an enclosing `subequations` wrapper are skipped before reading the
  following explanation. No first-person pronouns or `\ldots` occur in main text.
- `git diff --check` passes. Figure and original-label checks are documented in
  `SOURCE_INTEGRITY.md`.

## Resolution of technical findings

| Finding | Applied correction |
|---|---|
| T01 | Atomic tasks use singleton alphabet letters, projected to each mission's alphabet; empty reachable-state children are rejected and complete traces are verified. |
| T02 | Nontrivial decompositions use sequential retained-path checks; the lemma states graph reachability and subautomaton soundness, not language equivalence. |
| T03 | The exclusion-set method is explicitly restricted to compatible negative self-loop guards; full Boolean guards remain in the original automaton. |
| T04 | An accepted frozen-cost switch cannot increase the affected maximum and must strictly reduce the affected sum; moving-target convergence is not asserted. |
| T05 | ComOpt initializes every position and the maximum navigation arrival time; its loop runs without an equal-time entry test and reports failed initialization. |
| T06 | Every accepted event checks the entire communication graph, rather than one anchor edge. |
| T07 | The cycle result concerns the explored verified candidates; stationarity/ergodicity are not used to assert infinite-horizon optimality. |
| T08 | Timely deliveries are reserved and checked before replacement; late candidates are trimmed, rejected, or replaced by the certified fallback, with explicit failure if none exists. |
| T09 | Task and return values use first-hit probabilities and accepting continuations; recoverability is state-wise and is enforced through the baseline and lifted option checks. |
| T10 | VaR uses the lower-CDF quantile convention; CVaR uses the general-distribution optimization form for confidence levels strictly below one. |
| T11 | Joint forecast coverage uses a union bound without independence, with stated exchangeability, valid future speed, positive closing speed, and pursuit assumptions; the scenario law is an explicit input. |
| T12 | Completion bookkeeping and residual-plan evaluation replace the mixed formula/subtask quotient and clock-tick decrement of an absolute completion-time metric. |
| T13 | The collective plan consistently contains tau_1 through tau_N. |
| T14 | Simple-path seed enumeration is finite but not generally complete; tested words are distinct from the R-poset language and only verified schedules are returned. |
| T15 | Dominance comparisons require aligned dimensions and a valid continuation relation; otherwise nodes are retained and the profile only orders exploration. |
| T16 | Complete leaves must pass disjoint formation and local-execution checks; failed leaves are rejected and alternative candidates may be explored. |

Downstream complexity descriptions, execution conditions, R-poset composition,
symbol meanings, and response excerpts were updated to match these restrictions.

## Mathematical counterexample checks

The following checks passed independently of the unavailable experiment code:

- Sequential retained-path deletion preserved initial-to-target reachability on all
  512 directed graphs with three vertices.
- A positive self-loop guard was correctly identified as outside the exclusion-set
  representation.
- All 416 accepted small frozen-cost pair updates in the enumerated test decreased
  the full maximum-plus-mean objective.
- The travel-time and articulation-vertex communication counterexamples were rejected
  by the corrected initialization and full-graph tests.
- An already-late return failed the deadline test.
- Initial hit, later hit, and no-hit trajectories counted at most one first-hit event.
- A reachable low-return-probability state could not be hidden by averaging.
- A discrete two-point cost distribution gave the correct CVaR with quantile mass.
- The dependent-coverage counterexample was covered by the union bound; nonpositive
  closing speed was excluded.
- The performance update no longer divides a formula count by a subtask count.

These checks validate the specific mathematical correction patterns. They do not
certify that the historical experiments implemented the revised procedures.
