# Timpos Architecture

## Keeper

```text
Registry gives meaning to locator grammar.
Timpo records when + where.
Moment records what changed.
Replay reconstructs state.
Diff compares state over time.
```

## Core objects

```text
locator_registry -> timpos -> moments -> replay/diff
```

## Locator registry

The locator registry defines the grammar for source locators.

It answers:

```text
What source domains exist?
What scope segments are valid?
What resource types are valid?
What selector types are valid?
```

## Timpo

A Timpo records when and where an observation occurred.

```yaml
timpo:
  id: timpo.001
  t: 2026-06-24T15:42:00-04:00
  p: acme.monday://locate?scope=board:123456&resource=item:7891011&selector=column:status
```

## Moment

A Moment records what changed at a workstream path.

```yaml
moment:
  id: moment.001
  workstream: workstream.client_homepage_update
  path: tasks/update-hero-layout/status
  value: ready_for_client_review
  timpo: timpo.001
  previous: null
```

## Boundary

Timpos does not interpret meaning, assign owners, coordinate teams, or render surfaces.

Timpos only records source-located state changes so they can be replayed and diffed.
