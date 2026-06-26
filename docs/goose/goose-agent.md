# Goose Agent

## Configuration

On ubuntu the config file is located at:

```bash
~/.config/goose/config.yaml
```

## Setting up provider

## DeepSeek

Currently the only supported model from deepseek on Goose is

```text
deepseek-v4-flash
```

The model **deepseek-v4-pro** presents reasoning errors on its API.

To set the flash model properly the configuration section for that model should look like this:

```yaml
providers:
  custom_deepseek:
    enabled: true
    model: deepseek-reasoner
    configured: true
active_provider: custom_deepseek
GOOSE_THINKING_EFFORT: high
```

