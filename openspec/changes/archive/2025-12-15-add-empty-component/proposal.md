# Change: Add Empty Base UI Kit Component

## Why

The UI Kit lacks an Empty state component for displaying placeholder content when no data is available. This is a common pattern in SaaS applications for empty lists, search results, notifications, and file storage.

## What Changes

- Add `Empty` base component with sub-components: `Empty`, `EmptyHeader`, `EmptyMedia`, `EmptyTitle`, `EmptyDescription`, `EmptyContent`
- `EmptyMedia` supports variants via class-variance-authority: `default` (transparent) and `icon` (styled container)
- Export all components from `@hai3/uikit` package
- Add to `IMPLEMENTED_ELEMENTS` array in `uikitCategories.ts`
- Add demo examples in `FeedbackElements.tsx` showcasing outline, muted background, and avatar variants

## Impact

- Affected specs: `uikit-base`
- Affected code:
  - `packages/uikit/src/base/empty.tsx` (new)
  - `packages/uikit/src/index.ts` (export)
  - `src/screensets/demo/screens/uikit/uikitCategories.ts` (IMPLEMENTED_ELEMENTS)
  - `src/screensets/demo/components/FeedbackElements.tsx` (demo)
  - Translation files in `src/screensets/demo/screens/uikit/i18n/` (36 languages)
