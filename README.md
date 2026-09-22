# lockwright-utils-date

A collection of date utility functions for formatting and comparing dates.

Site: [lockwright.dexterity.works](https://lockwright.dexterity.works)

Community fork of PearPass (Apache 2.0). Not affiliated with or endorsed by Tether Data or the Pears project.

## Table of Contents
- [Features](#features)
- [Security Notice](#security-notice)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
  - [Format Dates](#format-dates)
  - [Compare Dates](#compare-dates)
- [Dependencies](#dependencies)
- [Related Projects](#related-projects)

## Features

- Format dates with customizable patterns using `formatDate`
- Compare dates with `isAfter` to check if one date is later than another
- Compare dates with `isBefore` to check if one date is earlier than another
- Support for both Date objects and string date inputs
- Customizable date separators
- Month and weekday abbreviations

## Security Notice

The package name is `lockwright-utils-date`.

## Installation

```bash
npm install git+https://github.com/Dexterity-Works/lockwright-utils-date.git
```

## Usage

Import the functions you need:

```javascript
import { formatDate, isAfter, isBefore } from 'lockwright-utils-date';
```

## Examples

### Format Dates

```javascript
// Basic formatting (default: yyyy-mm-dd)
formatDate(new Date('2023-05-15'));
// Output: '2023-05-15'

// Custom format
formatDate(new Date('2023-05-15'), 'dd-mm-yyyy');
// Output: '15-05-2023'

// Custom separator
formatDate(new Date('2023-05-15'), 'yyyy-mm-dd', '/');
// Output: '2023/05/15'

// With month abbreviation
formatDate(new Date('2023-05-15'), 'dd-mmm-yyyy');
// Output: '15-May-2023'

// With weekday abbreviation
formatDate(new Date('2023-05-15'), 'ddd-mm-dd');
// Output: 'Mon-05-15'
```

### Compare Dates

```javascript
// Check if a date is after another
isAfter('2023-01-02', '2023-01-01');
// Output: true

// Check if a date is before another
isBefore('2023-01-01', '2023-01-02');
// Output: true
```

## Dependencies

This package has no runtime dependencies.

## Related Projects

- [lockwright-app-mobile](https://github.com/Dexterity-Works/lockwright-app-mobile) - Lockwright for mobile
- [lockwright-app-desktop](https://github.com/Dexterity-Works/lockwright-app-desktop) - Lockwright for desktop
- [tether-dev-docs](https://github.com/Dexterity-Works/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.