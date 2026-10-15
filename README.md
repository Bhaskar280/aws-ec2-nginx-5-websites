# AWS EC2 – Hosting 5 Websites Using Nginx

## Project Overview
This project demonstrates how to host five static HTML websites on a single AWS EC2 Ubuntu instance using Nginx server blocks and different TCP ports.

## Technologies Used
- AWS EC2
- Ubuntu Linux
- Nginx
- HTML
- AWS Security Groups
- Git and GitHub

## Architecture
Internet → AWS Security Group → EC2 Ubuntu → Nginx → Five websites

## Website Configuration
| Website | Port | Directory |
|---|---|---|
| Website 1 | 80 | `/var/www/site1` |
| Website 2 | 8080 | `/var/www/site2` |
| Website 3 | 8081 | `/var/www/site3` |
| Website 4 | 9090 | `/var/www/site4` |
| Website 5 | 9091 | `/var/www/site5` |

## Implementation
1. Launched an Ubuntu EC2 instance.
2. Connected securely using SSH.
3. Installed and enabled Nginx.
4. Created five HTML websites under `/var/www/`.
5. Configured five Nginx server blocks.
6. Validated the configuration with `sudo nginx -t`.
7. Configured Security Group inbound rules.
8. Tested all five websites using the EC2 public IP and their respective ports.

## Validation
- Nginx configuration test passed.
- Verified Nginx listening ports using `sudo ss -tlnp | grep nginx`.
- Confirmed all five websites loaded successfully in a browser.

## Key Learnings
- Hosting multiple websites on one EC2 instance
- Nginx server blocks and port-based routing
- Linux server administration
- AWS Security Group configuration
- Troubleshooting network connectivity

## Security Notes
This is a learning project using HTTP. Production deployments should use HTTPS, restricted access, and appropriate availability and monitoring controls.

## Author
Bhaskar Reddy Kankanala
