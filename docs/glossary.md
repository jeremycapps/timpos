# Timpos Glossary

## Client

The enterprise, customer, workspace, or user namespace in a Timpos locator.

## Domain

The source system in a Timpos locator. Examples: monday, jira, notion, s3, github, local_file.

## Locator

The source address stored in `timpo.p`.

Template:

```text
{client}.{domain}://locate?scope={scope}&resource={resource}&selector={selector}
```

## Locator registry

The YAML file that defines valid systems, scope patterns, resource types, and selector types.

## Scope

A typed namespace path inside the client/domain.

## Resource

The typed primary object being located.

## Selector

The typed part of the resource being observed.

## Timpo

A time-position observation. It records when and where an observation occurred.

## Moment

A path-value observation. It records what changed at a workstream path.

## Workstream

A bounded context being versioned.

## Path

A state address inside a workstream.

## Replay

Reconstructing state from Moments.

## Diff

Comparing replayed state across Moments or time.
