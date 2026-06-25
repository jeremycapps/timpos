# Timpos Protocol

Timpos v1 is YAML-first.

Core files:

```text
locator_registry.schema.yaml
timpos.schema.yaml
moments.schema.yaml
```

Core model:

```text
locator_registry -> timpos -> moments -> replay/diff
```

Canonical locator:

```text
{client}.{domain}://locate?scope={scope}&resource={resource}&selector={selector}
```

Keeper:

```text
Registry gives meaning to locator grammar.
Timpo records when + where.
Moment records what changed.
```
