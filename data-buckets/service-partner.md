# Service Partner data bucket

## Service Partner

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the service partner | `string` | `e57836f3-308a-4ba2-b394-1dddcce92ed9` |
| `name` | **REQUIRED**. Name of the service partner | `string` | `Schreiner48 AG` |
| `address` | **REQUIRED** | `string` | `Zürcherstrasse 137d` |
| `zip` | **REQUIRED** | `int` | `8952` |
| `city` | **REQUIRED** | `string` | `Schlieren` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |
| `email` | **REQUIRED** | `string` | `info@schreiner48.ch` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `uid` | Enterprise Identification Number ([UID](https://www.bfs.admin.ch/bfs/en/home/registers/enterprise-register/enterprise-identification/uid-general/uid.html)) | `string` | `CHE-300.515.240` |
| `crafts` | Codes of the crafts the service partner is able to provide services for. | `[string]` | `[carpenter]`, `[35]`, `[78104660-fa22-4b17-a6de-5db3f8cddb70]` |
