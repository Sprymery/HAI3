# Calendar Spec Delta

## ADDED Requirements

### Requirement: Calendar Component

The system SHALL provide a Calendar component in the `@hai3/uikit` package for date selection, built on the react-day-picker library.

#### Scenario: Calendar component is available

- **WHEN** importing Calendar from `@hai3/uikit`
- **THEN** the Calendar component and CalendarDayButton are available
- **AND** the component uses internal icons (ChevronDownIcon, ChevronLeftIcon, ChevronRightIcon)

#### Scenario: Calendar basic rendering

- **WHEN** using Calendar without props
- **THEN** a month calendar grid is rendered with navigation
- **AND** outside days are shown by default
- **AND** the current month is displayed

#### Scenario: Calendar RTL support

- **WHEN** using Calendar in RTL context
- **THEN** navigation chevrons are rotated appropriately
- **AND** layout adapts to right-to-left direction

#### Scenario: Calendar single selection

- **WHEN** using Calendar with mode="single"
- **THEN** clicking a day selects that single date
- **AND** the selected date is visually highlighted

#### Scenario: Calendar range selection

- **WHEN** using Calendar with mode="range"
- **THEN** clicking two dates creates a date range
- **AND** range start, middle, and end dates are styled distinctly

#### Scenario: Calendar month/year dropdown

- **WHEN** using Calendar with captionLayout="dropdown"
- **THEN** month and year dropdowns are displayed
- **AND** users can quickly navigate to different months/years

#### Scenario: Calendar custom cell size

- **WHEN** using Calendar with custom --cell-size CSS variable
- **THEN** the calendar cells resize accordingly
- **AND** layout remains proportional

### Requirement: Calendar Demo Examples

The system SHALL provide Calendar examples in the Forms & Inputs category of the UI Kit demo.

#### Scenario: Calendar section in FormElements

- **WHEN** viewing the Forms & Inputs category
- **THEN** a Calendar section is displayed with heading and examples
- **AND** the section includes data-element-id="element-calendar" for navigation

#### Scenario: Calendar examples use translations

- **WHEN** Calendar examples are rendered
- **THEN** all text content uses the `tk()` translation helper
- **AND** all translated text is wrapped with TextLoader component

#### Scenario: Multiple Calendar examples

- **WHEN** viewing the Calendar section
- **THEN** 8 examples are shown demonstrating different capabilities
- **AND** examples include: Persian calendar, selected date with timezone, range, month/year selector, DOB picker, date-time picker, natural language, custom cell size

### Requirement: Calendar in Category System

The system SHALL include Calendar as an implemented element in the Forms & Inputs category.

#### Scenario: Calendar in IMPLEMENTED_ELEMENTS

- **WHEN** checking `uikitCategories.ts`
- **THEN** 'Calendar' is included in the IMPLEMENTED_ELEMENTS array
- **AND** Calendar appears in the Forms & Inputs category navigation menu

### Requirement: Calendar Translations

The system SHALL provide Calendar translations across all supported languages (36 languages).

#### Scenario: Calendar translation keys

- **WHEN** Calendar component is used in the demo
- **THEN** translation keys exist for all Calendar elements
- **AND** keys include headings and labels for all 8 example variations

#### Scenario: Translation files completeness

- **WHEN** checking translation files in `src/screensets/demo/screens/uikit/i18n/`
- **THEN** all 36 language files include Calendar translation keys
