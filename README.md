# Timpos

Timpos is a YAML-first protocol for recording source-located state changes inside workstreams.

## Keeper

```text
Registry gives meaning to locator grammar.
Timpo records when + where.
Moment records what changed.
Replay reconstructs state.
Diff compares state over time.
```

## Canonical locator

```text
{client}.{domain}://locate?scope={scope}&resource={resource}&selector={selector}
```

Example:

```text
acme.monday://locate?scope=board:123456&resource=item:7891011&selector=column:status
```

## Core model

```text
locator_registry -> timpos -> moments -> replay/diff
```

A workstream is a bounded context.
A path is a state address inside that workstream.
A locator points to the source location.
A Timpo binds that locator to time.
A Moment records a value at a workstream path.

## What Timpos is not

Timpos does not interpret meaning.
Timpos does not assign owners.
Timpos does not coordinate teams.
Timpos does not render dashboards.
Timpos does not run agents.

It only records state changes so they can be replayed and diffed.

## Status

Timpos v1 is YAML-first. Reference implementations may be added later.
