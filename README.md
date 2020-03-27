r2pm-test
=========

Test package for new r2pm YAML format. Does nothing :)

To add to the database, copy this YAML into a file named
~/.local/share/RadareOrg/r2pm/r2pm-db/db/r2pm-test (or equivalent for your
environment):

```yaml
---
name: r2pm-test
version: 1.0.0  # {{ .R2Version }}
description: "Test package for new format."

install:

  linux:
    source:
      type: git
      repo: https://github.com/imyxh/r2pm-test.git
      ref: master  # {{ .R2Version }}
    commands:
        - make

  macos:
    source:
      type: git
      repo: https://github.com/imyxh/r2pm-test.git
      ref: 1.0.0  # {{ .R2Version }}
    commands:
        - make

  windows:
    source:
      type: zip
      url: https://github.com/radareorg/radare2/archive/1.0.0.zip
    out:
      - path: bin/test.exe
        type: exe

# TODO: uninstall
# vim: ft=yaml sw=2:
```

