# Service Partner data bucket

## Service Partner

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the service partner | `string` | `e57836f3-308a-4ba2-b394-1dddcce92ed9` |
| `email` | **REQUIRED** | `string` | `info@schreiner48.ch` |
| `name` | **REQUIRED**. Name of the service partner | `string` | `Schreiner48 AG` |
| `address` | **REQUIRED** | `string` | `Zürcherstrasse 137d` |
| `zip` | **REQUIRED** | `int` | `8952` |
| `city` | **REQUIRED** | `string` | `Schlieren` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `uid` | Enterprise Identification Number ([UID](https://www.bfs.admin.ch/bfs/en/home/registers/enterprise-register/enterprise-identification/uid-general/uid.html)) | `string` | `CHE-300.515.240` |
| `crafts` | Crafts the service partner is able to provide services for. | [[Craft](#craft)] |  |

## Craft

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the craft | `string` | `78104660-fa22-4b17-a6de-5db3f8cddb70`, `35`, `carpenter` |
| `name` | **REQUIRED**. Name of the craft | `string` | `Schreiner` |
