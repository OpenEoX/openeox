# OpenEoX JSON Schema

This JSON schema provides a standard format for representing product lifecycle milestones including End-of-Life (EOL) and End-of-Support (EOS) information for products.

## Schema Required Properties

The following properties are required:

- `$schema`
- `supplierId`
- `supplierName`
- `productId`
- `productName`
- `productVersion`
- `EOLDate`

## Explanation of Schema Properties

1. **$schema**: This property references the schema definition (`schema_t`) and specifies the schema against which the JSON object must be validated. The valid value for this property is `"https://openeox.org/schema-0.2.0.json"`.

2. **creationTimestamp**: This property represents the timestamp when the record was created. The timestamp must follow the RFC 3339 standard for date-time formatting. For example: `"2023-05-01T12:00:00Z"`. The usage of the separator `T` and the timezone identifier is mandatory.

3. **EOLDate**: This property contains the End of Life (EOL) date of the product, indicating the date after which the product is no longer produced or maintained. The value can either be a date-time format following the RFC 3339 standard or the string "tba" (To Be Announced) if the EOL date is not yet determined or announced.

4. **supplierId**: This property contains a unique identifier for the supplier or service provider. It is a string with a minimum length of 1 character.
*Note: The exact usage and proper identifying method of this field is currently under discussion in the community (see #6). As a [CSAF](https://docs.oasis-open.org/csaf/csaf/v2.0/csaf-v2.0.html) issuing party, you could use the value `/document/publisher/namespace`.*

5. **supplierName**: This property contains the name of the supplier or service provider. It is a string with a minimum length of 1 character.

6. **productId**: This property contains the unique product identifier for the product. It is a string with a minimum length of 1 character and references the `productId_t` definition.
*Note: The exact usage and proper identifying method of this field is currently under discussion in the community (see #22). If you have an SBOM that you provide for download at a specific link and that one is stable, the download URL could be used as identifier.*

7. **productName**: This property contains the name of the product. It is a string with a minimum length of 1 character and references the `productName_t` definition.

8. **productVersion**: This property contains the version or release information of the product. It is a string with a minimum length of 1 character and references the `productVersion_t` definition. This SHALL not contain a version range.

9. **replacementProduct**: This property contains information about the recommended replacement product, if applicable. It is an object with the following required properties:

    - **productId**: Contains the unique product identifier for the replacement product. It is a string with a minimum length of 1 character and references the `productId_t` definition.
    *Note: The exact usage and proper identifying method of this field is currently under discussion in the community (see #22). If you have an SBOM that you provide for download at a specific link and that one is stable, the download URL could be used as identifier.*

    - **productName**: Contains the name of the replacement product. It is a string with a minimum length of 1 character and references the `productName_t` definition.
    
    - **productVersion**: Contains the version or release information of the product. It is a string with a minimum length of 1 character and references the `productVersion_t` definition. This SHALL not contain a version range.

These properties together allow for a complete and standardized representation of End-of-Life (EOL) and End-of-Support (EOS) information for products.
