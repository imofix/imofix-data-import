# Facility Management data bucket

## Property Contact

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `first_name` | **REQUIRED** | `string` | `Luke` |
| `last_name` | **REQUIRED** | `string` | `Skywalker` |
| `gender` |  | `string` | `male` |
| `email` | **REQUIRED** | `string` | `luke@jedi.org` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `language` | The person's preferred language | `string` | `en` |
| `roles` | The codes for the person's roles (for the given property) | `[string]` |  |

## Branch

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `name` | **REQUIRED** | `string` | `Filiale Zürich` |
| `company` | **REQUIRED** | `string` | `imofix.io` |
| `address` | **REQUIRED** | `string` | `Bahnhofstrasse 1` |
| `zip` | **REQUIRED** | `int` | `8000` |
| `city` | **REQUIRED** | `string` | `Zürich` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |
| `email` | **REQUIRED** | `string` | `info@imofix.io` |
| `phone` |  | `string` | `+41 12 345 67 89` |
