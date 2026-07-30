# Hardware source status

The native PCB and mechanical CAD archives are not currently available in this checkout. Recovery from old university accounts and personal storage is ongoing.

The images and preliminary datasheet in this repository are useful design evidence, but they are not substitutes for:

- editable schematics;
- PCB layout source;
- verified fabrication outputs;
- bill of materials and approved substitutions;
- centroid/pick-and-place data;
- mechanical assemblies; or
- firmware and FPGA source.

No reconstructed source has been presented as an original recovered file.

## Revision map

| Revision group | Status | Identifying material |
| --- | --- | --- |
| Later cost-reduced revision | Renders recovered; native source unavailable | QFP Spartan-6, revised placement, incomplete assembly concept |
| Earlier revision | Renders and preliminary documentation recovered; native source unavailable | BGA Spartan-6 and external application RAM |

## Planned source layout

If the original archives are recovered, they will be added without rewriting their history:

```text
hardware/
├── pcb/
│   ├── source/
│   └── fabrication/
├── mechanical/
│   ├── source/
│   └── exports/
└── README.md
```

Each recovered package should include its original revision/date and a short note identifying which images and datasheet sections correspond to it.
