## ADDED Requirements

### Requirement: Command Component

The UI kit SHALL provide Command, CommandDialog, CommandInput, CommandList, CommandEmpty, CommandGroup, CommandItem, CommandShortcut, and CommandSeparator components in the `@hai3/uikit` package for building keyboard-driven command palettes and search interfaces, built on the `cmdk` library.

#### Scenario: Command component is available

- **WHEN** importing Command from `@hai3/uikit`
- **THEN** all Command sub-components are available: Command, CommandDialog, CommandInput, CommandList, CommandEmpty, CommandGroup, CommandItem, CommandShortcut, CommandSeparator
- **AND** components support all standard cmdk props

#### Scenario: Command container

- **WHEN** using Command as a root container
- **THEN** the container displays with flex-col layout and full height/width
- **AND** the container has bg-popover text-popover-foreground styling
- **AND** the container has rounded-md and overflow-hidden
- **AND** the container has data-slot="command" attribute

#### Scenario: CommandDialog component

- **WHEN** using CommandDialog to display command palette in a modal
- **THEN** the dialog renders using the Dialog component
- **AND** the dialog has accessible title and description (sr-only for screen readers)
- **AND** the dialog content has no padding (p-0) and overflow-hidden
- **AND** the embedded Command has enhanced styling for dialog context

#### Scenario: CommandInput component

- **WHEN** using CommandInput for search/filter input
- **THEN** the input is wrapped in a container with search icon
- **AND** the container has border-b and flex layout with items-center
- **AND** the input has transparent background and no outline
- **AND** the input has data-slot="command-input" attribute
- **AND** the wrapper has data-slot="command-input-wrapper" attribute

#### Scenario: CommandList component

- **WHEN** using CommandList to contain command items
- **THEN** the list has max-h-[300px] with overflow-y-auto
- **AND** the list has scroll-py-1 for scroll padding
- **AND** the list has data-slot="command-list" attribute

#### Scenario: CommandEmpty component

- **WHEN** using CommandEmpty for no results state
- **THEN** the empty state displays with py-6 text-center text-sm styling
- **AND** the empty state has data-slot="command-empty" attribute

#### Scenario: CommandGroup component

- **WHEN** using CommandGroup to organize related items
- **THEN** the group has overflow-hidden and p-1 padding
- **AND** group headings have text-muted-foreground, text-xs, font-medium styling
- **AND** the group has data-slot="command-group" attribute

#### Scenario: CommandItem component

- **WHEN** using CommandItem for selectable options
- **THEN** items display with flex layout, gap-2, rounded-sm, and cursor-default
- **AND** selected items have data-[selected=true]:bg-accent styling
- **AND** disabled items have pointer-events-none and opacity-50
- **AND** icons within items have consistent sizing (size-4) and muted color
- **AND** the item has data-slot="command-item" attribute

#### Scenario: CommandShortcut component

- **WHEN** using CommandShortcut to display keyboard shortcuts
- **THEN** shortcuts display with ml-auto, text-xs, tracking-widest
- **AND** shortcuts have text-muted-foreground styling
- **AND** the shortcut has data-slot="command-shortcut" attribute

#### Scenario: CommandSeparator component

- **WHEN** using CommandSeparator between groups
- **THEN** the separator displays as a horizontal line (h-px)
- **AND** the separator has bg-border and -mx-1 negative margin
- **AND** the separator has data-slot="command-separator" attribute

### Requirement: Command Demo Examples

The UI kit demo SHALL provide examples for the Command component in the Actions & Buttons category demonstrating a command dialog with keyboard shortcut trigger, grouped items with icons, and keyboard shortcuts display.

#### Scenario: Command section in ActionElements

- **WHEN** viewing the Actions & Buttons category
- **THEN** a Command section is displayed with heading and examples
- **AND** the section includes data-element-id="element-command" for navigation

#### Scenario: Command examples use translations

- **WHEN** Command examples are rendered
- **THEN** all text content uses the `tk()` translation helper
- **AND** all translated text is wrapped with TextLoader component

#### Scenario: Keyboard shortcut trigger

- **WHEN** viewing the Command example
- **THEN** instructions show "Press ⌘J" to open command palette
- **AND** the keyboard shortcut is displayed in a styled kbd element
- **AND** pressing ⌘J (or Ctrl+J on Windows) toggles the command dialog

#### Scenario: Command dialog content

- **WHEN** the command dialog is open
- **THEN** a search input with placeholder is displayed
- **AND** a "Suggestions" group shows Calendar, Search Emoji, Calculator items with icons
- **AND** a "Settings" group shows Profile, Billing, Settings items with icons and shortcuts
- **AND** groups are separated by CommandSeparator
- **AND** "No results found." displays when search has no matches

### Requirement: Command in Category System

The UI kit element registry SHALL include 'Command' in the `IMPLEMENTED_ELEMENTS` array to mark it as an available component in the Actions & Buttons category.

#### Scenario: Category Menu Shows Command

- **WHEN** viewing the UIKit category menu
- **THEN** Command appears as an implemented element in Actions & Buttons category
- **AND** Command is positioned alphabetically among other action elements

### Requirement: Command Translations

The UI kit translations SHALL provide localized strings for all 36 supported languages with keys including:
- `command_heading` - Section heading
- `command_press` - "Press" instruction text
- `command_placeholder` - Search input placeholder
- `command_no_results` - Empty state message
- `command_suggestions` - Suggestions group heading
- `command_settings` - Settings group heading
- `command_calendar` - Calendar item label
- `command_search_emoji` - Search Emoji item label
- `command_calculator` - Calculator item label
- `command_profile` - Profile item label
- `command_billing` - Billing item label
- `command_settings_item` - Settings item label

#### Scenario: Translated Command Labels

- **WHEN** viewing the Command demo in a non-English language
- **THEN** all Command labels, placeholders, and group headings display in the selected language
- **AND** translations are contextually appropriate for command palette terminology
