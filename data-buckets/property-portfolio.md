# Property Portfolio data bucket

## Property

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the property | `string` | `41145`, `7e629e45-c6e7-4dc8-b8e5-c37f4cba91e1` |
| `name` | **REQUIRED**. Name of the property | `string` | `Überbauung Immergrün` |
| `zip` | **REQUIRED** | `int` | `8952` |
| `city` | **REQUIRED** | `string` | `Schlieren` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |
| `houses` | **REQUIRED**. List of the property's houses | [[House](#house)] |  |
| `managers` | **REQUIRED**. List of the persons responsible for the property | [[Property Manager](facility-management.md#property-manager)] |  |
| `branch` | Branch office managing the property | [Branch](facility-management.md#branch) |  |
| `type` | Code for the property's type | `string` | `residential`, `commercial` |
| `contract` | Code for the property's contract type (service agreement) | `string` | `tech` |
| `reference` | Reference to display to the facility managers | `string` | `41145` |
| `contractors` | List of the preferred contractors (service partners) | [[Property Contractor](#property-contractor)] |  |
| `janitors` | List of the property's janitors | [[Property Janitor](#property-janitor)] |  |

## House

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the house (building) | `string` | `41145.01` or `3aef9a13-6dba-4be8-8f09-57ebf3ad71c3` |
| `address` | **REQUIRED** | `string` | `Zürcherstrasse 137d` |
| `zip` | **REQUIRED** | `int` | `8952` |
| `city` | **REQUIRED** | `string` | `Schlieren` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |
| `units` | List of the house's units | [[Unit](#unit)] |  |
| `type` | Code for house's type (to differentiate types of buildings) | `string` | `01`, `parking` |
| `reference` | Reference to display to the facility managers | `string` | `41145.01` |
| `egid` | Swiss EGID ([Gebäudeidentifikator](https://www.bfs.admin.ch/bfs/de/home/register/personenregister/registerharmonisierung/egid-ewid.html)) | `int` | `190630248` |
| `janitors` | List of the house's janitors | [[Janitor](janitor.md#janitor)] |  |

## Unit

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the unit | `string` | `41145.01.01`, `1d329098-cb16-4cbb-95b2-e5961ffa2537` |
| `floor` | Code for the unit's floor (storey) | `string` | `EG` |
| `size` | Code for the unit's size | `string` | `3.5` |
| `type` | Code for the unit's type | `string` | `flat` |
| `reference` | Reference to display to the facility managers | `string` | `41145.01.01` |
| `ewid` | Swiss EWID ([Wohnungsidentifikator ](https://www.bfs.admin.ch/bfs/de/home/register/personenregister/registerharmonisierung/egid-ewid.html)) | `int` | `13` |
| `residents` | List of residents living in the unit | [[Resident](resident.md#resident)]  |  |

## Property Contractor

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `service_partner` | **REQUIRED** | [Service Partner](service-partner.md#service-partner) |  |
| `crafts` | Crafts for which the service partner is the preferred contractor. | [[Craft](service-partner.md#craft)] |  |

## Property Janitor

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `janitor` | **REQUIRED** | [Janitor](janitor.md#janitor) |  |
| `main` | Is the janitor the main one? | `bool` | `false` |
