# Conventional Changelog plugin for release-it

This plugin will provide the recommended bump to release-it, and update the changelog file (e.g. `CHANGELOG.md`).

```
npm install --save-dev @release-it/conventional-changelog
```

In [release-it](https://github.com/release-it/release-it) config:

```
"plugins": {
  "@release-it/conventional-changelog": {
    "preset": "angular",
    "infile": "CHANGELOG.md"
  }
}
```

You can also choose a preferred scheme for versioning:

```
// semver.org scheme
"plugins": {
  "@release-it/conventional-changelog": {
    "preset": "angular",
    "scheme": "semver"
  }
}

// calver.org scheme
"plugins": {
  "@release-it/conventional-changelog": {
    "preset": "angular",
    "scheme": "calver",
    "versionFormat": "YY.MM.MICRO"
  }
}
```

- Omit the `infile` at will. If set, but the file does not exist yet, it's created with the full history.
- Please find the
  [list of available presets](https://github.com/conventional-changelog/conventional-changelog/tree/master/packages)
  (`angular`, `ember`, etc).
- Options are passed verbatim to
  [conventional-recommended-bump](https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-recommended-bump#readme)
  and
  [conventional-changelog](https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-changelog#readme).
- Available version schemes: [semver.org](https://semver.org) and [calver.org](https://calver.org).
