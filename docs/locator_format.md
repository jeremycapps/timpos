# Timpos Locator Format

## Canonical template

```text
{client}.{domain}://locate?scope={scope}&resource={resource}&selector={selector}
```

## Parts

```text
client   = enterprise, customer, workspace, or user namespace
domain   = source system
locate   = fixed verb meaning this URI locates a source
scope    = typed namespace path inside the client/domain
resource = typed primary object
selector = typed fragment, field, version, range, or subpart
```

## Typed segments

Scope is a typed path:

```text
{type}:{id}/{type}:{id}
```

Resource and selector are typed segments:

```text
{type}:{id}
```

## Example

```text
acme.monday://locate?scope=board:123456&resource=item:7891011&selector=column:status
```

Decomposes as:

```yaml
client: acme
domain: monday
scope: board:123456
resource: item:7891011
selector: column:status
```

## Reserved characters

IDs containing reserved URI characters must be percent-encoded.

Common reserved characters:

```text
: / ? # & %
```

Example file path:

```text
file:examples%2Fclient_homepage_update%2Fsources%2Fclient-review.md
```

## Keeper

```text
Client names the world.
Domain names the system.
Scope names the namespace inside it.
Resource names the object.
Selector names the part.
```
