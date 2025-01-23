<p align="center">
 <img width="100px" src="https://res.cloudinary.com/anuraghazra/image/upload/v1594908242/logo_ccswme.svg" align="center" alt="GitHub Readme Stats" />
 <h2 align="center">GitHub Readme Stats</h2>
 <p align="center">Dynamically generated GitHub stats for READMEs!</p>
 <p align="center">The original project was made by Anurag Hazra. This fork only exists so I can host my own on Vercel.</p>
</p>
 
# GitHub Stats Card

Copy and paste this into your markdown, and that's it. Simple!

Change the `?username=` value to your GitHub username.

```md
[![Inês' GitHub stats](https://github-readme-stats.vercel.app/api?username=inesiscosta)](https://github.com/inesiscosta/github-readme-stats)
```

### Hiding individual stats

You can pass a query parameter `&hide=` to hide any specific stats with comma-separated values.

> Options: `&hide=stars,commits,prs,issues,contribs`

```md
![Inês' GitHub stats](https://github-readme-stats.vercel.app/api?username=inesiscosta&hide=contribs,prs)
```

### Showing icons

To enable icons, you can pass `&show_icons=true` in the query param, like so:

```md
![Inês' GitHub stats](https://github-readme-stats.vercel.app/api?username=inesiscosta&show_icons=true)
```

### Themes

With inbuilt themes, you can customize the look of the card without doing any [manual customization](#customization).

Use `&theme=THEME_NAME` parameter like so :

```md
![Inês' GitHub stats](https://github-readme-stats.vercel.app/api?username=inesiscosta&show_icons=true&theme=radical)
```

#### All inbuilt themes

GitHub Readme Stats comes with several built-in themes (e.g. `dark`, `radical`, `merko`, `gruvbox`, `tokyonight`, `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dracula`).

#### Responsive Card Theme
##### Use GitHub's theme context tag

You can use [GitHub's theme context](https://github.blog/changelog/2021-11-24-specify-theme-context-for-images-in-markdown/) tags to switch the theme based on the user GitHub theme automatically. This is done by appending `#gh-dark-mode-only` or `#gh-light-mode-only` to the end of an image URL. This tag will define whether the image specified in the markdown is only shown to viewers using a light or a dark GitHub theme:

```md
[![Anurag's GitHub stats-Dark](https://github-readme-stats.vercel.app/api?username=inesiscosta&show_icons=true&theme=dark#gh-dark-mode-only)](https://github.com/inesiscosta/github-readme-stats#gh-dark-mode-only)
[![Anurag's GitHub stats-Light](https://github-readme-stats.vercel.app/api?username=inesiscosta&show_icons=true&theme=default#gh-light-mode-only)](https://github.com/inesiscosta/github-readme-stats#gh-light-mode-only)
```

<details>
<summary>:eyes: Show example</summary>

[![Inês' GitHub stats-Dark](https://github-readme-stats.vercel.app/api?username=inesiscosta\&show_icons=true\&theme=dark#gh-dark-mode-only)](https://github.com/inesiscosta/github-readme-stats#gh-dark-mode-only)
[![Inês' GitHub stats-Light](https://github-readme-stats.vercel.app/api?username=inesiscosta\&show_icons=true\&theme=default#gh-light-mode-only)](https://github.com/inesiscosta/github-readme-stats#gh-light-mode-only)

</details>

### Customization

You can customize the appearance of all your cards however you wish with URL parameters.

#### Common Options

| Name | Description | Type | Default value |
| --- | --- | --- | --- |
| `title_color` | Card's title color. | string (hex color) | `2f80ed` |
| `text_color` | Body text color. | string (hex color) | `434d58` |
| `icon_color` | Icons color if available. | string (hex color) | `4c71f2` |
| `border_color` | Card's border color. Does not apply when `hide_border` is enabled. | string (hex color) | `e4e2e2` |
| `bg_color` | Card's background color. | string (hex color or a gradient in the form of *angle,start,end*) | `fffefe` |
| `hide_border` | Hides the card's border. | boolean | `false` |
| `theme` | Name of the theme, choose from [all available themes](themes/README.md). | enum | `default` |
| `cache_seconds` | Sets the cache header manually (min: 21600, max: 86400). | integer | `21600` |
| `locale` | Sets the language in the card, you can check full list of available locales [here](#available-locales). | enum | `en` |
| `border_radius` | Corner rounding on the card. | number | `4.5` |

##### Gradient in bg\_color

You can provide multiple comma-separated values in the bg\_color option to render a gradient with the following format:

    &bg_color=DEG,COLOR1,COLOR2,COLOR3...COLOR10

##### Available locales

Here is a list of all available locales:

<table>
<tr><td>

| Code | Locale |
| --- | --- |
| `cn` | Chinese |
| `zh-tw` | Chinese (Taiwan) |
| `ar` | Arabic |
| `cs` | Czech |
| `de` | German |
| `en` | English |
| `bn` | Bengali |
| `es` | Spanish |
| `fr` | French |
| `hu` | Hungarian |

</td><td>

| Code | Locale |
| --- | --- |
| `it` | Italian |
| `ja` | Japanese |
| `kr` | Korean |
| `nl` | Dutch |
| `pt-pt` | Portuguese (Portugal) |
| `pt-br` | Portuguese (Brazil) |
| `np` | Nepali |
| `el` | Greek |
| `ru` | Russian |
| `uk-ua` | Ukrainian |

</td><td>

| Code | Locale |
| --- | --- |
| `id` | Indonesian |
| `ml` | Malayalam |
| `my` | Burmese |
| `sk` | Slovak |
| `tr` | Turkish |
| `pl` | Polish |
| `uz` | Uzbek |
| `vi` | Vietnamese |
| `se` | Swedish |

</td></tr>
</table>

#### Stats Card Exclusive Options

| Name | Description | Type | Default value |
| --- | --- | --- | --- |
| `hide` | Hides the [specified items](#hiding-individual-stats) from stats. | string (comma-separated values) | `null` |
| `hide_title` | Hides the title of your stats card. | boolean | `false` |
| `card_width` | Sets the card's width manually. | number | `500px  (approx.)` |
| `hide_rank` | Hides the rank and automatically resizes the card width. | boolean | `false` |
| `rank_icon` | Shows alternative rank icon (i.e. `github`, `percentile` or `default`). | enum | `default` |
| `show_icons` | Shows icons near all stats. | boolean | `false` |
| `include_all_commits` | Count total commits instead of just the current year commits. | boolean | `false` |
| `line_height` | Sets the line height between text. | integer | `25` |
| `exclude_repo` | Excludes specified repositories. | string (comma-separated values) | `null` |
| `custom_title` | Sets a custom title for the card. | string | `<username> GitHub Stats` |
| `text_bold` | Uses bold text. | boolean | `true` |
| `disable_animations` | Disables all animations in the card. | boolean | `false` |
| `ring_color` | Color of the rank circle. | string (hex color) | `2f80ed` |
| `number_format` | Switches between two available formats for displaying the card values `short` (i.e. `6.6k`) and `long` (i.e. `6626`). | enum | `short` |
| `show` | Shows [additional items](#showing-additional-individual-stats) on stats card (i.e. `reviews`, `discussions_started`, `discussions_answered`, `prs_merged` or `prs_merged_percentage`). | string (comma-separated values) | `null` |

> [!NOTE]\
> When hide\_rank=`true`, the minimum card width is 270 px + the title length and padding.

#### Repo Card Exclusive Options

| Name | Description | Type | Default value |
| --- | --- | --- | --- |
| `show_owner` | Shows the repo's owner name. | boolean | `false` |
| `description_lines_count` | Manually set the number of lines for the description. Specified value will be clamped between 1 and 3. If this parameter is not specified, the number of lines will be automatically adjusted according to the actual length of the description. | number | `null` |
