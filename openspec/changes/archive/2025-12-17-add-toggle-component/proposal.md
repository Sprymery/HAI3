# Change: Add Toggle Base Component

## Why

The UI Kit needs a Toggle component for creating togglable buttons that can switch between on/off states. This is commonly used for toolbar buttons, formatting controls, and feature toggles. Toggle is already planned in the "Actions & Buttons" category but not yet implemented.

## What Changes

- Add `@radix-ui/react-toggle` dependency to `@hai3/uikit`
- Add `Toggle` component with `toggleVariants` (default/outline variants, sm/default/lg sizes)
- Add demo examples showing toggle with text, outline variant, and disabled state
- Add translations for all 36 supported languages
- Add 'Toggle' to `IMPLEMENTED_ELEMENTS` array

## Impact

- Affected specs: `uikit-base`
- Affected code:
  - `packages/uikit/package.json` (add @radix-ui/react-toggle dependency)
  - `packages/uikit/src/base/toggle.tsx` (new file)
  - `packages/uikit/src/index.ts` (export)
  - `src/screensets/demo/components/ActionElements.tsx` (demo)
  - `src/screensets/demo/screens/uikit/uikitCategories.ts` (IMPLEMENTED_ELEMENTS)
  - `src/screensets/demo/screens/uikit/i18n/*.json` (36 files)
