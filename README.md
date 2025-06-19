# 🧩 Poros Core

Reusable core utilities for LLM agent frameworks. Includes:

- Pydantic-to-OpenAI schema generation
- JSON output extraction and parsing
- Tool execution wrappers
- Core model-independent components

Built to power `poros-agent`, but usable in any LLM-based system.

## 📦 Installation

```bash
pip install poros-core
```

## 🔧 Example

```python
from poros_core.schema import generate_tool_schema
from pydantic import BaseModel

class WeatherInput(BaseModel):
    city: str

schema = generate_tool_schema(WeatherInput)
```

## 🛠 Components

- `schema.py`: Convert Pydantic models to OpenAI-compatible tool schemas
- `parsing.py`: Robust JSON fenced block extraction from model outputs
- `tool_runtime.py`: Input validation and tool function wrapping
