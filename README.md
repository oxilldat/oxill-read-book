# Oxill Read Book

[Русский](README.ru.md) | **English**

A desktop-only EPUB, FB2, and PDF reader for Obsidian. Oxill Read Book brings
together a visual library, focused reading, highlights, quotes, book notes,
series, and local reading analytics.

> Oxill Read Book supports the desktop version of Obsidian only.

## Features

- Read EPUB, FB2, and PDF files without sending books to external services.
- Browse a visual library with covers, search, categories, and reading status.
- Organize books into series with ordering, categories, and custom covers.
- Switch between paged and scrolling reading modes.
- Use the table of contents and full-text book search.
- Create color highlights, comments, and links to exact places in a book.
- Export quotes to the book note or separate notes using templates.
- Group exported quotes under the headings inherited from the book.
- Create, select, and open a book note directly from the reader.
- Use named manual save points and one overwritable automatic save point.
- Track reading with a collapsible timer, pause, reset, and local sounds.
- Review reading statistics and a GitHub-style activity calendar.
- Optionally map highlight colors to List Callouts symbols.
- Use the interface in English or Russian.

## Installation

### Manual installation

1. Open your Obsidian vault directory.
2. Create `.obsidian/plugins/oxill-read-book`.
3. Copy the following release files into that directory:
   - `main.js`
   - `manifest.json`
   - `styles.css`
   - `assets` directory
   - `sounds` directory
4. Restart Obsidian or reload the installed plugins.
5. Enable **Oxill Read Book** under **Community plugins**.

## Getting started

Open the Obsidian command palette and run
**Oxill Read Book: Open library**. Add books by dragging them into the library
or by placing them in the configured books directory.

Settings for the current book are available from the reader toolbar. Global
reading, note, appearance, connector, and storage settings are available on
the plugin settings page.

## Differences from Elton Reader

Oxill Read Book is based on
[Elton Reader](https://github.com/swayinfo/elton-reader), but focuses on a
different desktop workflow:

- Mobile support and mobile-specific interface elements have been removed.
- The library includes a series view, series categories, ordering, and covers.
- Book notes store categories, series information, and the book number.
- Quote handling includes deletion synchronization, inherited headings,
  navigation to highlights, and per-book quote templates.
- A List Callouts connector maps highlight colors to symbols.
- Save points were redesigned and an overwritable automatic save was added.
- The reading timer has a compact panel, manual hiding, reset, and local sounds.
- Reading analytics include summary metrics and an activity calendar.
- The library, settings, context menus, and cover controls were redesigned.
- Translation and AI features were removed; reading data remains local.

This is an independent adaptation and is not an official Elton Reader release.

## Building from source

Node.js and npm are required.

```bash
npm install
npm run build
```

The plugin source is kept in the single `src/main.js` file. The generated
`main.js` embeds the PDF.js worker and can be loaded directly by Obsidian.

Run the code check with:

```bash
npx eslint src/main.js
```

## Privacy

Books, reading progress, highlights, notes, and analytics are processed
locally. The plugin requires no account and contains no telemetry. The optional
List Callouts integration also works locally.
