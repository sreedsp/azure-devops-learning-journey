
| Concept            | Summary                                                                 |
| ------------------ | ----------------------------------------------------------------------- |
| Regions            | A geographical area with multiple datacenters connected via low latency |
| Availability Zones | Physically separate datacenters within one region for HA                |
| Availability Sets  | Logical grouping inside a datacenter for redundancy                     |
| Management Group   | Top-level governance container                                          |
| Subscription       | Billing + resource boundary                                             |
| Resource Group     | Logical resource container for lifecycle management                     |
| Resource           | Actual deployable item (VM, Storage, etc.)                              |



 Availability Set (within a single AZ)
 ├── Fault Domain 1
 │   ├── VM1 (Update Domain 1)
 │   └── VM2 (Update Domain 2)
 ├── Fault Domain 2
 │   ├── VM3 (Update Domain 1)
 │   └── VM4 (Update Domain 2)

 🌍 East US Region
 ├── Zone 1 [Datacenter A]
 ├── Zone 2 [Datacenter B]
 └── Zone 3 [Datacenter C]


 🌍 Azure Geography (e.g., North America)
   └── Region: East US
       ├── Availability Zone 1 (Data Center A)
       │     └── Availability Sets (logical groups inside)
       ├── Availability Zone 2 (Data Center B)
       │     └── Availability Sets
       └── Availability Zone 3 (Data Center C)
             └── Availability Sets
