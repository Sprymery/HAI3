## 1. Implementation

- [x] 1.1 Create `packages/uikit/src/base/empty.tsx` with Empty, EmptyHeader, EmptyMedia (with cva variants), EmptyTitle, EmptyDescription, EmptyContent
- [x] 1.2 Export all Empty components from `packages/uikit/src/index.ts`
- [x] 1.3 Add 'Empty' to IMPLEMENTED_ELEMENTS in `src/screensets/demo/screens/uikit/uikitCategories.ts`

## 2. Demo Examples

- [x] 2.1 Add Empty section to `FeedbackElements.tsx` with data-element-id="element-empty"
- [x] 2.2 Create outline example (border dashed, icon variant, cloud icon)
- [x] 2.3 Create muted background example (gradient background, notification icon)
- [x] 2.4 Create avatar example (default variant with Avatar component)

## 3. Translations

- [x] 3.1 Add translation keys for Empty demo (empty_heading, empty_outline_*, empty_muted_*, empty_avatar_*)
- [x] 3.2 Update all 36 language files with Empty translations

## 4. Validation

- [x] 4.1 Run `npm run arch:check` to verify architecture compliance
- [x] 4.2 Build packages with `npm run build:packages`
- [x] 4.3 Visual verification in browser via `npm run dev`
