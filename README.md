
* ✅ GitHub Pages hosting
* ✅ No custom domain
* ✅ AWS experience preserved (as previous architecture)
* ✅ Cost-aware engineering decision
* ✅ Professional tone

You can copy-paste this directly into your repo.

---

# 🌐 Portfolio Website – Static Site with Automated Deployment

This repository contains my personal portfolio website built using HTML, CSS, and JavaScript.

The site is currently deployed using **GitHub Pages** with automated deployment via **GitHub Actions**.

🚀 **Live Website**
👉 [https://addy07-byte.github.io/portfolio-website/](https://addy07-byte.github.io/portfolio-website/)

---

## 🛠️ Tech Stack

**Frontend**

* HTML5
* CSS3
* JavaScript

**Hosting**

* GitHub Pages

**CI/CD**

* GitHub Actions (auto-deploy on push to `main` branch)

---

## 🔁 Deployment Workflow

Every time I push changes to the `main` branch:

1. GitHub triggers a workflow
2. The repository is built and deployed automatically
3. The live website updates within minutes

Deployment configuration:

```
.github/workflows/deploy.yml
```

This ensures continuous integration and deployment without manual uploads.

---

## 🧠 Architecture Evolution

This portfolio was originally deployed on AWS using:

* Amazon S3 (static hosting)
* Amazon CloudFront (CDN + HTTPS)
* Amazon Route 53 (DNS management)
* IAM-secured GitHub Actions pipeline
* Automated CloudFront cache invalidation

It was later migrated to GitHub Pages to optimize infrastructure costs while maintaining automated deployment.

This reflects a cost-aware design decision for a purely static website.

---

## 📁 Project Structure

```
.
├── index.html
├── about.html
├── contact.html
├── projects.html
├── style.css
├── Resume.pdf
└── .github/
    └── workflows/
        └── deploy.yml
```

---

## 📌 Key Learnings

* Static site architecture design
* CI/CD implementation using GitHub Actions
* Secure secret management with GitHub Secrets
* Cloud cost optimization decisions
* Migration planning between hosting providers

---

## 📌 Future Improvements

* CSS/JS versioning for improved cache control
* Performance optimization (Lighthouse improvements)
* Accessibility enhancements
* Lightweight analytics integration

---

## 📜 License

Open for learning and reference. Please fork and credit if you reuse the structure.

---

## 🙋‍♂️ Connect With Me

🌐 Live Site:
[https://addy07-byte.github.io/portfolio-website/](https://addy07-byte.github.io/portfolio-website/)

💼 LinkedIn:
[https://www.linkedin.com/in/aditya-hede-1971211aa/](https://www.linkedin.com/in/aditya-hede-1971211aa/)

💻 GitHub:
[https://github.com/Addy07-byte](https://github.com/Addy07-byte)

---
