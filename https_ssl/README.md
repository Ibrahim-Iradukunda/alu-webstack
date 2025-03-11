# HTTPS and SSL Project

## Background Context
Securing website traffic is essential to protect data integrity, confidentiality, and authenticity. Without HTTPS, websites are vulnerable to attacks such as man-in-the-middle attacks, data interception, and loss of user trust.

## Learning Objectives
At the end of this project, you should be able to explain:
- The two main roles of HTTPS and SSL.
- The purpose of encrypting traffic.
- The meaning of SSL termination.

## Requirements
- Use editors: `vi`, `vim`, or `emacs`.
- All files will be interpreted on Ubuntu 16.04 LTS.
- Each file should end with a new line.
- The root of the project folder must contain a `README.md` file.
- All Bash script files must be executable.
- Bash scripts must pass `Shellcheck` (version 0.3.7) without errors.
- The first line of all Bash scripts should be `#!/usr/bin/env bash`.
- The second line of all Bash scripts should describe the script's purpose.

## Tasks
### 0. World Wide Web
- Configure your domain zone to add subdomains:
  - `www` pointing to `lb-01`.
  - `lb-01` pointing to `lb-01`.
  - `web-01` pointing to `web-01`.
  - `web-02` pointing to `web-02`.
- Create a Bash script to display subdomain information.
- The script must:
  - Accept `domain` (mandatory) and `subdomain` (optional) as arguments.
  - Output: `The subdomain [SUB_DOMAIN] is a [RECORD_TYPE] record and points to [DESTINATION]`.
  - Use `awk` and at least one Bash function.

### 1. HAProxy SSL Termination
- Configure HAProxy to handle SSL termination:
  - HAProxy must listen on TCP port 443.
  - Accept and decrypt SSL traffic.
  - Serve encrypted traffic returning `/` of the web server.
  - The page must contain "Holberton School".
- Submit the HAProxy config file as `1-haproxy_ssl_termination`.

### 2. No Loophole in Your Website Traffic
- Configure HAProxy to redirect HTTP traffic to HTTPS:
  - Return a `301 Moved Permanently` status.
  - Redirect HTTP traffic to HTTPS.
- Submit the HAProxy config file as `2-redirect_http_to_https`.

## Resources
- What is HTTPS?
- Two main elements that SSL provides.
- HAProxy SSL termination on Ubuntu 16.04.
- SSL termination.
- Bash functions.

## Useful Commands
- `awk` – Process and extract text.
- `dig` – Query DNS records.

This project ensures that web traffic is secure, enhances data confidentiality, and protects users from cyber threats.


