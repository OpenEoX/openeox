# OpenEoX
This GitHub repository has been created to start the creation of a "standardized" End-of-Life (EOL) and End-of-Support (EOS) machine-readable JSON schema. This schema can serve as a proof-of-concept example to initiate conversations around standardizing the representation of EOL and EOS product information. This is designed to be flexible and can be extended or modified to accommodate the needs of different stakeholders, including software providers, vendors, suppliers, and open-source maintainers.

## Background Information
Read the following articles for more information about the overall initiative:
- [Establishing Standardized End-of-Life and End-of-Support Programs for Software and Hardware](https://becomingahacker.org/establishing-standardized-end-of-life-and-end-of-support-programs-for-software-and-hardware-e3e231898e02)
- [The Open Product Lifecycle Framework (OPLF)](https://becomingahacker.org/the-open-product-lifecycle-framework-oplf-5462eba91084)

## Example Usage
Below is an example JSON object conforming to the EOL and EOS Product JSON schema:
```
{
  "$schema": "https://openeox.org/schema-0.2.0.json",
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

## Benefits of OPLF
As stated [in this article](https://becomingahacker.org/establishing-standardized-end-of-life-and-end-of-support-programs-for-software-and-hardware-e3e231898e02), the following are a few benefits of a Standardized EOL and EOS programs in the Supply Chain:

- Improved Communication: Standardized EOL and EOS programs for open-source projects can facilitate clear and consistent communication among project maintainers, contributors, and users. This ensures that all parties are well-informed about the status of a project and can plan accordingly, reducing potential disruptions.
- Enhanced Trust and Reliability: By adopting standardized EOL and EOS programs, open-source maintainers can demonstrate their commitment to transparency, stability, and responsible project management. This can foster trust and confidence in the open-source ecosystem, which is vital for encouraging broader adoption and investment in open-source solutions.
- Increased Stability for Businesses, Governments, and Critical Infrastructure: A wide range of stakeholders that rely on open-source software can benefit from a more predictable and transparent EOL and EOS process. This can help them plan their technology roadmaps more effectively, allocate resources appropriately, and mitigate potential risks associated with deprecated software.
- Support for Open-Source Sustainability: By implementing standardized EOL and EOS programs, open-source maintainers can help to ensure the long-term sustainability of their projects. This can encourage new contributors, attract funding, and ultimately contribute to the ongoing success and growth of the open-source community.

