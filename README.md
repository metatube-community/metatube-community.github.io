![Plugin Banner](logos/banner.png)

English | [简体中文](README_ZH.md)

## How it works

- Utilize a backend API server called `metatube-server` to scrape content from [providers](#providers) and response with JSON.
- The pre-installed MetaTube plugin will request the server and download corresponding metadata, and then serve with Jellyfin/Emby.

## Providers

Full provider list can be found at [here](https://github.com/metatube-community/jellyfin-plugin-metatube/wiki/%E6%95%B0%E6%8D%AE%E6%9D%A5%E6%BA%90).

## How to use

Full documentation and examples can be found at [Wiki](https://github.com/metatube-community/jellyfin-plugin-metatube/wiki).

### Deploy server

- [jump to portal](https://github.com/metatube-community/jellyfin-plugin-metatube/wiki/%E5%90%8E%E7%AB%AF%E9%83%A8%E7%BD%B2)

### Install Plugin

- [jump to portal](https://github.com/metatube-community/jellyfin-plugin-metatube/wiki/%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85)

### Update plugin

- Jellyfin will automatically update plugin as long as you install it via repo url.
- Emby's MetaTube uses scheduled tasks to check for and download updates, if any available.

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

- Normal file names can improve search/identification accuracy, see [naming rules](https://github.com/metatube-community/jellyfin-plugin-metatube/wiki/%E5%91%BD%E5%90%8D%E8%A7%84%E8%8C%83) for more details.
- Select `MetaTube` as the only Metadata Provider can avoid certain conflict bugs.

## Feedback

- If you encounter bugs, please submit issues at [Issues](https://github.com/metatube-community/jellyfin-plugin-metatube/issues).
- If you have any questions, welcome and feel free to ask at [Discussions](https://github.com/metatube-community/jellyfin-plugin-metatube/discussions).

## Previews

<!-- [Screenshots are for preview only](./previews/). -->
[Screenshots are for preview only](/#).

## License

This plugin is released under the [MIT](https://github.com/metatube-community/jellyfin-plugin-metatube/blob/main/LICENSE) License.
