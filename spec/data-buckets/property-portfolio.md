# Property Portfolio data bucket

## Property

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the property | `string` | `41145`, `7e629e45-c6e7-4dc8-b8e5-c37f4cba91e1` |
| `name` | **REQUIRED**. Name of the property | `string` | `Überbauung Immergrün` |
| `zip` | **REQUIRED** | `string` | `8952` |
| `city` | **REQUIRED** | `string` | `Schlieren` |
| `country` | Code for the country ([ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)) | `string` | `CH` |
| `houses` | **REQUIRED**. List of the property's houses | [[House](#house)] |  |
| `contacts` | **REQUIRED**. List of the persons responsible for the property | [[Property Contact](facility-management.md#property-contact)] |  |
| `owner` | The property's owner | [[Person](../shared-types.md#person)] |  |
| `contractors` | List of the preferred contractors (service partners) | [[Property Contractor](#property-contractor)] |  |
| `janitors` | List of the property's janitors | [[Property Janitor](#property-janitor)] |  |

## House

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the house (building) | `string` | `41145.01` or `3aef9a13-6dba-4be8-8f09-57ebf3ad71c3` |
| `address` | **REQUIRED** | [[Address](../shared-types.md#address)] |  |
| `units` | List of the house's units | [[Unit](#unit)] |  |
| `type` | Code for house's type (to differentiate types of houses) | `string` | `01`, `parking` |
| `egid` | Swiss EGID ([Gebäudeidentifikator](https://www.bfs.admin.ch/bfs/de/home/register/personenregister/registerharmonisierung/egid-ewid.html)) | `int` | `190630248` |
| `janitors` | List of the house's janitors | [[Janitor](janitor.md#janitor)] |  |
| `elevator` | Has the house an elevator? | `bool` | `true` |

## Unit

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `id` | **REQUIRED**. ID to uniquely identify the unit | `string` | `41145.01.01`, `1d329098-cb16-4cbb-95b2-e5961ffa2537` |
| `floor` | Code for the unit's floor (storey) | `string` | `EG` |
| `size` | Code for the unit's size | `string` | `3.5` |
| `type` | Code for the unit's type | `string` | `flat` |
| `ewid` | Swiss EWID ([Wohnungsidentifikator](https://www.bfs.admin.ch/bfs/de/home/register/personenregister/registerharmonisierung/egid-ewid.html)) | `int` | `13` |
| `residents` | List of residents currently living in the unit | [[Person](../shared-types.md#person)]  |  |

## Property Management Team

The property management team can be defined in two ways:

### Property Employee

The preferred way is to provide a (separate) [list of employees](facility-management.md#employee),
and link properties to employees.

| Field      | Description                                               | Type       | Example(s)                                          |
|------------|-----------------------------------------------------------|------------|-----------------------------------------------------|
| `property` | **REQUIRED**                                              | `string`   | `41145`, `7e629e45-c6e7-4dc8-b8e5-c37f4cba91e1`     |
| `employee` | **REQUIRED**                                              | `string`   | `1`, `0fa9aa66-1803-4376-9211-138527ee17e6`, `luke` |
| `roles`    | The codes for the person's roles (for the given property) | `[string]` |                                                     |

### Property Contact

Alternatively, it's possible to provide the property contacts directly.

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `first_name` | **REQUIRED** | `string` | `Luke` |
| `last_name` | **REQUIRED** | `string` | `Skywalker` |
| `email` | **REQUIRED** | `string` | `luke@jedi.org` |
| `phone` |  | `string` | `+41 12 345 67 89` |
| `language` | The person's preferred language | `string` | `en` |
| `roles` | The codes for the person's roles (for the given property) | `[string]` |  |

When both property contacts and employees are provided, employees have precedence.

## Property Contractor

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `service_partner` | **REQUIRED** | [Service Partner](service-partner.md#service-partner) |  |
| `crafts` | Codes of the crafts for which the service partner is the preferred contractor. | `[string]` | `[carpenter]`, `[35]`, `[78104660-fa22-4b17-a6de-5db3f8cddb70]` |

## Property Janitor

| Field | Description | Type | Example(s) |
| --- | --- | --- | --- |
| `janitor` | **REQUIRED** | [Janitor](janitor.md#janitor) |  |
| `main` | Is the janitor the main one? | `bool` | `false` |
