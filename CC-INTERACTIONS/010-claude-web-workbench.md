# B"H


UPDATE THE PROMPT TO INCLUDE THE FOLLOWING GUIDANCE:

Here is an example of a case where categories SHOULD be consolidated!


specific_category:

```json
  {
    "category":"Service/Product",
    "sample_values":"dlr, sce (Service/Product Code), cfs, sce (Infor SCE service), ssb, dor, ionce12 (ION Common Services version 12), ism (ISM), nc (Notification Center subsystem), ifs"
  },
```

similar category:
```json
  {
    "category":"Product/System",
    "sample_values":"ion (ION - Infor's integration platform), hms (Health Management System), rms (Restaurant Management System), gtndo1, eln (ELN Product), wfm (WFM - Workforce Management), ionce, ion (Infor Operating Network), ELN, gtnod1b"
  },
```

In the above case, they should be consolidated!

- Do NOT say: "hey, they look similar BUT they appear to maintain distinct naming conventions that may reflect different semantic purposes. `Service/Product` appears to encompass both services and products as a unified concept, whereas `Product/System` specifically emphasizes products and systems". Do NOT say that. Do NOT use that reasoning. Rather, remember that the category names are not so precise. The most important thing is that the sample_values are very similar and that the category name is similar. The category name doesn't have to exactly similar, it just needs to be similar. The sample_values need to match more closely.

- Additionally, do NOT say: "hey, there are multiple other related categories in the taxonomy (Product/Application, Service/Application, Service/Component) that create a broader ecosystem of similar categories. So I should probably leave as is". Do NOT say that. Do NOT use that reasoning. Rather, remember that the category names are not so precise. The most important thing is that the sample_values are very similar and that the category name is similar. The category name doesn't have to exactly similar, it just needs to be similar. The sample_values need to match more closely.