# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project will adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) when it reaches `v1.0.0`.

## [Unreleased]

### Changed

- **BREAKING `remirror/react-utils`:** Rename `childIsFunction` to `propIsFunction` and make it a _pseudo_ predicate function (returns true when it doesn't throw an error).
- Add support for [Git Large File Storage (LFS)](https://git-lfs.github.com/)
- `remirror/editor-twitter`, `remirror/editor-wysiwyg` : Use image-snapshot testing to ensure SSR and DOM rendered editors are identical

## [0.2.0] - 2019-06-18

### Added

- Support for server side rendering (SSR) with passing integration tests for NextJS.
- Support for plain extension with styles impacting SSR (PlaceholderExtension can be rendered in SSR).
- **`remirror/core`:** `ssrTransformer` added to extension methods as a way of wrapping and transforming the JSX element produced on the server.
- **`remirror/core`:** `SSRComponent: React.ComponentType<any>` option added to `MarkExtensionOptions` and `NodeExtensionOptions` as a way of overriding the component rendered in an SSR environment.
- **`remirror/core`:** `SSRHelpersExtension` added as a shorthand way of defining SSR transformations via ssrTransformer.
- **`remirror/core`:** `injectBrIntoEmptyParagraphs` added for better SSR rendering.
- **`remirror/react-utils`:** `isReactFragment` added to test if an element is a fragment.
- Create better unit tests for SSR.
- Add a changelog with changes starting from `v0.1.0`

### Changed

- **BREAKING:** Rename `@remirror/ui-*` packages to `@remirror/editor-*` for example @remirror/ui-twitter is .now called `@remirror/editor-twitter`.
- **BREAKING `remirror/editor-twitter`:** Rename `UITwitter` and `TwitterUI` to `TwitterEditor`
- **BREAKING `remirror/editor-markdown`:** Rename `UIMarkdown` and `MarkdownUI` to `MarkdownEditor`
- **BREAKING `remirror/editor-wysiwyg`:** Rename `UIWysiwyg` and `WysiwygUI` to `WysiwygEditor`
- Speed up tslint by enforcing linting on individual modules (new `tsconfig.lint.json` files).
- Remove `cx` import from `emotion` library in from `@remirror/core` to reduce the bundle size.
- Set `@emotion/core` and `@emotion/styled` as peer dependencies.

### Remove

- **BREAKING:** `@remirror/ui-*` packages.

## [0.1.0] - 2019-06-10

### Added

- Enable remirror as a controlled component #79 #78.
- @remirror/ui-markdown - Still in progress.
- @remirror/extension-multicursor - this is currently just a stub (almost no code).
- @remirror/api-documenter - will be used to generate the api documentation.

### Changed

- **BREAKING:** Rename all extensions to include an Extension postfix. e.g. Emoji is now EmojiExtension. This will hopefully reduce name collisions in the future.
- Improves the puppeteer testing by separating it out from unit tests in the package.
- Upgrade docz to v1 #65.
- General improvements to docs.
- Fixes missing TypeScript definitions #77.
- Fixes crash when rendering a ReactNodeView in NextJS #75.

[unreleased]: https://github.com/ifiokjr/remirror/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/ifiokjr/remirror/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/ifiokjr/remirror/releases/tag/v0.1.0