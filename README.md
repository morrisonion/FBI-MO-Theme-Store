# FBI-MO-Theme-Store

Theme catalog for the **Theme Store** in [FBI-MO](https://github.com/morrisonion/FBI-MO).

thanks to [The0zymandias](https://github.com/The0zymandias) for the original FBI theme Unistore.

 All credit for the themes goes to the original authors. If you are an author and want your theme removed, contact me with proof it is yours.

## How it works

* `themestore.json` is the endpoint FBI-MO downloads into `sdmc:/fbi/themes/` on the 3DS.
* Every theme is a `.motheme` file (a ZIP renamed from `.zip`):

```
name.txt        <- theme name 
Previews/       <- optional PNG previews
theme/          <- the theme itself (normal FBI theme layout); extracted to sdmc:/fbi/theme
```

* Themes live in `Authors/<Author>/<Theme>/<Theme>.motheme`.

## themestore.json format

```json
{
  "store":  { "title": "...", "author": "...", "description": "...", "format": 1, "revision": 1 },
  "themes": [
    { "name": "Simple Dark", "author": "1ted59", "version": "v1", "description": "",
      "previews": 2, "size": 69645, "url": "https://raw.githubusercontent.com/.../Simple%20Dark.motheme" }
  ]
}
```
FBI-MO reads `name`, `author`, `version`, `description` and `url`.
