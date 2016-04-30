# Suggestions:
- [SublimeLinter Package](http://www.sublimelinter.com/en/latest/)
 - [JSON Linter](https://github.com/SublimeLinter/SublimeLinter-json)
 - [Annotations Linter](https://github.com/SublimeLinter/SublimeLinter-annotations)
- [Alignment Plugin](https://github.com/randy3k/AlignTab)
- [Highlight non-ascii chars](https://github.com/TuureKaunisto/highlight-dodgy-chars)
- [Markdown preview](https://github.com/revolunet/sublimetext-markdown-preview)
- [JSON Pretty Print](https://github.com/dzhibas/SublimePrettyJson)
- [SFTP Plugin](https://wbond.net/sublime_packages/sftp)

## JSON Linter Configuration
```json
"json": {
    "@disable": false,
    "args": [],
    "excludes": [],
    "strict": true
}
```

## Annotations Linter Configuration
```json
"annotations": {
    "@disable": false,
    "args": [],
    "errors": [
        "FIXME"
    ],
    "excludes": [],
    "warnings": [
        "NOTE",
        "README",
        "TODO",
        "XXX",
        "@todo"
    ]
}
```

## SFTP Configuration
```json
{
    "type": "sftp",
    "save_before_upload": true,
    "upload_on_save": true,
    "sync_down_on_open": false,
    "sync_skip_deletes": false,
    "sync_same_age": true,
    "confirm_downloads": false,
    "confirm_sync": true,
    "confirm_overwrite_newer": false,
    "host": "server.example.com",
    "user": "username",
    "remote_path": "/path/to/project/",
    "ignore_regexes": [
        "\\.sublime-(project|workspace)", "sftp-config(-alt\\d?)?\\.json",
        "sftp-settings\\.json", "/venv/", "\\.svn/", "\\.hg/", "\\.git/",
        "\\.bzr", "_darcs", "CVS", "\\.DS_Store", "Thumbs\\.db", "desktop\\.ini",
        "\\.log","/vendor/","\\.lock"
    ],
    "extra_list_connections": 25,
    "connect_timeout": 5,
    "keepalive": 120,
    "ssh_key_file": "~/.ssh/id_rsa",
}
```
