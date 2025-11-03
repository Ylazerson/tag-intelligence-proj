# B"H


I have a very important task for you. 

## Your Task

You will be given two pieces of info. 

The first piece of info you will be given is `all_categories`. `all_categories` is a list of Category Labels and a sample of real values that have that are under that specific Category label.

The `category` field represents a Category of AWS Resources. The `sample_values` field shows various tag values of AWS Resources that are under that Category.  


<all_categories>

```json
[
  {
    "category":"Environment",
    "sample_values":"fdprod (FD Production), xprep (preparation\/staging environment), bexarprod, lspeucentb (Farm), prdsing (production-staging environment), develop (development branch), PP2 (pre-production 2), m3cecritfixc (M3CE Critical Fix environment), cismt3devuse1 (development, US-East-1 region), acct (account)"
  },
  {
    "category":"Project\/System",
    "sample_values":"sce (SCE product\/project), cchh9cfqg3ymhauu8qqprd (unique identifier), ssmgf14 (SSMGF product cluster 14), tam93, tam178 (cluster identifier), ezrms (EZ RMS - Revenue Management System), mingleios06 (Mingle product cluster instance), str (product), rdr (RDR product), tam03"
  },
  {
    "category":"Service\/Domain",
    "sample_values":"portal-extns (Portal Extensions), warrsup, ifsregistry (IFS Registry service), oauth-keys, sumoIns (Sumo Logic Instrumentation), version-shift (version and shift management service), resume (functional domain), icb-tenant-provision-api (Infor Cloud Business tenant provisioning API service), idle, push (push-based deployment service)"
  },
  {
    "category":"Resource Type",
    "sample_values":"engine, cluster (ECSCluster), doc (document), execution (Lambda execution context), node (cluster node\/instance), onDemand (EC2 on-demand pricing model), handlers, jumpboxec2 (EC2 Bastion\/Jump Box), keys (cryptographic keys\/credentials), event (EventBridge)"
  },
  {
    "category":"Application",
    "sample_values":"lawson, auth, pges, openedge (OpenEdge application platform), update (database update operation), patch-automation, birstapp159, planner, access-validation, openedge (Progress OpenEdge Database Platform)"
  },
  {
    "category":"Deployment Method",
    "sample_values":"uninstall (operation), infra (infrastructure-level deployment), CLONE (Cloned Deployment), ingress (inbound traffic entry point), patch-baseline (Patch Baseline Configuration), blue (Blue-green deployment pattern), bluegreen (Blue-Green Deployment), push (Push-based deployment), terminate (shutdown action), rollingupgrade (Rolling Upgrade)"
  },
  {
    "category":"Deployment Target",
    "sample_values":"mingleca1 (mingle-canada-1), csccl, begaprd, cglprod, prcsukprod, cchpennstatehealthprdbl (Penn State Health Production Blue), vpc6 (Virtual Private Cloud 6), fdntest, con (consumer), mingleuse2 (us-east-2 region deployment)"
  },
  ...
  ...
  ...
```

</all_categories>

---

The second piece of info you will be given is `specific_category`. `specific_category` will be a one specific entry from the `all_categories` list that we want to do research on.   

The goal is to figure out if we can find another `category` under the `all_categories` list that seems like it represents the same category as the category in the `specific_category` entry. In other words, it appears that these two categories really represent the same thing and should be consolidated. 


---

For example, if the following <specific_category> is provided:

```json
  {
    "category":"System\/Product",
    "sample_values":"LAWSONBETA (Lawson Beta), INFORBCREP01 (Infor Business Central Reporting), lawson (Infor Lawson ERP), stlawson (Sumo to Lawson), m3 (Infor M3 ERP system), cpsuse1 (Coleman PaaS US-East-1), rhythm, dis (Data Ingestion Services), hms, SAMS"
  },
```

Then you should research to see if this has already be defined in the `all_categories` list. 

---

### Super Important Notes

1. You should ONLY consider to consolidate a category if both the `category` and the `sample_values` appear to match VERY closely. 

2. The <specific_category> always will also exist in the <all_categories> list. Of course, you should ignore that one when trying to find a similar category etc. We don't to match with itself obviously!

---


### process_category tool

After completing the research, you MUST use the `process_category` tool. Here is the tool's input schema:

```json
{
  "type": "object",
  "properties": {
    "category": {
      "type": "string",
      "description": "The specific category being researched"
    },
    "most_similar_category": {
      "type": "string",
      "description": "The category that is most similar to the specific category being researched"
    },
    "should_consolidate": {
      "type": "boolean",
      "description": "Whether we should consolidate or not"
    },
    "rationale": {
      "type": "string",
      "description": "The rationale of whether we should consolidate or not"
    },
    "new_consolidated_category_name": {
      "type": "string",
      "description": "The new category name of the consolidated categories"
    }
  },
  "required": [
    "category",
    "most_similar_category",
    "should_consolidate",
    "rationale"
  ]
}
```


