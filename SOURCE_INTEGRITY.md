# Source integrity after audit corrections

The changes are confined to the response, active manuscript statements and notation,
associated bibliography records, and revision/validation documentation.

- All 27 existing files under `tex/figures/` retain their pre-correction SHA-256 hashes.
- All original manuscript labels are retained; no original cross-reference target
  was removed. Algorithm line numbers may change as their pseudocode changes.
- All 24 quoted question blocks retain their wording, including the quoted word
  `monograph`. Whitespace was reflowed to meet the response line-length limit.
- All original bibliography keys remain available in the active or held database.
  Two verified duplicate keys were moved to the held database rather than discarded.
  The new CVaR reference brings the combined record count to 536.
- There are 452 active records and 84 held records; only the active database is loaded.
- Original figures and reported numerical results were not replaced or regenerated.
- Pre-existing unrelated working-tree changes were left untouched.

The response's obsolete internal certification and author-question appendices were
removed. Its reviewer-facing additional technical corrections contain source excerpts;
remaining external evidence requests are kept in `AUTHOR_QUESTIONS.md`.
