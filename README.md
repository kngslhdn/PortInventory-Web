# PortInventory Web

Public read-only web presentation of sanitized switch port inventory data exported from LibreNMS.

## Architecture

LibreNMS → Private PortInventory → GitHub Actions → PortInventory-Web → GitHub Pages

The public repository is intended to contain sanitized inventory only.

## Public data

The site displays:

- Switch/device selector
- Port status and administrative status
- Port description and alias
- Link speed
- Interface type
- Search, sorting, and pagination
- Physical switch ports only; LAG, VLAN, and virtual interfaces are excluded

No internal IP addresses are intended to be published.

## Deployment

The site is published through GitHub Pages.

Data is synchronized from the private PortInventory repository by GitHub Actions after inventory changes.

## Security

Do not commit:

- IP addresses
- Credentials
- API keys or tokens
- SNMP communities
- MAC addresses
- Private keys
- Other internal security-sensitive data

Repository: https://github.com/kngslhdn/PortInventory
