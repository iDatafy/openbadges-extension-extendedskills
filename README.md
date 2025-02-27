# openbadges-extension-extendedskills

This repository contains an Open Badges 3.0 extension that enables issuers to include category and level information related to skills alignments in a lightweight way.

An example of the extension in use:
```json
{
  "type": "Achievement",
  "alignment": [
{  
    "targetName": "Skill Framework",
    "targetUrl": "https://example.com/skill-framework",
    "targetDescription": "A framework for categorizing skills",
    "targetCode": "SKF",
    "targetCategory": "Category 1",
    "targetLevel": "Level 1",
    "targetFramework": "https://example.com/skill-framework/level1",
}
  ]
}
```