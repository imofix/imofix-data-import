# Shared types

## Address

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `street` | **REQUIRED** | `string` | `Bahnhofstrasse 1` |
| `zip` | **REQUIRED** | `string` | `8000` |
| `city` | **REQUIRED** | `string` | `Zürich` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |

## Person

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the person (or company) | `string` | `ce55be8e-373e-46c1-b52e-cdd2c386074b` |
| `name` | **REQUIRED**. Name of the person | `string` | `imofix.io` |
| `address` |  | [[Address](#address)] |  |
| `email` |  | `string` | `info@schreiner48.ch` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `language` | The person's preferred language | `string` | `en` |
