# DesignsLabz Theme

A lightweight, developer-friendly WordPress theme built for the block editor (Gutenberg). The header, footer and other site-wide sections are managed as reusable blocks, so editors can change them without touching code, while developers get a clean SCSS and Webpack setup.

![DesignsLabz Theme screenshot](screenshot.png)

![WordPress 6.7+](https://img.shields.io/badge/WordPress-6.7%2B-21759B?style=flat-square&logo=wordpress&logoColor=white)
![PHP 8.0+](https://img.shields.io/badge/PHP-8.0%2B-777BB4?style=flat-square&logo=php&logoColor=white)
![License GPL-3.0-or-later](https://img.shields.io/badge/license-GPL--3.0--or--later-blue?style=flat-square)

## Features

- **Built for the block editor:** wide and full alignment, block styles, responsive embeds, and editor styles that match the front end
- **Design tokens in `theme.json`:** colour palette, typography, spacing, borders and shadows in one place
- **Theme Options page:** pick reusable blocks for the header message bar, social menu, main menu and footer; set the 404 page message; store a Google Tag Manager ID
- **Blog templates:** post cards with a fallback thumbnail when a post has no featured image, and a styled single post page
- **Latest Posts card style** for the core Latest Posts block
- **Branded login screen** using the theme logo, linking back to your site
- **Modern build setup:** SCSS, Babel, PostCSS with Autoprefixer, cssnano and Stylelint, bundled by Webpack
- **Clean, object-oriented PHP** with each concern in its own class

## Requirements

| Requirement | Version |
| --- | --- |
| WordPress | 6.7 or newer (tested up to 6.8) |
| PHP | 8.0 or newer |
| Node.js | 18 or newer (only to rebuild the CSS and JavaScript) |

## Installation

1. Download the theme: click **Code → Download ZIP** on this page, or clone it into your themes folder:

   ```bash
   cd wp-content/themes
   git clone https://github.com/designs-labz/designslabz-theme.git
   ```

2. In WordPress, go to **Appearance → Themes** and activate **DesignsLabz Theme**.

The compiled assets are included, so the theme works straight away. You only need Node.js if you want to change the SCSS or JavaScript.

## Setting it up

After activating the theme, open **Theme Options** in the admin menu.

| Setting | What it does |
| --- | --- |
| Header Message Bar | A reusable block shown in a bar at the top of every page, e.g. an announcement |
| Header Social Menu | A reusable block with your social links |
| Header Menu | A reusable block holding the main navigation |
| Footer Reusable Block | The reusable block used as the site footer |
| 404 Message | The content shown on the "page not found" page |
| Google Tag Manager ID | Saves your GTM container ID, e.g. `GTM-XXXXXXX` (the snippet output is not added to the page yet) |

Create the reusable blocks first (in the block editor, select blocks, then **⋮ → Create pattern** and make it synced), then choose them here.

## Development

Install the build tools once:

```bash
npm install
```

| Command | What it does |
| --- | --- |
| `npm start` | Watches the SCSS and JavaScript and rebuilds on every change |
| `npm run build` | Creates minified production files in `assets/build/` |

### Where things are

| Path | Contents |
| --- | --- |
| `includes/theme-setup.php` | Theme supports and meta tags |
| `includes/theme-options.php` | The Theme Options admin page |
| `includes/enqueuer.php` | Loads CSS and JavaScript for the front end, editor and admin |
| `includes/admin.php` | Login screen branding |
| `parts/` | Header, footer, message bar and social menu template parts |
| `assets/scss/` | Styles: `base/` (variables, mixins, reset), `partials/`, `blocks/`, `templates/` |
| `assets/js/` | Front-end, editor and admin scripts |
| `theme.json` | Global styles and block editor settings |

To change the brand colours, edit the palette in `theme.json` and the variables in `assets/scss/base/`, then run `npm run build`.

## License

Released under the [GNU General Public License v3.0 or later](LICENSE).

## Author

Built by [Bhavanaditya D R](https://www.bhavanaditya.com/) for [DesignsLabz](https://designslabz.com/).
