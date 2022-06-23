![Plugin Banner](logos/banner.png)

English | [简体中文](README_ZH.md)

## How it works

- Utilize a backend API server called `javtube-server` to scrape content from [providers](#providers) and response with JSON.
- The pre-installed JavTube plugin will request the server and download corresponding metadata, and then serve with Jellyfin/Emby.

## Providers

Full provider list can be found at [here](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%95%B0%E6%8D%AE%E6%9D%A5%E6%BA%90).

## How to use

Full documentation and examples can be found at [Wiki](https://github.com/javtube/jellyfin-plugin-javtube/wiki).

### Deploy server

- [jump to portal](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E5%90%8E%E7%AB%AF%E9%83%A8%E7%BD%B2)

### Install Plugin

- [jump to portal](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85)

### Update plugin

- Jellyfin will automatically update plugin as long as you install it via repo url.
- Emby's JavTube uses scheduled tasks to check for and download updates, if any available.

*A restart is required to apply plugin updates.*

### Configuration

- Locate JavTube plugin configuration page.
- Input server url and server token (if any).
- Go to movie library:

  - Select the `Movie` type.
  - Check `JavTube` as Metadata and Image provider.

## Usage

- Click `Scan Library` button after adding movies.
- Use `Refresh Metadata` to update metadata.
- Use `Identify` to search for specific movies.

### Actor Images

JavTube integrates Actor Providers and is able to automatically search and identify actors by their names. You don't need to do any configuration to make it work, it already works like a charm!

For now, [`GFriends`](https://github.com/xinxin8816/gfriends) and [`XsList`](https://xslist.org/zh) are used as sources to provider actor information and images.

### Suggestions

- Normal file names can improve search/identification accuracy, see [naming rules](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E5%91%BD%E5%90%8D%E8%A7%84%E8%8C%83) for more details.
- Select `JavTube` as the only Metadata Provider can avoid certain conflict bugs.

## Feedback

- If you encounter bugs, please submit issues at [Issues](https://github.com/javtube/jellyfin-plugin-javtube/issues).
- If you have any questions, welcome and feel free to ask at [Discussions](https://github.com/javtube/jellyfin-plugin-javtube/discussions).

## Previews

[Screenshots are for preview only](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%95%88%E6%9E%9C%E9%A2%84%E8%A7%88).

## License

This plugin is released under the [MIT](https://github.com/javtube/jellyfin-plugin-javtube/blob/main/LICENSE) License.
