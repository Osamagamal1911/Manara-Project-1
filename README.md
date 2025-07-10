# Manara-Project-1
# 🌐 Highly Available Web App on AWS

This project shows how to launch a simple web application on AWS that automatically scales and stays online even if some servers go down. It’s a real-world example of building for **availability**, **scalability**, and **monitoring**, all using AWS services.

---

## 🧰 What It Includes

- **EC2 Instances** to host the app (a small website that shows which server you're hitting).
- **Application Load Balancer (ALB)** to spread traffic between servers.
- **Auto Scaling Group (ASG)** to add/remove servers based on demand.
- **CloudWatch & SNS** to monitor performance and send email alerts.
- **IAM Roles** for secure access.
- **Fully automated** using one CloudFormation file.

---

## 👨‍💻 What the App Does

Each EC2 server runs a tiny web app that simply tells you:

```
Served from EC2 Instance: i-xxxxxxxxxxxx
```

When you visit the site (via the Load Balancer), try refreshing a few times — you’ll see the instance ID change. That means your traffic is being **load balanced** across multiple servers.

---

## 🚀 How to Launch It

1. **Get the Code**
   ```bash
   git clone https://github.com/Osamagamal1911/Manara-Project-1.git
   cd Manara-Project-1
   ```

2. **Deploy Using CloudFormation**
   - Go to the AWS Console → CloudFormation
   - Click **Create Stack**
   - Upload the file: `manara-project1.yaml`
   - Enter your **EC2 KeyPair name** when asked
   - Launch the stack (takes ~5–10 minutes)

3. **Visit the Web App**
   - Go to the **Outputs** tab of the CloudFormation stack
   - Click on the `LoadBalancerDNS` value
   - You’ll see the web app in action!

---

## 🔔 Email Alerts

This setup includes automatic email alerts using **SNS**.

You’ll get notified if:
- CPU usage is too high (servers scale up)
- CPU usage drops (servers scale down)

📩 Make sure to check your inbox and **confirm the subscription** when AWS emails you.

---

## 💡 Good to Know

- The EC2 instances are **t2.micro** (free-tier eligible).
- It uses the **latest Amazon Linux 2 image** (automatically).
- The servers update themselves and run Apache with a simple HTML page.
- The Load Balancer and Auto Scaling keep your site up and responsive.

---

## ✅ Why This Matters

This setup gives you a strong foundation for running **real web apps in production**, with:

- Zero downtime scaling  
- Email alerts on usage  
- Easy maintenance  
- Clean separation of concerns

---

## 📁 Files Included

| File                        | Description                                   |
|-----------------------------|-----------------------------------------------|
| `manara-project1.yaml` | The full setup — deploys everything automatically |
| `README.md`                | This file you're reading now                  |

---

