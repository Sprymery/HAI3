## ADDED Requirements

### Requirement: Toggle Component

The UI kit SHALL provide Toggle and toggleVariants in the `@hai3/uikit` package for creating togglable buttons that switch between on/off states, built on the `@radix-ui/react-toggle` library.

#### Scenario: Toggle component is available

- **WHEN** importing Toggle from `@hai3/uikit`
- **THEN** Toggle component and toggleVariants are available
- **AND** the component supports all standard @radix-ui/react-toggle props

#### Scenario: Toggle styling

- **WHEN** using Toggle component
- **THEN** the toggle displays with inline-flex, items-center, justify-center layout
- **AND** the toggle has rounded-md, text-sm, font-medium styling
- **AND** hover state shows bg-muted and text-muted-foreground
- **AND** pressed state (data-[state=on]) shows bg-accent and text-accent-foreground
- **AND** disabled state has pointer-events-none and opacity-50
- **AND** icons within have consistent sizing (size-4) and shrink-0
- **AND** the toggle has data-slot="toggle" attribute

#### Scenario: Toggle variants

- **WHEN** using Toggle with variant prop
- **THEN** "default" variant has bg-transparent
- **AND** "outline" variant has border, border-input, bg-transparent, shadow-xs
- **AND** "outline" variant hover shows bg-accent and text-accent-foreground

#### Scenario: Toggle sizes

- **WHEN** using Toggle with size prop
- **THEN** "sm" size has h-8, px-1.5, min-w-8
- **AND** "default" size has h-9, px-2, min-w-9
- **AND** "lg" size has h-10, px-2.5, min-w-10

### Requirement: Toggle Demo Examples

The UI kit demo SHALL provide examples for the Toggle component in the Actions & Buttons category demonstrating variants, sizes, and disabled states.

#### Scenario: Toggle section in ActionElements

- **WHEN** viewing the Actions & Buttons category
- **THEN** a Toggle section is displayed with heading and examples
- **AND** the section includes data-element-id="element-toggle" for navigation

#### Scenario: Toggle examples use translations

- **WHEN** Toggle examples are rendered
- **THEN** all text content uses the `tk()` translation helper
- **AND** all translated text is wrapped with TextLoader component

#### Scenario: Toggle example content

- **WHEN** viewing the Toggle section
- **THEN** a default toggle with icon and text is shown
- **AND** an outline variant toggle with bookmark icon is shown
- **AND** a disabled toggle is shown

### Requirement: Toggle in Category System

The UI kit element registry SHALL include 'Toggle' in the `IMPLEMENTED_ELEMENTS` array to mark it as an available component in the Actions & Buttons category.

#### Scenario: Category Menu Shows Toggle

- **WHEN** viewing the UIKit category menu
- **THEN** Toggle appears as an implemented element in Actions & Buttons category
- **AND** Toggle is positioned alphabetically among other action elements

### Requirement: Toggle Translations

The UI kit translations SHALL provide localized strings for all 36 supported languages with keys including:
- `toggle_heading` - Section heading
- `toggle_default_label` - Default variant label
- `toggle_outline_label` - Outline variant label
- `toggle_disabled_label` - Disabled state label
- `toggle_italic` - Italic text
- `toggle_bookmark` - Bookmark text

#### Scenario: Translated Toggle Labels

- **WHEN** viewing the Toggle demo in a non-English language
- **THEN** all Toggle labels and text display in the selected language
- **AND** translations are contextually appropriate for toggle button terminology
