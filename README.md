# Repository Structure

```text
dns-project/
│
├── README.md
├── screenshots/
│   ├── github-pages-settings.png
│   ├── route53-records.png
│   ├── nginx-working.png
│   └── final-domain-output.png
│
├── site/
│   ├── index.html
│   └── assets/
│
└── docs/
    └── dns-setup-notes.md
```

---

# README.md

# Basic DNS Setup

## Project Objective

This project demonstrates how to configure a custom domain and set up DNS records for:

* GitHub Pages
* AWS Route 53
* Nginx hosted static website

The objective was to understand how DNS connects a domain name to web hosting services.

---

## Technologies Used

* AWS Route 53
* Nginx
* GitHub Pages
* Git
* Linux (Ubuntu)

---

## Task 1 – Custom Domain for GitHub Pages

### Steps Performed

1. Created and configured a GitHub Pages website.
2. Opened repository settings and enabled Pages deployment.
3. Added custom domain in GitHub Pages settings.
4. Configured DNS records in AWS Route 53.
5. Waited for DNS propagation and verified successful access.

### DNS Records Used

#### Root Domain (A Records)

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

#### WWW Record

```text
Type: CNAME
Value: username.github.io
```

---

## Task 2 – Custom Domain for Nginx Static Site

### Steps Performed

1. Hosted a static website using Nginx.
2. Updated Nginx configuration.
3. Configured domain records in Route 53.
4. Pointed the domain to server public IP.
5. Restarted Nginx and validated deployment.

### Nginx Commands

```bash
sudo systemctl restart nginx
sudo systemctl status nginx
```

### Example Server Configuration

```nginx
server_name yourdomain.com www.yourdomain.com;
```

---

## Verification

Validation completed by:

* Opening the custom domain in browser
* Confirming DNS resolution
* Confirming static site delivery through Nginx

---

## Screenshots

Add screenshots in the `/screenshots` folder:

* Route 53 DNS records
* GitHub Pages configuration
* Nginx running output
* Final website output

---

## Conclusion

This project helped in understanding:

* DNS fundamentals
* Domain configuration
* Route 53 record management
* Custom domain integration
* Static website hosting using Nginx
* GitHub Pages deployment
