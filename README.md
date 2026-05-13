# NWO Text-to-CAD

**AI-Powered CAD Generation for NWO Robotics**

## Overview

NWO Text-to-CAD integrates with the NWO Robotics API to enable autonomous robot design, manufacturing, and self-production. Transform natural language descriptions into production-ready mechanical designs.

## Features

- **Text-to-CAD**: Generate parametric models from descriptions
- **Motor/Gear Design**: Specialized tools for drivetrains
- **Electronics Integration**: PCB enclosures, cable management
- **Robot Assembly**: URDF/SDF generation
- **Self-Production**: Manufacturing outputs (STEP, STL, BOM)
- **NWO API Integration**: Direct connection to robotics commands

## Quick Start

```bash
pip install nwo-text-cad
```

```python
from nwo_text_cad import CADGenerator
from nwo_robotics import RobotAPI

api = RobotAPI(api_key="your_key")
cad = CADGenerator()

# Design from task
task = api.get_task("task_001")
gripper = cad.generate_from_task(task)
gripper.export_step("gripper.step")
```

## Skills

| Skill | Description |
|-------|-------------|
| `cad` | Core CAD generation |
| `urdf` | Robot descriptions |
| `assembly` | Assembly planning |
| `production` | Manufacturing outputs |

## Documentation

- [Integration Guide](INTEGRATION.md)
- [CAD Skill](skills/cad/SKILL.md)
- [URDF Skill](skills/urdf/SKILL.md)
- [Assembly Skill](skills/assembly/SKILL.md)
- [Production Skill](skills/production/SKILL.md)

## License

MIT - Part of NWO Robotics ecosystem
