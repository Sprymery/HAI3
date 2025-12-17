## 1. Dependency Installation

- [x] 1.1 Add `cmdk` package to `packages/uikit/package.json` dependencies

## 2. Component Implementation

- [x] 2.1 Create `packages/uikit/src/base/command.tsx` with Command, CommandDialog, CommandInput, CommandList, CommandEmpty, CommandGroup, CommandItem, CommandShortcut, CommandSeparator components
- [x] 2.2 Export all Command components from `packages/uikit/src/index.ts`

## 3. Demo Examples

- [x] 3.1 Add Command section to `ActionElements.tsx` with data-element-id="element-command"
- [x] 3.2 Create command dialog example with keyboard shortcut (⌘J) trigger
- [x] 3.3 Include grouped items (Suggestions, Settings) with icons and shortcuts

## 4. Category System

- [x] 4.1 Add 'Command' to `IMPLEMENTED_ELEMENTS` array in `uikitCategories.ts`

## 5. Translations

- [x] 5.1 Add translation keys to all 36 language files:
  - `command_heading` - Section heading
  - `command_press` - "Press" text
  - `command_placeholder` - Input placeholder
  - `command_no_results` - Empty state message
  - `command_suggestions` - Suggestions group heading
  - `command_settings` - Settings group heading
  - Item labels: calendar, search_emoji, calculator, profile, billing, settings

## 6. Validation

- [x] 6.1 Verify TypeScript compilation passes
- [x] 6.2 Run `npm run arch:check` to ensure architecture rules pass
- [x] 6.3 Visually verify component renders correctly in dev server
