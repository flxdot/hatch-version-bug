# Hatch version bug

This repository show cases a bug introduced with hatch version [1.16.0](https://github.com/pypa/hatch/releases/tag/hatch-v1.16.0).

With version 1.16.0 a new feature has been introduced: 

> The `version` and `project metadata` commands now support projects that do not use Hatchling as the build backend

But that seems to be false. It seems as if it dropped the support for non hatchling build backends.

## `v1.16.0` - `version` no longer works with non hatchling build system

```bash
uvx hatch@1.16.0 version patch
```

Result:
```
The version can only be set when Hatchling is the build backend
```

## `v1.15.1` - `version` works with non hatchling build system


```bash
uvx hatch@1.15.1 version patch
```

Result:
```
Old: 0.1.3
New: 0.1.4
```
