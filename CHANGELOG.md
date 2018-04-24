# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [1.10.2] - 2018-04-18

### Fixed
- A bug that prevented using `add_field( $field, 'first' )` when there were no previously added fields in a GroupableField.

## [1.10.1] - 2018-04-17

### Fixed
- A minor bug fix.

## [1.10.0] - 2018-04-17

### Added
- A possibility to define priorities and accepted arguments on the filter functions.

### Fixed
- Set `Field->$conditional_logic` to be an empty array by default as otherwise it causes a warning in GroupableField.php:81.

## [1.9.2] - 2018-04-12

### Fixed
- A pair of minor bugs that could cause PHP warnings.

## [1.9.1] - 2018-04-12

### Fixed
- A bug on Image field that would cause an error on JavaScript.

## [1.9.0] - 2018-04-12

### Added
- `add_fields()` method for Groupable.

### Fixed
- A bug where `hide_label()` would not work inside Flexible Content layouts.

## [1.8.0] - 2018-04-04

### Added
- Support for ACF Gravity Forms plugin.

### Fixed
- Two minor bugs that caused some PHP warnings.

## [1.7.3] - 2018-03-29

### Fixed
- A bug that caused cloned pseudo groups to not clone their subfields properly.

## [1.7.2] - 2018-03-27

### Fixed
- A bug that occurred when checking key uniqueness without WP_DEBUG.

## [1.7.1] - 2018-03-27

### Changed
- Updated class documentation.

## [1.7.0] - 2018-03-27

### Added
- PseudoGroup field type with which you can treat multiple fields like a group but they appear in the admin as independent.

### Fixed
- A bug that caused cloned fields lose their hidden label status.
- A bug that caused Link field to be unusable.

## [1.6.0] - 2018-03-19

### Added
- Support for Button group field type.
- Support for Accordion field type.
- Support for `Return format` setting for User field type.

### Changed
- Enhanced documentation and corrected a few typos.

## [1.5.5] - 2018-03-16

### Fixed
- A bug that caused fields to occur multiple times in a tab inside an options page.

## [1.5.4] - 2018-03-06

### Fixed
- A bug that prevented removing fields from tab afterwards

## [1.5.3] - 2018-02-26

### Fixed
- A bug in post type filtering within the PostObject field.
- A bug in cloning a groupable field with conditional logic in it.
- A bug with the key uniqueness check that would throw a warning if `WP_DEBUG` was not set `true`.

## [1.5.2] - 2018-02-23

### Fixed
- A bug with remove_field() function.

## [1.5.1] - 2018-02-22

### Fixed
- A bug where cloning a Flexible Content layout would not update the references to it in all places.

## [1.5.0] - 2018-02-21

### Added
- A possibility to filter Flexible Content layouts by field name.

### Fixed
- A few minor bug fixes on various things.

### Changed
- Removed array_unique check from FlexibleContent class because it doesn't work.

## [1.4.0] - 2018-02-13

### Added
- A possibility to filter Flexible Content layouts by post types and page templates.
- Key prefixing for tabs to eliminate the possibility of collisions.

## [1.3.3] - 2018-02-09

### Changed
- Updated the class documentation.

## [1.3.2] - 2018-02-07

### Changed
- Fixed a bug in a function `add_field_location()` which is used by the functions `add_field_before()` and `add_field_after()`.

## [1.3.1] - 2018-02-07

### Changed
- Enhanced the checking of non-unique field keys.

## [1.3.0] - 2018-02-06

### Added
- A support for installing the Codifier as an ordinary plugin instead of autoloaded mu-plugin.
- A check that non-unique field keys throw a notice, and debug information if WP_DEBUG is set.

### Changed
- Enhanced the documentation to reflect the above-mentioned changes.

## [1.2.4] - 2018-01-31

### Fixed
- Fixed a bug that occured after the change made in 1.2.3.

## [1.2.3] - 2018-01-30

### Changed
- Clone field now throws an exception if a conditional logic is tried to be applied to it.

## [1.2.2] - 2018-01-29

### Fixed
- A bug in Groupable class' `remove_field()` method.

## [1.2.1] - 2018-01-23

### Fixed
- A bug that threw a warning if a File field was used without setting allowed MIME types.

## [1.2.0] - 2018-01-18

### Added
- Support for ACF Medium Editor plugin.

### Changed
- Remove_field now uses key instead of the index number.

### Fixed
- A bug where setting allowed mime types for a file field would cause the field not to work.

## [1.1.4] - 2018-01-16

### Fixed
- Fixed the CSS on the `hide_label()` method to prevent affecting child elements.

## [1.1.3] - 2017-11-27

### Changed
- Another small bug fix regarding Group field

## [1.1.2] - 2017-11-27

### Changed
- Fixed a bug regarding Group field type that prevented them from working properly

## [1.1.1] - 2017-11-27

### Changed
- Enhanced documentation with more comprehensive namespace examples

## [1.1.0] - 2017-11-22

### Added
- Lots of ACF filter functionality to be used easily when defining the fields.

## [1.0.0] - 2017-11-22

### Changed
- Fixed a bug that Repeater and Flexible Content fields wouldn't accept key and name as their constructor parameters
- Updated version number to 1.0.0 for compatibility purposes

## [0.2.1] - 2017-11-21

### Changed
- Fixed a bug with the fields' clone method

## [0.2.0] - 2017-11-20

### Added
- Added a possibility to hide a field label easily on the admin side

## [0.1.0] - 2017-11-17

### Changed
- Published a stable release

## [0.0.3-beta] - 2017-11-16

### Changed
- Fixed a bug where field instructions were not shown if instructions placement property wasn't set

## [0.0.2-beta] - 2017-11-07

### Changed
- Enhanced documentation

## [0.0.1-alpha] - 2017-10-31

### Added
- Message, link & color fields
- Datepicker, timepicker & google map fields
- Changelog file
- Added an extra value choice to select, checkbox & radio add_choice function
- Docs generator

### Changed
- Renamed various files to match the psr-4 autoload standard so the autoloading can actually work
- Changed some namespaces & extends paths so they work as well
- Made ConditionalLogicGroup add_rule $value accept others than booleans as this can be used on select fields as well
