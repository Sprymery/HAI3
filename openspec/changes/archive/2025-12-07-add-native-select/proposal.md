# Change: Add Native Select Base UI Kit Element

## Why
Native Select provides a lightweight, browser-native dropdown alternative to the custom Select component. It offers better accessibility, mobile support, and smaller bundle size for simple use cases.

## What Changes
- Add `NativeSelect`, `NativeSelectOption`, and `NativeSelectOptGroup` base components
- Add `ChevronDownIcon` to the icons folder
- Export components from `@hai3/uikit` package
- Add demo examples in Forms & Inputs category with translations
- Mark Native Select as implemented in category system

## Impact
- Affected specs: `uikit-base`
- Affected code:
  - `packages/uikit/src/base/native-select.tsx` (new)
  - `packages/uikit/src/icons/ChevronDownIcon.tsx` (new)
  - `packages/uikit/src/index.ts`
  - `src/screensets/demo/components/FormElements.tsx`
  - `src/screensets/demo/screens/uikit/uikitCategories.ts`
  - `src/screensets/demo/screens/uikit/i18n/*.json` (36 language files)
