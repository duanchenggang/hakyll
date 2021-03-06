---
title: Releases
---

# Releases

## Hakyll 4.7.2.3

- Fix time dependency in tests

## Hakyll 4.7.2.2

- Relax time dependency

## Hakyll 4.7.2.1

- Bump fsnotify dependency to 0.2

## Hakyll 4.7.2.0

- Improve documentation of `getResourceXXX` functions (contribution by Matthias
  C. M. Troffaes)
- Allow for empty templates
- Bump pandoc dependency to 1.15

## Hakyll 4.7.1.0

- Drop old-time, old-locale, time-locale-compat dependencies
- Add convenicence `pandocBiblioCompiler` (contribution by
  Matthias C. M. Troffaes)
- Add support for mediawiki (contribution by Chen Lei)

## Hakyll 4.7.0.0

- Bump pandoc to 1.14. This will break a lot of sites: since the pandoc parser
  might now return an error message, it is ran inside the `Compiler` monad where
  we can nicely handle the error.

## Hakyll 4.6.9.0

- Let caller decide exit (fix by Erik Dominikus)
- Bump pandoc-citeproc dependency

## Hakyll 4.6.8.1

- Fix test suite dependencies

## Hakyll 4.6.8.0

- Fix building on GHC 7.10 (fix by Charles Strahan)
- Add support for a custom teaser separator (contribution by Tom Sydney
  Kerckhove)
- Let Pandoc handle DocBook files (contribution by Joshua SImmons)

## Hakyll 4.6.7.1

- Bump dependencies

## Hakyll 4.6.7.0

- Bump dependencies
- Fix bug where hakyll-init would create a file called `name.cabal.cabal` (fix
  by Hans-Peter Deifel)

## Hakyll 4.6.6.0

- Fix compilation error when preview server is disabled (fix by Magnus Therning)
- Add author name by default to RSS feeds (contribution by Calen Pennington)

## Hakyll 4.6.5.0

- Bump dependencies
- Fix garbled "Listening on 0.0.0.0:8000" message
- Add `boolField` (contribution by Ferenc Wágner)

## Hakyll 4.6.4.0

- Fix another dependency handling bug when using snapshots
- Add `matchMetadata` for examining metadata when defining rules

## Hakyll 4.6.3.0

- Fix dependency handling bug

## Hakyll 4.6.2.0

- Loosen `binary` dependency
- Make dependency handling more granular so you can depend on specific snapshots
  of an item

## Hakyll 4.6.1.0

- Bump `fsnotify` and `pandoc-citeproc` dependencies
- Rewrite polling code a bit

## Hakyll 4.6.0.0

- Added `listFieldWith` function
- Improved `rulesExtraDependencies` behaviour
- Changed function syntax in templates from `$foo arg1 arg2$` to
  `$foo("arg1", "arg2")$`
- Support parsing date from directory names in addition to file names

## Hakyll 4.5.5.0

- Fix Binary instances for `pandoc` and `pandoc-citeproc`
- Fix `network-uri` dependency issue

## Hakyll 4.5.4.0

- Fix issue with HTML entities when running `withUrls` and `demoteHeaders`.
- Generate a cabal file for the initialised site.
- Add pagination support.

## Hakyll 4.5.3.0

- Bump Pandoc to 1.12.4 to include the org-mode reader.

## Hakyll 4.5.2.0

- Fix rebuilding everything issue with latest directory (contribution by Jorge
  Israel Peña)
- Fix issue with `toSiteRoot` (contribution by Izzy Cecil)
- Fix issue with tag dependencies, slightly improve caching

## Hakyll 4.5.0.0

- Fix issue with syntax highlighting and line numbers (contribution by Adelbert
  Chang)
- Improve documentation for `Context` (contribution by Daniil Frumin)
- Added `IsString` instance for `Template`
- Added the `pandocCompilerWithTransformM` function (contribution by Daniil
  Frumin)
- Make `./site check` return the right exit code (contribution by Andres Loeh)
- Use OS threads to make `./site watch` work nicely on Windows (contribution by
  Simonas Kazlauskas)
- Make the `unixFilter` function work better on windows by calling `shell`
  (contribution by Collin J. Doering)
- Add a command-line flag to bind on a user-specified host (contribution by
  chrisdotcode)

## Hakyll 4.4.3.0

- Fix issue when using `metadataRoute` after other custom routes

## Hakyll 4.4.2.0

- Fix issue where Hakyll would not detect a change if a `.metadata` file was
  deleted

## Hakyll 4.4.1.0

- Use Pandoc 1.12 highlighting by default

## Hakyll 4.4.0.0

- Update to work with Pandoc 1.12. This changes the type of `readPandocBibilio`:
  the `CSL` argument is no longer optional (contribution by Jorge Israel Peña)

- Fix incorrect output of `toSiteRoot` on windows (contribution by Saeid
  Al-Wazzan)

- Add a preview port option to `Configuration` (contribution by Jorge Israel
  Peña)

- Add `watch` command that polls for changes but does not necessarily launch a
  server (contribution by Eric Stolten)

- Generalise type of `metadataField`

- Fix issue where metadata was not correctly loaded when using versions

## Hakyll 4.3.3.0

- Re-add the `functionField` function

## Hakyll 4.3.2.0

- Re-add the `mapContext` function

- Unescape internal URLs when using `./site check` (contribution by Marc-Antoine
  Perennou)

## Hakyll 4.3.1.0

- Make teasers undefined if no `<!--more-->` comment is found

- Sanitize tag URLs (contribution by Simonas Kazlauskas)

## Hakyll 4.3.0.0

- Add conditionals, partials and for loops to the template system (includes a
  contribution by Ivan N. Veselov)

- Improvements to the preview functionality on windows (contribution by Jorge
  Israel Peña)

- Add pagination support (contribution by Anton Dubovik)

- Slight speedup for the Hakyll cache (contribution by justnoxx)

- Add teaser functionality (contribution by Ivan N. Veselov)

- Make `./site check` work with scheme-relative URLs (contribution by Simonas
  Kazlauskas)

- The `./site deploy` command can now be customized with Haskell code
  (contribution by Samuel Tardieu)

- Use `hsnotify` for proper polling instead of sleep loop on all platforms
  (contribution by Simonas Kazlauskas)

- More useful debug info available

## Hakyll 4.2.2.0

- Fix issue with `Alternative` instance of `Compiler`

## Hakyll 4.2.1.1

*March 9, 2013*

- Make `http-conduit` dependency optional by adding a `checkExternal` cabal flag

## Hakyll 4.2.1.0

*March 7, 2013*

- Fix issue where `copyFileCompiler` ignored `providerDirectory`

## Hakyll 4.2.0.0

*March 7, 2013*

- Read second extension for `.lhs`, e.g. `.md.lhs` or `.tex.lhs` (contribution
  by Alexander Vershilov)

- Speedup initialization by using modification times instead of hashing files

- Speedup initialization with a rewritten resource provider

- Fix `./site check` not working with sites that require a user agent (e.g.
  <http://www.wikipedia.org/>)

- Change `chronological` and `recentFirst` to actually look at the dates of
  items. This changes their types from:

        chronological, recentFirst :: [Item a] -> [Item a]

    to:

        chronological, recentFirst
            :: MonadMetadata m => [Item a] -> m [Item a]

    (contribution by Simonas Kazlauskas)

- Add `metadataRoute`, so it is now possible to use metadata when determining
  routes

- Improve metadata parser for multiline metadata fields (contribution by Peter
  Jones)

- Add the `getMetadataField` utility

## Hakyll 4.1.4.0

*January 26, 2013*

- Export the flexible `renderTags` function

## Hakyll 4.1.3.0

*January 26, 2013*

- Export the constructor of the `Tags` datatype

## Hakyll 4.1.2.0

*January 20, 2013*

- Fix an issue where a dependency cycle would lead to infinite recursion/stack
  overflow

## Hakyll 4.1.1.0

*January 20, 2013*

- Fix an issue regarding `relativizeUrls` expanding `<meta />` to
  `<meta></meta>`

## Hakyll 4.1.0.0

*January 20, 2013*

Update to use Pandoc 1.10, this requires changes to your `site.hs` if you're
using custom Pandoc options or the `Hakyll.Web.Pandoc.Biblio` module.

- `defaultHakyllParserState` renamed to `defaultHakyllReaderOptions`

- The type of `readPandocBiblio` changed

Because of the many changes, this release is no longer compatible with Pandoc
1.9.

## Hakyll 4.0.0.0

*January 16, 2013*

The Initial release of Hakyll 4, see
[this blogpost](http://jaspervdj.be/posts/2013-01-16-hakyll-4.0.html) and
[the migration guide](/tutorials/hakyll-3-to-hakyll4-migration-guide.html) for
an overview of changes.
