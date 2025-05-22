🌐 Portfolio Website - CI/CD on AWS

This is my personal portfolio website hosted on AWS, built using HTML, CSS, and JavaScript, and deployed via a fully automated CI/CD pipeline using GitHub Actions.

🚀 Live Website
👉 [Visit My Portfolio] https://www-adityhede.com/index.html

---

🛠️ Tech Stack

- Frontend: HTML5, CSS3, JavaScript
- Hosting:AWS S3 (static website hosting)
- CDN & HTTPS: AWS CloudFront
- Domain Management:AWS Route 53
- CI/CD:GitHub Actions
- Security: IAM-based access with GitHub Secrets

---

🔁 CI/CD Workflow

Every time I push changes to the `main` branch, GitHub Actions:
1. Uploads all files to my S3 bucket
2. Invalidates CloudFront cache for `.html` pages
3. Automatically updates my live website in minutes

CI/CD File: `.github/workflows/deploy.yml`

```yaml
on:
  push:
    branches: [ main ]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: aws-actions/configure-aws-credentials@v2
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: ${{ secrets.AWS_REGION }}
      - run: aws s3 sync . s3://${{ secrets.S3_BUCKET_NAME }} --delete
      - run: aws cloudfront create-invalidation \
              --distribution-id ${{ secrets.CLOUDFRONT_DISTRIBUTION_ID }} \
              --paths "/*.html"
```

---

🧠 What I Learned

- Configuring S3 buckets for static site hosting
- Setting up HTTPS and CDN via CloudFront
- Using Route 53 for domain routing
- Writing secure IAM policies for CI/CD access
- Automating deployment using GitHub Actions

---
📁 Project Structure

```
.
├── index.html
├── about.html
├── contact.html
├── projects.html
├── style.css
├── book recommendation.jpg
├── aditya.jpg
├── cloud.jpg
├── employee analytics.jpg
├── employee-directory.jpg
├── Resume.pdf
└── .github
    └── workflows
        └── deploy.yml
```

---

📌 Future Improvements

- Auto-version CSS/JS files to avoid cache invalidation
- Add visitor analytics (e.g., Plausible or CloudWatch)
- Improve mobile responsiveness
- 
---

📜 License

This project is open for learning and personal use. If you want to use this structure, please fork the repo and credit it appropriately.

---

🙋‍♂️ Connect With Me

- 🌐 https://www-adityhede.com/index.html
- 💼 [LinkedIn] https://www.linkedin.com/in/aditya-hede-1971211aa/
- 💻 [GitHub] https://github.com/Addy07-byte
