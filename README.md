# imofix-data-import

This gives an overview of how to provide [imofix](https://imofix.io) with the data required to operate the service.

## Data buckets

imofix makes use of the following data:

| Bucket | Content (extract) | Intended use |
| ------------- | ------------- | ----- |
| [Property Portfolio](#property-portfolio) | property, house, unit | Match inquiry to property/house/unit. |
| [Facility Management](#facility-management) | contact data of involved employees (e.g. assistant, manager) | Assign inquiry to responsible person. |
| [Service Partner](#servce-partner) | branch and contact data of service partner | Place orders with service partners (craftsmen, etc.). |
| [Janitor](#janitor) | contact data of responsible janitor | Inform responsible janitor about relevant inquiries. Provide janitor contact to service partners. |
| [Property Owner](#property-owner) | contact data of the property owner | Provide information with orders as relevant invoicing parameter. |
| [Resident](#resident) | contact and contract data of renters and owners | Attach unit to inquiry. Validate inquiry requester. |

At the minimum, the data buckets [Property Portfolio](#property-portfolio) and [Facility Management](#facility-management) are required to operate.

### Property Portfolio

### Facility Management

### Service Partner

### Janitor

### Property Owner

### Resident

## Data transmission

There are several options to provide imofix with the data:

- [Web Service API](#web-service-api)
- [File based exports](#file-based-exports)
- [Self managed data sheet](#self-managed-data-sheet) (Excel, Google Sheet)

### Web Service API

If you have a system which provides some or all of the data, imofix can connect to the system's Web Service API.

### File based exports

Out of the box, imofix supports these formats:

- [JSON](#json)
- [CSV](#csv)

If you're files are formatted differently, imofix can probably support it as well by customizing the import for you.

#### JSON

#### CSV

### Self managed data sheet

The most basic variant it so maintain an Excel file or Google Sheet in the structure defined in [CSV][#csv].
In this variant, updating the data is a manual process. Please get in touch to discuss the details.
