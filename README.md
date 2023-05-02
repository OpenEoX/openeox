# Open Product Lifecycle Framework (OPLF)
This GitHub repository has been created to start the creation of a potential "standardized" [End-of-Life (EOL) and End-of-Support (EOS) JSON schema](poc-schema.json). This schema can serve as a proof-of-concept example to initiate conversations around standardizing the representation of EOL and EOS product information. The schema is designed to be flexible and can be extended or modified to accommodate the needs of different stakeholders, including software providers, vendors, suppliers, and open-source maintainers.

NOTE: Read the [initial article](https://becomingahacker.org/establishing-standardized-end-of-life-and-end-of-support-programs-for-software-and-hardware-e3e231898e02) for more background.

## Example Usage
Below is an example JSON object conforming to the EOL and EOS Product JSON schema:
```
{
  "$schema": "https://openplf.org/schema-0.2.0.json",
  "creationTimestamp": "2023-05-02T01:27:00Z"
  "EOLDate": "2023-06-01T23:59:59Z",
  "supplierId": "123456",
  "supplierName": "ExampleSupplier",
  "productId": "PID12345",
  "productName": "ExampleProduct",
  "productVersion": "1.0",
  "replacementProduct": {
    "productId": "P67890",
    "productName": "ExampleReplacementProduct",
    "productVersion": "2.0"
  }
}

```
This is a very rough draft of a potential schema to start the discussion in the industry.
