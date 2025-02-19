![Mini Shell PHP Script Overview](https://i.imgur.com/PyKET5A.png "Mini Shell PHP Script Overview")

## What is Web Shell Detector?

Web Shell Detector is a PHP script developed to detect PHP, CGI (Perl), ASP/ASPX shells. It uses a signature-based database to identify these threats with up to 99% accuracy. It features a modern, user-friendly interface leveraging contemporary technologies.

## Usage
To activate Web Shell Detector:

1. Upload `shelldetect.php` and `shelldetect.db` to your root directory.
2. Open `shelldetect.php` in your browser (e.g., `http://www.website.com/shelldetect.php`).
3. Log in with the default username & password:
   - Username: `admin`
   - Password: `protect`
4. Inspect suspicious files. If any files seem suspicious, submit them to [Shell Detector Team](http://www.shelldetector.com). The file will be inspected, and if threats are found, they will be added to the web shell signature database.
5. If web shells are detected, use your FTP/SSH client to remove them from your server (IMPORTANT: Be cautious, as some shells may be integrated into system files).

## Demo
[Web Shell Detector Demo](http://www.emposha.com/demo/shelldetect/)

## Options
- `extension`: File extensions to scan
- `showlinenumbers`: Show line numbers for suspicious functions
- `dateformat`: Used for access and modification times
- `language`: Set the language
- `directory`: Scan a specific directory
- `task`: Perform different tasks
- `report_format`: Use with `is_cron(true)` to define report file format
- `is_cron`: If true, run as cron (no output)
- `filelimit`: Maximum files to scan (for more than 30,000 files, scan specific directories)
- `useget`: Enable `_GET` variable for task submission
- `authentication`: Protect the script with user & password (set to NULL to disable)
- `remotefingerprint`: Get shell signatures remotely


## Features

- **extension**: Specify file extensions to scan.
- **showlinenumbers**: Display line numbers for suspicious functions.
- **dateformat**: Set the date format.
- **language**: Language support.
- **directory**: Scan specific directories.
- **report_format**: Choose the report format.

## Updates

Web Shell Detector is a regularly updated tool with new shell types added and existing features improved.

## Security Tips

- Run the Web Shell Detector periodically to keep your site secure.
- Carefully inspect suspicious files and regularly check log files.



## Detection
- Number of known shells: 604

## Requirements
- PHP 5.x
- OpenSSL (for secure file submission)


## Changelog
- **1.66**: Small tweaks and PHP 5.3.3 support (thanks to John Thornton)
- **1.64**: Added INI file support, output method rewritten, Italian translation (thanks to Marco Saiu)
- **1.63**: New shell recognition mechanism, updated shell signatures
- **1.62**: jQuery version reverted to 1.7.x due to bug with jQuery UI dialog, new file types added, updated shell signatures
- **1.61**: New way to submit suspicious files, CSS & code fixes, updated shell signatures
- **1.6**: Added support to indicate non-shell files, loader indicator added
- **1.52**: Noindex meta tag added, scan all files option added (`extension = *`)
- **1.51**: Unpack function update
- **1.5**: Unpack function added, application version check, fixed warnings and error handler
- **1.4**: Hide suspicious files option, file scanning changed
- **1.3**: File submission changes, email field added for notifications
- **1.2**: Encryption function and authentication added, small bug fixes
- **1.1**: Fingerprint function change, show line regex updated
- **1.0**: Initial version
