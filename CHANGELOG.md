## Version 7.0

### FEATURE

- Add a new [tree-sitter based](https://github.com/ikatyang/tree-sitter-vue) syntax for Vue files
- Support graphql blocks (requires external syntax extension)

#### NOTES ON THE NEW SYNTAX

The new tree-sitter based syntax is pretty much a one-to-one porting of the old one. However it comes with some caveats:

- PUG in templates will not be supported due to the new way of managing template blocks
- Coffeescript, SCSS, SASS and Less syntaxes are **not yet** supported. They will start working automatically as soon as Panic converts them to tree-sitter
- Under the hood the old syntax will still be shipped for backwards compatibility until Panic ends support

**Missing syntaxes workaround:**

If Coffeescript, SCSS, SASS or Less are essential to your workflow you can use the old syntax shipped as `Vue (Compatibility)`.\
By default a `.vue` file will use the new tree-sitter syntax so you have to set a **custom file type** rule in the settings `Settings -> Files -> Custom Types`.

## Version 6.2

### FIX

- Fix a bug that prevented the reload function to execute

## Version 6.1

### IMPROVE

- Add better error messages and notifications when something goes wrong with language server activation

### FIX

- Disable custom Volar LSP requests
- Fix minor issues with console outputs when errors occur

## Version 6.0

### FEATURE

- Support the new Volar language server. Check the README for the new required installation process
- Switch between the Volar and Vetur servers
- Support the i18n tag in the Vue file. Both in the `json` and `yaml` formats

### IMPROVE

- Simplify and speed up the extension by removing not so useful features and improving the code quality

## Version 5.4

### FIX

- Fix syntax detection of alternatives languages in style and script tags

## Version 5.3

### FIX

- Fix wrong version of VLS in production

## Version 5.2

### FIX

- Add missing Vue tags in scope selectors
- Add missing support for PUG syntax

## Version 5.1

### FIX

- Rolling back to VLS v0.5.7 because of issues with setting registration

## Version 5.0

### FEAT

- Display Vue version in the Information Sidebar

### IMPROVE

- Upgrade Vue Language Server to version v0.7.4
- Greatly improve Vue syntax long-term maintainability by using template-scopes
- Improve syntax REGEX for better matching Vue directives

### CHORE

- Upgrade development dependencies

## Version 4.2

### FIX

- Added missing highlighting for Nuxt unique kebab-case tags

## Version 4.1

### FIX

- Reverted VLS version to 0.5.7 for unknown breaking issues

## Version 4.0

### NEW

- Exposed VLS settings for both Global and per Project
- Added a new Information Sidebar
- Updated the version of VLS (0.7.2)
- Added informative notifications
- Added new commands for the extension
- Added a Clip for scaffolding a Vue file with POSTCSS

### IMPROVED

- Improved general stability and maintanability with better structure and comments
- Polished the main extension object
- Polished the VueLanguageClient class
- Uniformed all the logs, notifications and alerts
- Polished the syntax definition

### DOCS

- Improved the general quality and structure of the README
- Add a new Help section with some troubleshooting information

## Version 3.4

### FIX

- Removed single template block syntax which causes problems in Nova 4

## Version 3.3

### FIX

- Fixed broken single template block syntax in Nova 4

## Version 3.2

### FIX

- Fixed broken script and style blocks syntax in Nova 4

## Version 3.1

### DOCS

- Added warning for Nova crash without pug extension

## Version 3.0

### FEATURE

- Added support for PUG syntax

## Version 2.3

### CHORE

- Upgrade VLS to v0.5.7

## Version 2.2

### FEATURE

- Added the extension icon

## Version 2.1

### FIX

- Fixed syntax error with v-directives cut-off

## Version 2.0

### FEATURE

- Added support for template interpolation suggestions
- Configured Vetur for using workspace dependencies
- Typescript: Auto import completions

### CHORE

- Upgrade VLS to v0.5.5

### FIX

- Closed Vetur format until Nova will support it
- Closed Vetur validation for preventing xxx errors to show up

## Version 1.5

### FIX

- Changed cut-off expression for v-directives that could cause the js block to not end correctly

## Version 1.4

### REFACTOR

- Changed how template tag is parsed
- Improved symbols definition for vue elements

### FIX

- Supported nested template tags

## Version 1.3

### FEATURE

- Added Vue specific styling hooks for Nova themes

### DOCS

- Added funding link in Extension Settings

## Version 1.2

### Chore

- Changed default mode for the extension
- Updated the help link for mode config

## Version 1.1

### Fix

- Upload the DOCS changes

## Version 1.0

### Feature

- Add the Vetur mode 🔥

## Version 0.9.1

### Fix

- Removed forgotten preference in the extension definition.

## Version 0.9.0

### Feature

- Added scaffolding Clips based on Sarah Drasner VSCode snippets.

WARNING: The Clips even if inspired by Sarah Drasner are not exactly the same. Triggers are different and the basic Vue scaffold has no longer scss but css.

## Version 0.8.2

### Fix

- Added different definitions for vue-directives single and double quoted in order to prevent errors with nested quotes

## Version 0.8.0

### Feature

- Added support for typescript and coffeescript
- Added support for scss, sass, less

### Fix

- Added missing equal-sign to v-for completion

## Version 0.7.1

### Docs

- Updated README with current state of development

## Version 0.7.0

### Feature

- Added Completions in vue-html for events, triggered by @ shorthand.

### Fix

- Changed vue-html syntax to encapsulate javascript inside vue-directives quotes.

### Refactor

- Changed Vue Completions structure to follow the Official API structure.

## Version 0.6.2

- Added support for npm packages.
- Removed no longer needed completions thanks to a bug fix from Panic.

## Version 0.6.1

Fixed a minor bug that displayed html, css and js completions in every tag. The completions are now shown only in the corresponding vue tag.

## Version 0.6.0

Added support for standard HTML, CSS, JS and WebAPI Completions.

## Version 0.5.1

Updated CHANGELOG with previous versions.

## Version 0.5.0

Added Completions for Vue API.

## Version 0.4.0

Basic features of Vue Syntax: custom tags, directives, interpolation.
