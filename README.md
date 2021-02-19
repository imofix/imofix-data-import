# Data Import

This gives an overview of how to provide [imofix](https://imofix.io) with the data required to operate the service.

## Data buckets

imofix makes use of the following data:

| Bucket | Content (extract) | Intended use |
| --- | --- | --- |
| [Property Portfolio](data-buckets/property-portfolio.md) | property, house, unit | Match inquiry to property/house/unit. |
| [Facility Management](data-buckets/facility-management.md) | contact data of involved employees (e.g. assistant, manager) | Assign inquiry to responsible person. |
| [Service Partner](data-buckets/servce-partner.md) | branch and contact data of service partner | Place orders with service partners (craftsmen, etc.). |
| [Janitor](data-buckets/janitor.md) | contact data of responsible janitor | Inform responsible janitor about relevant inquiries. Provide janitor contact to service partners. |
| [Property Owner](data-buckets/property-owner.md) | contact data of the property owner | Provide information with orders as relevant invoicing parameter. |
| [Resident](data-buckets/resident.md) | contact and contract data of renters and owners | Attach unit to inquiry. Validate inquiry requester. |

At the minimum, the data buckets [Property Portfolio](#property-portfolio) and [Facility Management](#facility-management) are required to operate.

## Data transmission

There are several options to provide imofix with the data:

- [Web Service API](#web-service-api)
- [File based exports](#file-based-exports)
- [Self managed data sheet](#self-managed-data-sheet) (Excel, Google Sheet)

### Web Service API

If you have a system which provides some or all of the data, imofix can connect to the system's Web Service API.

### File based exports

Out of the box, imofix supports these formats to import data based on your file exports:

- [JSON](import-formats/json.md)
- [CSV](import-formats/csv.md)

If you're files are formatted differently, imofix can probably support it as well by customizing the import for you.

### Self managed data sheet

The most basic variant it so maintain an Excel file or Google Sheet in the structure defined in [CSV](#csv).
In this variant, updating the data is a manual process. Please get in touch to discuss the details.
