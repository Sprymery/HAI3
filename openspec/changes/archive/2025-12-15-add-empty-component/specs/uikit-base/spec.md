## ADDED Requirements

### Requirement: Empty Component

The system SHALL provide an Empty component in the `@hai3/uikit` package for displaying placeholder content when no data is available.

#### Scenario: Empty component is available

- **WHEN** importing Empty from `@hai3/uikit`
- **THEN** the Empty component and its sub-components are available
- **AND** components include: Empty, EmptyHeader, EmptyMedia, EmptyTitle, EmptyDescription, EmptyContent

#### Scenario: Empty container layout

- **WHEN** using Empty component
- **THEN** the container is displayed as a flex column with centered items
- **AND** the container has rounded-lg corners, dashed border style, and balanced text
- **AND** the container has responsive padding (p-6 on mobile, p-12 on md+)

#### Scenario: EmptyMedia with default variant

- **WHEN** using EmptyMedia with variant="default" or no variant
- **THEN** the media container has transparent background
- **AND** the container is flex with centered items

#### Scenario: EmptyMedia with icon variant

- **WHEN** using EmptyMedia with variant="icon"
- **THEN** the media container has bg-muted background with size-10
- **AND** the container has rounded-lg corners
- **AND** SVG icons inside are sized to size-6 by default

#### Scenario: Empty styling follows theme

- **WHEN** rendering Empty components
- **THEN** EmptyTitle uses text-lg font-medium tracking-tight
- **AND** EmptyDescription uses text-muted-foreground text-sm/relaxed
- **AND** EmptyDescription links have underline with underline-offset-4

### Requirement: Empty Demo Examples

The system SHALL provide Empty examples in the Feedback & Status category of the UI Kit demo.

#### Scenario: Empty section in FeedbackElements

- **WHEN** viewing the Feedback & Status category
- **THEN** an Empty section is displayed with heading and examples
- **AND** the section includes data-element-id="element-empty" for navigation

#### Scenario: Empty examples use translations

- **WHEN** Empty examples are rendered
- **THEN** all text content uses the `tk()` translation helper
- **AND** all translated text is wrapped with TextLoader component

#### Scenario: Multiple empty state examples

- **WHEN** viewing the Empty section
- **THEN** at least 3 empty state examples are shown: outline, muted background, and avatar
- **AND** each example demonstrates different EmptyMedia variants and styling options

### Requirement: Empty in Category System

The system SHALL include Empty as an implemented element in the Feedback & Status category.

#### Scenario: Empty in IMPLEMENTED_ELEMENTS

- **WHEN** checking `uikitCategories.ts`
- **THEN** 'Empty' is included in the IMPLEMENTED_ELEMENTS array
- **AND** Empty appears in the Feedback & Status category navigation menu

### Requirement: Empty Translations

The system SHALL provide Empty translations across all supported languages (36 languages).

#### Scenario: Empty translation keys

- **WHEN** Empty component is used in the demo
- **THEN** translation keys exist for all Empty elements
- **AND** keys include: empty_heading, empty_outline_title, empty_outline_description, empty_muted_title, empty_muted_description, empty_avatar_title, empty_avatar_description

#### Scenario: Translation files completeness

- **WHEN** checking translation files in `src/screensets/demo/screens/uikit/i18n/`
- **THEN** all 36 language files include Empty translation keys
- **AND** translations are contextually appropriate for each language
