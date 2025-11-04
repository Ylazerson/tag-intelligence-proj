# B"H


UPDATE THE PROMPT TO INCLUDE THE FOLLOWING GUIDANCE:

---

Here is an example of a case where categories SHOULD be consolidated!


specific_category:

```json
  {
    "category":"Release Type",
    "sample_values":"release, newrel (new release), PATCH, feature, patch (patch release), hf (Hotfix), PATCH (patch-level release), patch, bugfix, hotfix"
  }
```

similar category:
```json
  {
    "category":"Release Status",
    "sample_values":"release, beta2, rc (Release Candidate), beta (pre-release/testing version), beta, pre7 (pre-release 7), stable, prerelease, ga (General Availability)"
  }
```

In the above case, they should be consolidated!

- Do NOT say: "hey, they represent distinct dimensions that should remain separate". Do NOT say that. Do NOT use that reasoning. The sample_values and category names are most definitely similar enough in the above case. In the above case, they should be consolidated!


---

INCLUDE THE ABOVE EXAMPLE in the <examples> section in the prompt. It should include the above example explicitly. ultrathink on this PROMPT improvement!