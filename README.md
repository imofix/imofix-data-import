# Data Import

This gives an overview of how to provide [imofix.io](https://imofix.io) with the data required to operate the service.

## Data buckets

imofix.io makes use of the following data (if available):

| Bucket | Content (extract) | Intended use |
| --- | --- | --- |
| [Property Portfolio](spec/data-buckets/property-portfolio.md) | property, house, unit | Match inquiry to property/house/unit. |
| [Service Partner](spec/data-buckets/service-partner.md) | contact data of service partner | Place orders with service partners (craftsmen, etc.). |
| [Janitor](spec/data-buckets/janitor.md) | contact data of responsible janitor | Inform responsible janitor about relevant inquiries. Provide janitor contact to service partners. |

In the data buckets, there are many fields which allow to provide your codes
(e.g. `03` as `property.house.type` for a parking garage).
The idea is that you provide imofix with the necessary code tables as well, so your data can be mapped to imofix.io's representation.

## Data transmission

There are several options to provide imofix.io with the data:

- [Web Service API](#web-service-api)
- [File based exports](#file-based-exports)
- [Self managed data sheet](#self-managed-data-sheet) (Excel, Google Sheet)

### Web Service API

If you have a system which provides some or all of the data, imofix.io can connect to the system's Web Service API.

The Web Service API needs to be accessible from the public internet.

### File based exports

Out of the box, imofix.io supports these formats to import data based on your file exports:

- [JSON](import-formats/json)
- [CSV](import-formats/csv)

If your files are formatted differently, imofix.io can probably support it as well by customizing the import for you.

Most means of transferring files are supported (your publicly accessible FTP server, a Google Cloud Storage bucket provided by imofix.io, etc.).

### Self managed data sheet

The most basic variant is to maintain an Excel file or Google Sheet in the structure defined in [CSV](import-formats/csv).
In this variant, updating the data is a manual process. Please get in touch to discuss the details.
