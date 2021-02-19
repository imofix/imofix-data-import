# Resident data bucket

## Resident

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the person | `string` | `1765f98e-5f14-4d6f-ba58-00044ffae3ee` |
| `name` | **REQUIRED** | `string` | `Han Solo`, `imofix.io` |
| `address` | **REQUIRED** | `string` | `Zürcherstrasse 137d` |
| `zip` | **REQUIRED** | `int` | `8952` |
| `city` | **REQUIRED** | `string` | `Schlieren` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |
| `email` | **REQUIRED** | `string` | `han@mill-falcon.com` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `language` | The person's preferred language | `string` | `en` |
