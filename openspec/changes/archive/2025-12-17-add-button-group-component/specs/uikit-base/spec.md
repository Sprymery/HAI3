## ADDED Requirements

### Requirement: Button Group Component

The UI kit SHALL provide ButtonGroup, ButtonGroupText, and ButtonGroupSeparator components in the `@hai3/uikit` package for visually grouping related buttons with consistent spacing and connected appearance, built on @radix-ui/react-slot for polymorphic composition.

#### Scenario: Button Group component is available

- **WHEN** importing ButtonGroup from `@hai3/uikit`
- **THEN** all Button Group sub-components are available: ButtonGroup, ButtonGroupText, ButtonGroupSeparator
- **AND** buttonGroupVariants is exported for external styling

#### Scenario: ButtonGroup container

- **WHEN** using ButtonGroup to wrap button components
- **THEN** the container displays with flex layout and w-fit sizing
- **AND** the container has role="group" for accessibility
- **AND** the container has data-slot="button-group" attribute
- **AND** the container has data-orientation attribute reflecting current orientation
- **AND** child buttons receive focus z-index boost via [&>*]:focus-visible:z-10

#### Scenario: Horizontal orientation (default)

- **WHEN** using ButtonGroup with default or orientation="horizontal"
- **THEN** buttons display in a horizontal row
- **AND** intermediate buttons have border-radius removed on adjacent sides
- **AND** intermediate buttons have left border removed to prevent double borders
- **AND** first button keeps left border-radius, last button keeps right border-radius

#### Scenario: Vertical orientation

- **WHEN** using ButtonGroup with orientation="vertical"
- **THEN** buttons display in a vertical column via flex-col
- **AND** intermediate buttons have border-radius removed on adjacent sides
- **AND** intermediate buttons have top border removed to prevent double borders
- **AND** first button keeps top border-radius, last button keeps bottom border-radius

#### Scenario: Nested ButtonGroups

- **WHEN** placing ButtonGroup components inside another ButtonGroup
- **THEN** nested groups receive gap-2 spacing via has-[>[data-slot=button-group]]:gap-2
- **AND** nested groups function independently with their own orientation

#### Scenario: ButtonGroupText component

- **WHEN** using ButtonGroupText to display static text or labels
- **THEN** the text displays with bg-muted background
- **AND** the text has rounded-md border with px-4 padding
- **AND** the text has shadow-xs for subtle depth
- **AND** icons within text have pointer-events-none and size-4 defaults
- **AND** asChild prop enables polymorphic composition via Slot

#### Scenario: ButtonGroupSeparator component

- **WHEN** using ButtonGroupSeparator between buttons
- **THEN** a visual divider is rendered using the Separator component
- **AND** the separator has data-slot="button-group-separator" attribute
- **AND** the separator defaults to vertical orientation
- **AND** the separator has bg-input styling and self-stretch sizing
- **AND** the separator removes default margins (!m-0)

#### Scenario: Select trigger integration

- **WHEN** using Select component triggers within ButtonGroup
- **THEN** select triggers without explicit width class get w-fit
- **AND** hidden select elements at end preserve border-radius on visible trigger

### Requirement: Button Group Demo Examples

The UI kit demo SHALL provide examples for the Button Group component in the Actions & Buttons category demonstrating size variants, nested groups, and orientation options, using `tk()` for translations.

#### Scenario: Button Group section in ActionsElements

- **WHEN** viewing the Actions & Buttons category
- **THEN** a Button Group section is displayed with heading and examples
- **AND** the section includes data-element-id="element-button-group" for navigation

#### Scenario: Button Group examples use translations

- **WHEN** Button Group examples are rendered
- **THEN** all text content uses the `tk()` translation helper
- **AND** all translated text is wrapped with TextLoader component

#### Scenario: Size example

- **WHEN** viewing the Button Group size example
- **THEN** three button groups are displayed showing sm, default, and lg sizes
- **AND** each group contains multiple outline buttons with text labels
- **AND** each group includes an icon-only button with PlusIcon

#### Scenario: Nested example

- **WHEN** viewing the Button Group nested example
- **THEN** a parent ButtonGroup contains two nested ButtonGroups
- **AND** one nested group contains numbered page buttons (1, 2, 3, 4, 5)
- **AND** another nested group contains navigation icon buttons (previous, next)
- **AND** aria-label attributes provide accessibility for icon buttons

#### Scenario: Orientation example

- **WHEN** viewing the Button Group orientation example
- **THEN** a vertical ButtonGroup is displayed
- **AND** the group contains Plus and Minus icon buttons
- **AND** the group has aria-label="Media controls" for accessibility

### Requirement: Button Group in Category System

The UI kit element registry SHALL include 'Button Group' in the `IMPLEMENTED_ELEMENTS` array to mark it as an available component in the Actions & Buttons category.

#### Scenario: Category Menu Shows Button Group

- **WHEN** viewing the UIKit category menu
- **THEN** Button Group appears as an implemented element in Actions & Buttons category
- **AND** Button Group is positioned after Button in the category elements list

### Requirement: Button Group Translations

The UI kit translations SHALL provide localized strings for all 36 supported languages with keys including:
- `button_group_heading` - Section heading
- `button_group_size_label` - Size variants example label
- `button_group_nested_label` - Nested groups example label
- `button_group_orientation_label` - Orientation example label
- Button labels: `button_group_small`, `button_group_default`, `button_group_large`

#### Scenario: Translated Button Group Labels

- **WHEN** viewing the Button Group demo in a non-English language
- **THEN** all Button Group labels and descriptions display in the selected language
- **AND** translations are contextually appropriate for UI action terminology
