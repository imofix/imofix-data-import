# Janitor data bucket

## Janitor

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the janitor (company) | `string` | `4fc4847d-469d-42a1-9cde-d6f13e7341c4` |
| `name` | **REQUIRED**. Name of the janitor | `string` | `Schreiner48 AG` |
| `address` | **REQUIRED** | [[Address](../shared-types.md#address)] |  |
| `email` | **REQUIRED** | `string` | `info@schreiner48.ch` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `language` | The janitor's preferred language | `string` | `en` |
| `uid` | Enterprise Identification Number ([UID](https://www.bfs.admin.ch/bfs/en/home/registers/enterprise-register/enterprise-identification/uid-general/uid.html)) | `string` | `CHE-300.515.240` |
