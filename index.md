<h1 align="center">Jellyfin Plugin JavTube</h1>
<h5 align="center">English | <a href="https://github.com/javtube/jellyfin-plugin-javtube/wiki">简体中文</a></h5>

<p align="center">
<img alt="Plugin Banner" src="https://github.com/javtube/jellyfin-plugin-javtube/raw/main/docs/banner.png"/>
<br/>
<br/>

# How it works

- Utilize a backend API server called `javtube-server` to scrape content from [providers](#providers) and response with JSON.
- The pre-installed JavTube plugin will request the server and download corresponding metadata, and then serve with Jellyfin/Emby.

# Providers

[Here are supported providers.](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%95%B0%E6%8D%AE%E6%9D%A5%E6%BA%90)

# How to use

## Deploy `javtube-server`

➤ [portal](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E5%90%8E%E7%AB%AF%E9%83%A8%E7%BD%B2)

## Install Plugin

➤ [portal](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85)

## Update plugin

### Jellyfin

Jellyfin will automatically update plugin as long as you install it via repo url.

### Emby

Emby's JavTube uses scheduled tasks to check for and download updates, if any available.

*A restart is required to apply plugin updates.*

## Configuration

- Locate JavTube plugin configuration page.
- Input server url and server token (if any).
- Go to movie library:

  - Select the `Movie` type.
  - Check `JavTube` as Metadata and Image provider.

## Usage

- After adding movies, click `scan library` button.
- Use `Refresh Metadata` to update metadata.
- Use `Identify` to search for specific movies.

## Actor Images

JavTube integrates Actor Providers and is able to automatically search and identify actors by their names. You don't need to do any configuration to make it work, it already works like a charm!

For now, we use [`GFriends`](https://github.com/xinxin8816/gfriends) ans [`XsList`](https://xslist.org/zh) as sources to provider actor information and images.

## Suggestions

- Better file naming can improve search/identification accuracy, see [naming rules](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E5%91%BD%E5%90%8D%E8%A7%84%E8%8C%83) for more details.
- Select `JavTube` as the only Metadata Provider can avoid certain conflict bugs.

# Feedback

- If you encounter bugs, please submit issues at [issues](https://github.com/javtube/jellyfin-plugin-javtube/issues).
- If you have any questions, welcome and feel free to ask at [Discussions](https://github.com/javtube/jellyfin-plugin-javtube/discussions).

# Screenshots

[Here are screenshots for preview purpose.](https://github.com/javtube/jellyfin-plugin-javtube/wiki/%E6%95%88%E6%9E%9C%E9%A2%84%E8%A7%88)

# License

This plugin is released under the [MIT](https://github.com/javtube/jellyfin-plugin-javtube/blob/main/LICENSE) License.
