# folder-sync

One-way folder synchronization from tree-view. Copies new/changed files to target and removes files that no longer exist in source.

## Features

- **One-way sync**: Copies only new or changed files to target.
- **Auto cleanup**: Removes files from target that no longer exist in source.
- **Ignore extensions**: Skip specific file types during sync.
- **Open target**: Uses `open-external` service to open target folder.

## Installation

To install `folder-sync` run `ppm install asiloisad/pulsar-folder-sync` to install a package directly from the GitHub repository.

## Usage

1. Right-click a folder in tree-view and run `folder-sync:create`
2. Edit the `.sync` config file with your target path
3. Right-click the `.sync` file and run `folder-sync:run`

## Config file

Use `target` for absolute path:

```json
{
  "target": "C:/Backup/MyFolder",
  "ignoreExts": ["log", "tmp"]
}
```

Or use `name` with package setting `storagePath`:

```json
{
  "name": "MyFolder",
  "ignoreExts": ["log", "tmp"]
}
```

Target is built as `storagePath/name`.

### Options

- `target` - absolute destination path
- `name` - folder name inside storagePath
- `ignoreExts` - file extensions to ignore (optional)

## Commands

Commands available in `.tree-view`:

- `folder-sync:create` - create `.sync` config in selected folder
- `folder-sync:run` - run sync using selected `.sync` file
- `folder-sync:open` - open target folder in file manager

## Contributing

Got ideas to make this package better, found a bug, or want to help add new features? Just drop your thoughts on GitHub — any feedback's welcome!
