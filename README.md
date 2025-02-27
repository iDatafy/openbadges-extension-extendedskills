# openbadges-extension-extendedskills

This repository contains an Open Badges 3.0 extension that enables issuers to include category and level information related to skills alignments in a lightweight way.

An example of the extension in use:
```json
{
  "@context": [
    "https://www.w3.org/ns/credentials/v2",
    "https://purl.imsglobal.org/spec/ob/v3p0/context-3.0.3.json",
    "{{baseUrl}}v1.json"
  ],
  "id": "urn:uuid:d3e5aeaf-ea53-4a31-a9ed-ecf7a1343193",
  "type": ["VerifiableCredential","OpenBadgeCredential"],
  "issuer": {
    "id": "did:key:z6MkqQ7h8Gq8Zq6Q7Y8",
    "type": [
      "Profile"
    ],
    "name": "Example Skills Academy"
  },
  "validFrom": "2025-01-01T00:00:00Z",
  "credentialSubject": {
    "id": "did:example:ebfeb1f712ebc6f1c276e12ec21",
    "type": [
      "AchievementSubject"
    ],
    "achievement": {
      "id": "urn:uuid:e53b5964-4b19-4f9f-ae91-d42191ae1e14",
      "type": ["Achievement"],
      "name": "Brain Stormer",
      "criteria": {
        "narrative": "This badge is recognized when at least two colleagues observe individual's ability to..."
      },
      "description": "This badge recognizes the development of the capacity to apply brainstorming techniques...",
      "alignment": [
        {
          "targetUrl": "https://skills.emsidata.com/skills/KS122HN7559WPNWPMDML",
          "targetName": "Creative Thinking",
          "targetDescription": "Creative thinking is a skill that involves generating unique ideas...",
          "targetLevel": "Intermediate",
          "targetCategory": "Durable Skills"
        }
      ]
    }
  },
  "credentialSchema": [{
    "id": "{{baseUrl}}schema.json",
    "type": "1EdTechJsonSchemaValidator2019"
  }]
}
```