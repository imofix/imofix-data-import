# JSON import format

The JSON import supports these files:

- [properties.json](examples/properties.json), required
- [service-partners.json](examples/service-partners.json), optional
- [janitors.json](examples/janitors.json), optional

Alternatively, It is possible to provide everything in a single file named `export.json`:

```json
{
   "properties":[],
   "service_partners":[],
   "janitors":[]
}
```
