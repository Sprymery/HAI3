# Change: Add Command Base Component

## Why

The UI Kit needs a Command component (command palette/menu) for providing keyboard-driven navigation and search interfaces. This is a common UI pattern for power users and productivity applications. Command is already planned in the "Actions & Buttons" category but not yet implemented.

## What Changes

- Add `cmdk` dependency to `@hai3/uikit`
- Add `Command`, `CommandDialog`, `CommandInput`, `CommandList`, `CommandEmpty`, `CommandGroup`, `CommandItem`, `CommandShortcut`, `CommandSeparator` components
- Add demo example showing command dialog with keyboard shortcut trigger
- Add translations for all 36 supported languages
- Add 'Command' to `IMPLEMENTED_ELEMENTS` array

## Impact

- Affected specs: `uikit-base`
- Affected code:
  - `packages/uikit/package.json` (add cmdk dependency)
  - `packages/uikit/src/base/command.tsx` (new file)
  - `packages/uikit/src/index.ts` (export)
  - `src/screensets/demo/components/ActionElements.tsx` (demo)
  - `src/screensets/demo/screens/uikit/uikitCategories.ts` (IMPLEMENTED_ELEMENTS)
  - `src/screensets/demo/screens/uikit/i18n/*.json` (36 files)
