# Paper

A Redmine theme that feels written on paper: cream sheets with a fine grain
and soft creases, serif type, and pen, pencil and highlighter colors, with a
newspaper-style masthead and double rules.

## Installation

1. Clone this theme ([https://github.com/zaburt/redmine_paper](https://github.com/zaburt/redmine_paper)) into the Redmine `themes/`
   directory at the application root (Redmine 7+) as `paper`:

   ```
   git clone https://github.com/zaburt/redmine_paper.git themes/paper
   ```

   The result should contain:

   ```
   themes/paper/stylesheets/application.css
   ```

   > Note: Redmine 6 and earlier used `public/themes/` instead of `themes/`.

2. Restart Redmine. In production, precompile assets:

   ```
   RAILS_ENV=production bin/rails assets:precompile
   ```

3. Go to `Administration -> Settings -> Display` and select "Paper"
   in the "Theme" drop-down list.

## Customize

1. Change `images/logo.svg` for the header logo, `images/logo-login.svg` for
   the login page and `favicon/favicon.svg` for the browser tab icon.
2. The palette is defined inline as hex values in
   `stylesheets/application.css`:

   | Role                       | Color     |
   |----------------------------|-----------|
   | Blue-black ink (text)      | `#1D2233` / `#262B3D` |
   | Blue ink (links, buttons)  | `#25449A` / `#1F3A7A` |
   | Red pen (underlines, hover)| `#A3262A` |
   | Green ink                  | `#2F6B3A` |
   | Highlighter (hover)        | `#FFE98A` |
   | Paper sheet / desk         | `#FFFCF2` / `#FBF6E8` / `#E6DCC4` |

   The paper grain and creases are inline SVG/gradients in the "Paper layer"
   section at the end of `stylesheets/application.css`; remove the
   `background-image` lines there for perfectly flat paper.
3. In production, re-run `assets:precompile` after editing any theme file.

## License

Licensed under [GNU GPLv2](LICENSE).

Copyright (c) 2026 Onur Küçük (onur [at] delipenguen.net)
