---
hide:
  - navigation
  # - toc
---

# Home

![Plugin Banner](images/banner.png)

English | [简体中文](README_ZH.md)

-----

**Documentation**: [https://metatube-community.github.io](https://metatube-community.github.io)

**Community Link**: [https://github.com/metatube-community](https://github.com/metatube-community)

-----

## How it works

- Powered by a backend API server called `metatube-server` to scrape content from internet and response with JSON.
- The pre-installed MetaTube plugin will request the server and download corresponding metadata, and then serve with Jellyfin/Emby.

## How to use

- [How to deploy server](./wiki/server-deployment.md)
- [How to install plugin](./wiki/plugin-installation.md)

Full documentation and examples can be found at [Wiki](./wiki/README.md).

### Update plugin

- Jellyfin will automatically update plugin as long as you install it via repo url.
- Emby's MetaTube uses scheduled tasks to check for and download updates, if any available.
- Plex plugin needs to be updated manually.

*A restart is required to apply plugin updates.*

### Configuration

- Locate MetaTube plugin configuration page.
- Input server url and server token (if any).
- Go to movie library:

    - Select the `Movie` type.
    - Check `MetaTube` as Metadata and Image provider.

## Usage

- Click `Scan Library` button after adding movies.
- Use `Refresh Metadata` to update metadata.
- Use `Identify` to search for specific movies.

### Actor Images

MetaTube integrates Actor Providers and is able to automatically search and identify actors by their names. You don't need to do any configuration to make it work, it already works like a charm!

For now, [`GFriends`](https://github.com/xinxin8816/gfriends) and [`XsList`](https://xslist.org/zh) are used as sources to provide actor information and images.

### Suggestions

- Normal file names can improve search/identification accuracy, see [naming rules](./wiki/naming-rules.md) for more details.
- Select `MetaTube` as the only Metadata Provider can avoid certain conflict bugs.

## Feedback

- If you encounter bugs, please submit issues at [Issues](https://github.com/metatube-community/jellyfin-plugin-metatube/issues).
- If you have any questions, welcome and feel free to ask at [Discussions](https://github.com/metatube-community/jellyfin-plugin-metatube/discussions).

<!-- ## Previews

[Screenshots are for preview only](./previews/README.md). -->

## License

This plugin is released under the [MIT](https://github.com/metatube-community/jellyfin-plugin-metatube/blob/main/LICENSE) License.
