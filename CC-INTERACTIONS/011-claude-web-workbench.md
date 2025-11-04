# B"H


UPDATE THE PROMPT TO INCLUDE THE FOLLOWING GUIDANCE:

---

Here is an example of a case where categories SHOULD be consolidated!


specific_category:

```json
  {
    "category":"Release",
    "sample_values":"rel202601 (Release 2026-01), 10, 205, newrel, rel (release), newrel (new release), 1"
  }
```

similar category:
```json
  {
    "category":"Release Version",
    "sample_values":"newrel (new release), pre3 (pre-release 3), 09f, 2025-04 (year-month), 2025-07, 11b, pre4 (pre-release version 4), pre3 (pre-release version 3), 2025-04 (Year-Month), rel-205-10 (release 205.10)"
  }
```

In the above case, they should be consolidated!

- Do NOT say: "hey, they look the sample values reveals important differences: `Release Version` includes pre-release versions (pre3, pre4), date-based versions (2025-04, 2025-07), and version suffixes (09f, 11b), while `Release` focuses on simpler numeric identifiers (10, 205, 1) and basic release status indicators". Do NOT say that. Do NOT use that reasoning. The sample_values and category names are most definitely similar enough in the above case. In the above case, they should be consolidated!


---

INCLUDE THE ABOVE EXAMPLE in the <examples> section in the prompt. It should include the above example explicitly. ultrathink on this PROMPT improvement!