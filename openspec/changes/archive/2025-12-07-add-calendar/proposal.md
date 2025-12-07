# Add Calendar Base UI Kit Element

## Purpose

Add a Calendar component to the `@hai3/uikit` package for date selection, built on the react-day-picker library with extensive customization options.

## What Changes

1. **New Package Dependencies**: Install `react-day-picker` and `date-fns` in packages/uikit
2. **New Component**: Create `calendar.tsx` in packages/uikit/src/base/ with Calendar and CalendarDayButton components
3. **Export**: Add exports to packages/uikit/src/index.ts
4. **Demo**: Add Calendar examples to FormElements.tsx with 8 variations:
   - Persian/Hijri/Jalali Calendar
   - Selected Date (With TimeZone)
   - Range Calendar
   - Month and Year Selector
   - Date of Birth Picker
   - Date and Time Picker
   - Natural Language Picker
   - Custom Cell Size
5. **Translations**: Add translation keys to all 36 language files
6. **Category System**: Add 'Calendar' to IMPLEMENTED_ELEMENTS array

## Impact

- Medium complexity: Multiple demo variations showcasing different capabilities
- New dependencies: `react-day-picker`, `date-fns`
- Uses existing internal icons: ChevronDownIcon, ChevronLeftIcon, ChevronRightIcon
- No breaking changes to existing components
