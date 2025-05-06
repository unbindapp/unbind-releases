# unbind-releases

Meta release repository for Unbind components

## metadata.json

Supports simple rules for specify dependencies of an upgrade. For example, if we are on `v0.0.1`, to get to `v0.0.4` we need to upgrade to `v0.0.3` first if this metadata is defined:

```json
{
  "v0.0.1": {
    "version": "v0.0.2",
    "description": "Initial release",
    "breaking": false
  },
  "v0.0.2": {
    "version": "v0.0.2",
    "description": "Feature update",
    "breaking": false
  },
  "v0.0.3": {
    "version": "v0.0.3",
    "description": "Feature update",
    "breaking": false
  },
  "v0.0.4": {
    "version": "v0.4.0",
    "description": "Major feature update",
    "breaking": true,
    "depends_on": ["v0.3.0"]
  }
}
```
