# Change: Add Button Group Base Component

## Why

The UI Kit needs a ButtonGroup component to group related buttons together with consistent spacing and visual connection. This is a common UI pattern for toolbars, pagination controls, and action groups. Button Group is already planned in the "Actions & Buttons" category but not yet implemented.

## What Changes

- Add `ButtonGroup`, `ButtonGroupText`, `ButtonGroupSeparator` components to `@hai3/uikit`
- Export `buttonGroupVariants` for external styling
- Support horizontal and vertical orientations
- Add demo examples showing size variants, nested groups, and orientation
- Add translations for all 36 supported languages
- Add 'Button Group' to `IMPLEMENTED_ELEMENTS` array

## Impact

- Affected specs: `uikit-base`
- Affected code:
  - `packages/uikit/src/base/button-group.tsx` (new file)
  - `packages/uikit/src/base/index.ts` (export)
  - `src/screensets/demo/screens/uikit/elements/ActionsElements.tsx` (demo)
  - `src/screensets/demo/screens/uikit/uikitCategories.ts` (IMPLEMENTED_ELEMENTS)
  - `src/screensets/demo/screens/uikit/i18n/*.json` (36 files)
