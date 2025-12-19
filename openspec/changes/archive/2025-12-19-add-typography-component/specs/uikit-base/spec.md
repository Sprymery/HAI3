## ADDED Requirements

### Requirement: Typography Components

The UI kit SHALL provide Typography components in the `@hai3/uikit` package for consistent text styling with semantic HTML elements and Tailwind CSS classes.

#### Scenario: Typography components are available

- **WHEN** importing Typography from `@hai3/uikit`
- **THEN** TypographyH1, TypographyH2, TypographyH3, TypographyH4 heading components are available
- **AND** TypographyP, TypographyLarge, TypographySmall, TypographyMuted text components are available
- **AND** TypographyBlockquote, TypographyList, TypographyInlineCode components are available
- **AND** the components support standard HTML element props via className extension

#### Scenario: Heading typography styling

- **WHEN** using TypographyH1
- **THEN** the element renders as `<h1>` with scroll-m-20, text-4xl, font-extrabold, tracking-tight styling
- **WHEN** using TypographyH2
- **THEN** the element renders as `<h2>` with scroll-m-20, border-b, pb-2, text-3xl, font-semibold, tracking-tight styling
- **WHEN** using TypographyH3
- **THEN** the element renders as `<h3>` with scroll-m-20, text-2xl, font-semibold, tracking-tight styling
- **WHEN** using TypographyH4
- **THEN** the element renders as `<h4>` with scroll-m-20, text-xl, font-semibold, tracking-tight styling

#### Scenario: Body text typography styling

- **WHEN** using TypographyP
- **THEN** the element renders as `<p>` with leading-7 and margin-top for non-first-child
- **WHEN** using TypographyLarge
- **THEN** the element renders as `<div>` with text-lg and font-semibold
- **WHEN** using TypographySmall
- **THEN** the element renders as `<small>` with text-sm, leading-none, font-medium
- **WHEN** using TypographyMuted
- **THEN** the element renders as `<p>` with text-sm and text-muted-foreground

#### Scenario: Special typography styling

- **WHEN** using TypographyBlockquote
- **THEN** the element renders as `<blockquote>` with mt-6, border-l-2, pl-6, italic styling
- **WHEN** using TypographyList
- **THEN** the element renders as `<ul>` with my-6, ml-6, list-disc, and li margin styling
- **WHEN** using TypographyInlineCode
- **THEN** the element renders as `<code>` with bg-muted, rounded, px/py padding, font-mono, text-sm, font-semibold

### Requirement: Typography Demo Examples

The UI kit demo SHALL provide examples for the Typography components in the Data Display category demonstrating headings, body text, blockquotes, lists, and code.

#### Scenario: Typography section in DataDisplayElements

- **WHEN** viewing the Data Display category
- **THEN** a Typography section is displayed with heading and examples
- **AND** the section includes data-element-id="element-typography" for navigation

#### Scenario: Typography examples use translations

- **WHEN** Typography examples are rendered
- **THEN** all text content uses the `tk()` translation helper
- **AND** all translated text is wrapped with TextLoader component

#### Scenario: Typography example content

- **WHEN** viewing the Typography section
- **THEN** a Headings example with H1, H2, H3, H4 is shown
- **AND** a Body text example with P, Large, Small, Muted is shown
- **AND** a Blockquote example is shown
- **AND** a List example with items is shown
- **AND** an Inline Code example is shown

### Requirement: Typography in Category System

The UI kit element registry SHALL include 'Typography' in the `IMPLEMENTED_ELEMENTS` array to mark it as an available component in the Data Display category.

#### Scenario: Category Menu Shows Typography

- **WHEN** viewing the UIKit category menu
- **THEN** Typography appears as an implemented element in Data Display category
- **AND** Typography is positioned alphabetically among other data display elements

### Requirement: Typography Translations

The UI kit translations SHALL provide localized strings for all 36 supported languages with keys including:
- `typography_heading` - Section heading
- `typography_headings_label` - Headings example label
- `typography_body_label` - Body text example label
- `typography_blockquote_label` - Blockquote example label
- `typography_list_label` - List example label
- `typography_code_label` - Code example label

#### Scenario: Translated Typography Labels

- **WHEN** viewing the Typography demo in a non-English language
- **THEN** all Typography labels display in the selected language
- **AND** translations are contextually appropriate for typography terminology
