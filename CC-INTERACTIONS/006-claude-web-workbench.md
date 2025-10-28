# B"H


I have a very important task for you. 

## Your Task

I need you to create a prompt that will be given pieces of info about a specific AWS Resource Tag:

- 'COMPANY_NAME'
- 'SELECTED_TAG_KEY'
- 'SELECTED_TAG_VAL'
- 'ALL_TAGS'
- 'ALL_TAGS_LENGTH'
- 'PROJECT_ID'
- 'RESOURCE_TYPE_NAME'
- 'RESOURCE_ID'

Here are some examples

```python
[{'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'CSP-Gov-Status-Page',
  'ALL_TAGS': '{\n  "InforCost": "CLD-DOPLB",\n  "Name": "/aws/ecs/cluster/csp-StatusPage-Gov-GOVSTAGE-GOVSTAGE",\n  "Owner": "DLG-CSP-DevOps@infor.com",\n  "Product": "CSSP",\n  "RegFinancialOwner": "Manjunath.Ganimasty@infor.com",\n  "RegTechnicalOwner": "ladislav.pecho@infor.com",\n  "Service": "CSP:StatusPage",\n  "Stage": "GOVSTAGE",\n  "Team": "CSP",\n  "aws:cloudformation:logical-id": "CloudWatchLogsGroup",\n  "aws:cloudformation:stack-id": "arn:aws:cloudformation:us-east-1:116931851636:stack/CSP-Gov-Status-Page/f4936f00-3bf3-11f0-a0fb-0affc932e23d",\n  "aws:cloudformation:stack-name": "CSP-Gov-Status-Page",\n  "faro:deployment": "CSP-Gov-Status-Page"\n}',
  'ALL_TAGS_LENGTH': 587,
  'PROJECT_ID': 116931851636,
  'RESOURCE_TYPE_NAME': 'AWSCloudwatchLogGroup',
  'RESOURCE_ID': 'arn:aws:logs:us-east-1:116931851636:log-group:/aws/ecs/cluster/csp-StatusPage-Gov-GOVSTAGE-GOVSTAGE'},
 {'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'zadara-zms-core-infra-sb',
  'ALL_TAGS': '{\n  "CreatedOn": "2018-12-05",\n  "DeleteOn": "20190603",\n  "InforCost": "DOPLB-CLD",\n  "Name": "zadara-test-us-east-1",\n  "Owner": "luis.lavinajr@infor.com",\n  "Product": "infra",\n  "RegFinancialOwner": "durga.dash@infor.com",\n  "RegTechnicalOwner": "ladislav.pecho@infor.com",\n  "Service": "infra",\n  "faro:deployment": "zadara-zms-core-infra-sb"\n}',
  'ALL_TAGS_LENGTH': 308,
  'PROJECT_ID': 936614981112,
  'RESOURCE_TYPE_NAME': 'AWSEC2Ami',
  'RESOURCE_ID': 'arn:aws:ec2:us-east-1:936614981112:image/ami-0ef0adaada8077693'},
 {'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'zadara-zms-core-sb02',
  'ALL_TAGS': '{\n  "CreatedOn": "2019-11-11",\n  "DeleteOn": "20200509",\n  "InforCost": "DOPLB-CLD",\n  "Name": "zadara-zms-test-b",\n  "Nightly": "exception:database",\n  "Owner": "luis.lavinajr@infor.com",\n  "Product": "infra:storage-zadara",\n  "RegFinancialOwner": "durga.dash@infor.com",\n  "RegTechnicalOwner": "ladislav.pecho@infor.com",\n  "Schedule": "ZMS-infor-sb",\n  "Service": "infra:storage-zadara",\n  "faro:deployment": "zadara-zms-core-sb02"\n}',
  'ALL_TAGS_LENGTH': 387,
  'PROJECT_ID': 936614981112,
  'RESOURCE_TYPE_NAME': 'AWSEC2Ami',
  'RESOURCE_ID': 'arn:aws:ec2:us-east-1:936614981112:image/ami-04239fc017d940e6b'},
 {'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'zadara-zms-softnas-clamav-sb',
  'ALL_TAGS': '{\n  "CreatedOn": "2019-04-13",\n  "DeleteOn": "20191010",\n  "InforCost": "DOPLB-CLD",\n  "Name": "eln-softnas-clamav",\n  "Nightly": "utc-5",\n  "Owner": "luis.lavinajr@infor.com",\n  "Product": "infra",\n  "RegFinancialOwner": "durga.dash@infor.com",\n  "RegTechnicalOwner": "ladislav.pecho@infor.com",\n  "Schedule": "storage-softnas",\n  "Service": "infra:storage",\n  "Team": "infra",\n  "faro:deployment": "zadara-zms-softnas-clamav-sb"\n}',
  'ALL_TAGS_LENGTH': 379,
  'PROJECT_ID': 936614981112,
  'RESOURCE_TYPE_NAME': 'AWSEC2Ami',
  'RESOURCE_ID': 'arn:aws:ec2:us-east-1:936614981112:image/ami-008e7ced69eb5c6bc'},
 {'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'zms-s3bucket-pbc',
  'ALL_TAGS': '{\n  "InforCost": "DMGRJ-PBC",\n  "RegFinancialOwner": "Massimo.Capoccia@infor.com",\n  "RegTechnicalOwner": "Curt.Fish@infor.com",\n  "aws:cloudformation:logical-id": "zmsbucket",\n  "aws:cloudformation:stack-id": "arn:aws:cloudformation:us-east-1:427410248247:stack/s3-bucketzms-s3bucket-pbc/ed7dfbf0-1bd9-11e8-b6df-500c3d441629",\n  "aws:cloudformation:stack-name": "s3-bucketzms-s3bucket-pbc",\n  "faro:deployment": "zms-s3bucket-pbc"\n}',
  'ALL_TAGS_LENGTH': 404,
  'PROJECT_ID': 427410248247,
  'RESOURCE_TYPE_NAME': 'AWSS3Bucket',
  'RESOURCE_ID': 'arn:aws:s3:::infor-pbc-zadara-backups-us-east-1'},
 {'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'zms-securitygroups-infra-pbc',
  'ALL_TAGS': '{\n  "InforCost": "DMGRJ-PBC",\n  "Name": "zadara-sg",\n  "RegFinancialOwner": "Massimo.Capoccia@infor.com",\n  "RegTechnicalOwner": "Curt.Fish@infor.com",\n  "Service": "infra",\n  "aws:cloudformation:logical-id": "ProductSecurityGroup",\n  "aws:cloudformation:stack-id": "arn:aws:cloudformation:us-east-1:427410248247:stack/securitygroupszms-securitygroups-infra-pbc/e04970d0-1bda-11e8-8fe6-50fae98a10fe",\n  "aws:cloudformation:stack-name": "securitygroupszms-securitygroups-infra-pbc",\n  "faro:deployment": "zms-securitygroups-infra-pbc"\n}',
  'ALL_TAGS_LENGTH': 498,
  'PROJECT_ID': 427410248247,
  'RESOURCE_TYPE_NAME': 'AWSEC2SecurityGroup',
  'RESOURCE_ID': 'arn:aws:ec2:us-east-1:427410248247:security-group/sg-a17193d7'}]
```

---

You will ONLY be given one record at a time. 

The goal of the prompt is to guide on trying to explain the given `SELECTED_TAG_VAL` based on the other 7 fields:
- 'COMPANY_NAME'
- 'SELECTED_TAG_KEY'
- 'ALL_TAGS'
- 'ALL_TAGS_LENGTH'
- 'PROJECT_ID'
- 'RESOURCE_TYPE_NAME'
- 'RESOURCE_ID'

---

For example, for the SELECTED_TAG_VAL `'CSP-Gov-Status-Page'` you should try to explain all the components of the SELECTED_TAG_VAL ('CSP', 'Gov', and 'Status-Page' etc.) based on the clues from the other  6 fields:

```
{'COMPANY_NAME': 'Infor',
  'SELECTED_TAG_KEY': 'faro:deployment',
  'SELECTED_TAG_VAL': 'CSP-Gov-Status-Page',
  'ALL_TAGS': '{\n  "InforCost": "CLD-DOPLB",\n  "Name": "/aws/ecs/cluster/csp-StatusPage-Gov-GOVSTAGE-GOVSTAGE",\n  "Owner": "DLG-CSP-DevOps@infor.com",\n  "Product": "CSSP",\n  "RegFinancialOwner": "Manjunath.Ganimasty@infor.com",\n  "RegTechnicalOwner": "ladislav.pecho@infor.com",\n  "Service": "CSP:StatusPage",\n  "Stage": "GOVSTAGE",\n  "Team": "CSP",\n  "aws:cloudformation:logical-id": "CloudWatchLogsGroup",\n  "aws:cloudformation:stack-id": "arn:aws:cloudformation:us-east-1:116931851636:stack/CSP-Gov-Status-Page/f4936f00-3bf3-11f0-a0fb-0affc932e23d",\n  "aws:cloudformation:stack-name": "CSP-Gov-Status-Page",\n  "faro:deployment": "CSP-Gov-Status-Page"\n}',
  'ALL_TAGS_LENGTH': 587,
  'PROJECT_ID': 116931851636,
  'RESOURCE_TYPE_NAME': 'AWSCloudwatchLogGroup',
  'RESOURCE_ID': 'arn:aws:logs:us-east-1:116931851636:log-group:/aws/ecs/cluster/csp-StatusPage-Gov-GOVSTAGE-GOVSTAGE'}
```

For example you can see that `"Team": "CSP"` etc. 

---

The output should be short and concise, first mentioning the AWS Resource Tag Value ("CSP-Gov-Status-Page") and then explaining very briefly what the components of the SELECTED_TAG_VAL mean. 

---
It should NOT guess inappropriately on what components of the SELECTED_TAG_VAL mean. mean. It should ONLY provide commentary on components when it is at-least pretty clear from the clues what it is or it is self-evident (for example in "zms-s3bucket-pbc" the "s3bucket" clearly refers to an AWS S3 Bucket etc. )

