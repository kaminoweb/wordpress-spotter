# WordPress Spotter

**WordPress Spotter** is a collection of bash scripts to detect if a website is powered by WordPress. It uses various methods, including scanning for WordPress-specific files, directories, headers, cookies, and REST API endpoints. This tool helps automate the detection of WordPress sites by performing multiple checks and ensuring comprehensive results.

## Features

- **Check for common WordPress directories**: Detects if the website has `/wp-content/` or `/wp-includes/` in its structure.
- **Check meta tags**: Looks for the WordPress generator meta tag in the HTML.
- **Check HTTP headers**: Scans for WordPress-specific HTTP headers such as `X-Powered-By`.
- **Check for WordPress login page**: Detects the existence of `/wp-login.php`.
- **Check WordPress REST API**: Verifies if the site responds to WordPress REST API endpoints like `/wp-json/`.
- **Check for WordPress cookies**: Identifies WordPress-specific cookies such as `wordpress_logged_in_`.
- **Check for common files**: Scans for `license.txt`, `readme.html`, `xmlrpc.php`, and themes to identify WordPress installations.
- **Comprehensive URL validation**: Ensures the URL is properly formatted before running tests.

## Prerequisites

Make sure you have the following installed on your system:

- **bash**: Most Linux/Unix systems have Bash preinstalled.
- **curl**: Used to make HTTP requests.
- **grep**: Used for text searching within files and responses (usually preinstalled).

## Installation

Clone the repository to your local machine and navigate to the project directory. 

```bash
git clone https://github.com/yourusername/wordpress-spotter.git
cd wordpress-spotter
```

Make sure the scripts are executable.

```bash
chmod +x *.bsh
```

## Usage

Run any of the detection scripts by passing a URL as an argument. For example, to check the WordPress REST API.

```bash
./check-wp-api.sh https://example.com
```

You can also run the combined detection script to perform multiple checks at once.

```bash
./check-wp-api.sh https://example.com
```

## Example Output

```bash
./check-wp-api.sh https://example.com
URL is properly formatted.
WordPress detected via REST API.
```

### Available Scripts

| Script Name             | Description |
| ----------------------- | ----------- |
| `check-wp-directories.bsh`    | Checks for common WordPress directories (`/wp-content/`, `/wp-includes/`). |
| `check-wp-meta.bsh`       | Detects if a WordPress meta tag is present. |
| `check-wp-header.bsh`     | Scans HTTP headers for WordPress-related information. |
| `check-wp-loginpage.bsh` | Verifies the existence of the WordPress login page (`/wp-login.php`). |
| `check-wp-api.bsh`        | Checks if the website responds to WordPress REST API requests. |
| `check-wp-api2.bsh`        | Checks if the website responds to WordPress REST API v2 requests. |
| `check-wp-cookies.bsh`    | Detects WordPress-specific cookies such as `wordpress_logged_in_`. |
| `check-wp-license.bsh`    | Checks for the existence of `license.txt` in the root directory. |
| `check-wp-readme.bsh`     | Detects `readme.html` to identify WordPress. |
| `check-wp-theme.bsh`      | Checks for common WordPress themes like `twentytwentyone`. |
| `check-wp-xmlrpc.bsh`     | Checks for the presence of the `xmlrpc.php` file. |
| `check-wp-graphql.bsh`   | Test if the website responds to the WordPress GraphQL API. |
| `check-wp-pingback.bsh`   | Scans for WordPress `X-Pingback` header. |

## URL Validation

The scripts include a URL validation function to ensure that the URL passed as an argument is correctly formatted (i.e., starting with `http://` or `https://`). If the URL is not properly formatted, the script will output an error and stop execution.

## Contributing

Feel free to fork the repository and submit pull requests if you have improvements or additional detection methods to contribute.

### Steps to Contribute

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Commit your changes and push to your fork.
5. Submit a pull request.

## License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for details.

