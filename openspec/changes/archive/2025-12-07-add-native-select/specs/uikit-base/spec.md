## ADDED Requirements

### Requirement: Native Select Component

The UI kit SHALL provide `NativeSelect`, `NativeSelectOption`, and `NativeSelectOptGroup` components using native HTML select elements for lightweight dropdown selection with proper styling and accessibility.

#### Scenario: Native Select component is available

- **WHEN** importing NativeSelect from `@hai3/uikit`
- **THEN** the NativeSelect, NativeSelectOption, and NativeSelectOptGroup components are available
- **AND** components support all standard HTML select/option/optgroup props

#### Scenario: Native Select styling

- **WHEN** NativeSelect is rendered
- **THEN** the select has consistent styling with other form inputs
- **AND** a chevron down icon is displayed on the right side
- **AND** native browser appearance is hidden

#### Scenario: Native Select disabled state

- **WHEN** NativeSelect has disabled prop
- **THEN** the select shows disabled styling (opacity, cursor)
- **AND** the select cannot be interacted with

#### Scenario: Native Select invalid state

- **WHEN** NativeSelect has aria-invalid="true"
- **THEN** destructive ring styling is applied
- **AND** the border shows destructive color

### Requirement: Native Select Demo Examples

The UI kit demo SHALL provide examples for the Native Select component in the Forms & Inputs category demonstrating default select, option groups, disabled state, and invalid state, using `tk()` for translations.

#### Scenario: Demo Example Display

- **WHEN** viewing the Forms & Inputs category in UIKitElementsScreen
- **THEN** a Native Select section is displayed with heading and examples
- **AND** the section includes `data-element-id="element-native-select"` for navigation

#### Scenario: Multiple native select examples

- **WHEN** viewing the Native Select section
- **THEN** examples demonstrate: default with options, option groups, disabled, and invalid states
- **AND** each example has a descriptive label using translations

### Requirement: Native Select in Category System

The UI kit element registry SHALL include 'Native Select' in the `IMPLEMENTED_ELEMENTS` array to mark it as an available component in the Forms & Inputs category.

#### Scenario: Category Menu Shows Native Select

- **WHEN** viewing the UIKit category menu
- **THEN** Native Select appears as an implemented element in Forms & Inputs category

### Requirement: Native Select Translations

The UI kit translations SHALL provide localized strings for all 36 supported languages with keys including:
- `native_select_heading` - Section heading
- `native_select_default_label` - Default example label
- `native_select_groups_label` - Option groups example label
- `native_select_disabled_label` - Disabled example label
- `native_select_invalid_label` - Invalid example label
- `native_select_placeholder` - Placeholder text
- `native_select_department_*` - Department options

#### Scenario: Translated Native Select Labels

- **WHEN** viewing the native select demo in a non-English language
- **THEN** all native select labels and options display in the selected language
