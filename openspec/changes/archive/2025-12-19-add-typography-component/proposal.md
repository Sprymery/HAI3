# Change: Add Typography Base Component

## Why

The UI Kit needs Typography components for consistent text styling across the application. Typography is already planned in the "Data Display" category but not yet implemented. These components provide semantic HTML elements with pre-configured Tailwind CSS classes for headings, paragraphs, blockquotes, lists, code, and text variations.

## What Changes

- Add Typography components to `@hai3/uikit` (H1, H2, H3, H4, P, Blockquote, List, InlineCode, Large, Small, Muted)
- Add demo examples showing all typography variants
- Add translations for all 36 supported languages
- Add 'Typography' to `IMPLEMENTED_ELEMENTS` array

## Impact

- Affected specs: `uikit-base`
- Affected code:
  - `packages/uikit/src/base/typography.tsx` (new file)
  - `packages/uikit/src/index.ts` (export)
  - `src/screensets/demo/components/DataDisplayElements.tsx` (demo)
  - `src/screensets/demo/screens/uikit/uikitCategories.ts` (IMPLEMENTED_ELEMENTS)
  - `src/screensets/demo/screens/uikit/i18n/*.json` (36 files)
