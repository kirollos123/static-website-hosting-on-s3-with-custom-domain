# static-website-hosting-on-s3-with-custom-domain
# Static Website Hosting on S3 with Custom Domain (Free Setup)

This project demonstrates how to host a static website on **Amazon S3** and connect it to a **custom domain (from Freenom)** using **Cloudflare DNS** for a fully functional, cost-free deployment.

---

## 🌐 Tech Stack

- **Amazon S3** – Static website hosting
- **Freenom** – Free domain (.tk, .ml, etc.)
- **Cloudflare** – DNS configuration and SSL

---

## 📌 Architecture Diagram

![Architecture](docs/architecture-diagram.png)

---

## 🚀 Steps to Deploy

### 1. Upload Static Files to S3
- Create a bucket with the same name as your domain (e.g., `example.tk`)
- Enable "Static Website Hosting"
- Upload `index.html` and `error.html`

### 2. Get a Free Domain
- Go to [https://www.freenom.com](https://www.freenom.com)
- Register a domain like `example.tk`

### 3. Use Cloudflare for DNS
- Add your domain to [Cloudflare](https://cloudflare.com)
- Change Freenom Nameservers to Cloudflare’s
- In Cloudflare DNS, add:
  - Type: CNAME  
  - Name: `www`  
  - Target: `example.tk.s3-website-region.amazonaws.com`

### 4. Enable HTTPS (Optional)
- Use **Cloudflare's SSL Full mode** to secure your site for free

---

## 📸 Screenshots

| S3 Hosting Setup | Freenom Domain | Cloudflare DNS |
|------------------|----------------|----------------|
| ![](screenshots/s3-hosting-setup.png) | ![](screenshots/freenom-domain.png) | ![](screenshots/cloudflare-dns-setup.png) |

---

## 📁 Folder Structure

```bash
website/
│   ├── index.html
│   └── error.html
