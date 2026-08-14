> [!WARNING]
> 🍐 PearPass is currently paused from active development, so please use at your own caution until further notice.

# pear-apps-utils-date

A collection of date utility functions for formatting and comparing dates.

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

1. To ensure the security and integrity of your projects, please note that official PearPass packages are distributed exclusively through our GitHub organization.
2. Any packages with similar names found on the npm registry or other third-party package managers are not affiliated with PearPass and should be strictly avoided. We recommend installing directly from this repository to ensure you are using the verified, open-source version.

## Installation

```bash
npm install git+https://github.com/tetherto/pear-apps-utils-date.git
```

## Usage

Import the functions you need:

```javascript
import { formatDate, isAfter, isBefore } from '@tetherto/pear-apps-utils-date';
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

- [@tetherto/pearpass-app-mobile](https://github.com/tetherto/pearpass-app-mobile) - A mobile app for PearPass, a password manager
- [@tetherto/pearpass-app-desktop](https://github.com/tetherto/pearpass-app-desktop) - A desktop app for PearPass, a password
- [@tetherto/tether-dev-docs](https://github.com/tetherto/tether-dev-docs) - Documentations and guides for developers

## License

This project is licensed under the Apache License, Version 2.0. See the [LICENSE](./LICENSE) file for details.