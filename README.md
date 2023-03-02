[![Latest Stable Version](https://poser.pugx.org/codeq/htmlwidget/v/stable)](https://packagist.org/packages/codeq/htmlwidget)
[![License](https://poser.pugx.org/codeq/htmlwidget/license)](LICENSE)

# HTML Widget for Neos CMS

## For new projects we recommend to use [CodeQ.HtmlContent](https://github.com/code-q-web-factory/CodeQ.HtmlContent), this will still be maintianed.

This package allows developers to create HTML widgets in the administration. Editors can reuse them across on the website.

Administrators and everyone with the role `CodeQ.HtmlWidget:HtmlWidgetDefinitionEditor` can create HTML Widget Definitions including HTML, CSS and JavaScript.

All editors can add those HTML Widgets as content NodeType without being able to change the content.

## Features

* Automatically removes JavaScript code in the backend, to not break the Neos Administration
* Reference used media assets in your widget definition, so these assets can not be deleted.
* Restricts editing of HTML widget definitions, while allowing editors to use those widgets

[![HTML Widget Demo](https://img.youtube.com/vi/pOhYHlYH_6Q/0.jpg)](https://www.youtube.com/watch?v=pOhYHlYH_6Q)

*The development and the public-releases of this package are generously sponsored by [Code Q Web Factory](http://codeq.at).*

## Installation

CodeQ.HtmlWidget is available via packagist. `"codeq/htmlwidget" : "^1.7"` to the require section of the composer.json
or run:

```bash
composer require codeq/htmlwidget
```

We use semantic-versioning so every breaking change will increase the major-version number.

## Use Case 1: Administrators create widgets, which can be used by editors

This is the default case and you just need to install the package. 

If you are planning to create a whole widget library, we recommend creating a separate, hidden Widget Definition page for that.

## Use Case 2: Developers can create HTML Widgets, no reuse planned

If you want to create HTML widgets, but don't want to reuse them you only need the 
`CodeQ.HtmlWidget:Content.HtmlWidgetDefinition`. Disable the reusing element in YAML:

```yaml
'CodeQ.HtmlWidget:Content.HtmlWidget':
  abstract: true
```

If your Neos user has no admin privilege, add the role `HtmlWidgetDefinitionEditor`.

## License

Licensed under MIT, see [LICENSE](LICENSE)

## Contribution

We will gladly accept contributions. Please send us pull requests.
