# CA Onboarding - OnboardCA Project

Hey there! Welcome to my **CA Onboarding** project! This is a full-stack application I built for **LinkBuddy** using **Spring Boot**. It has a form where new joinees can enter their name and email, and they get a welcome email with a **UTM link**. The app tracks clicks on the UTM link and shows the data in a **performance dashboard**. I deployed it on **Render** with a **PostgreSQL** database.

---

## 🚀 Project Overview

### 🔗 **GitHub Repo:**  
[https://github.com/thesonuchauhan/OnboardCA.git](https://github.com/thesonuchauhan/OnboardCA.git)

---

## 🛠️ Tech Stack
- **Backend:** Spring Boot (Java)
- **Frontend:** HTML, CSS, Bootstrap, JavaScript
- **Database:** PostgreSQL
- **Email Service:** Gmail (SMTP)
- **Deployment:** Render (Free Tier)

---

## ✨ Features
- New Joinee Form: Enter your name and email, then submit.
- Welcome Email: Automatically sends an email with a UTM link.
- UTM Link Tracking: Tracks clicks on the UTM link.
- Performance Dashboard: Displays ambassadors’ data (name, email, UTM link, and clicks).
- Dark Mode: Toggle between light and dark themes.

---

## 🏃 How to Run Locally

### 1. **Clone the Repo**
```bash
git clone https://github.com/thesonuchauhan/OnboardCA.git
cd OnboardCA
2. Set Up PostgreSQL
Install PostgreSQL (Windows/Linux/Mac).

Create a database:

sql
Copy
Edit
CREATE DATABASE linkbuddy;
Update src/main/resources/application.properties:

properties
Copy
Edit
spring.datasource.url=jdbc:postgresql://localhost:5432/linkbuddy
spring.datasource.username=postgres
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update

spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_gmail@gmail.com
spring.mail.password=your_gmail_app_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

app.base-url=http://localhost:8080
3. Generate Gmail App Password
Enable 2-Step Verification on your Gmail account.

Go to Google Account → Security → App Passwords, generate a new password.

Use that in application.properties for email sending.

4. Run the App
Build and run using Maven:

bash
Copy
Edit
mvn clean package
java -jar target/ca-onboarding-0.0.1-SNAPSHOT.jar
Or directly run from IntelliJ IDEA.

5. Access the App
Open your browser at:
http://localhost:8080/

Fill the form, check your email, and view the dashboard.

🌍 Deployment on Render
✅ Steps:
GitHub Repo:
https://github.com/thesonuchauhan/OnboardCA.git

Render Setup:

Signed up on Render with GitHub.

Created a new Web Service linked to the repo.

Added environment variables:

env
Copy
Edit
SPRING_DATASOURCE_URL=jdbc:postgresql://dpg-d0pqu5re5dus73e461g0-a.singapore-postgres.render.com:5432/linkbuddy
SPRING_DATASOURCE_USERNAME=linkbuddy_user
SPRING_DATASOURCE_PASSWORD=Nyuo2MNhtWzC1xIo09VllRYHUvLrojC6
SPRING_MAIL_HOST=smtp.gmail.com
SPRING_MAIL_PORT=587
SPRING_MAIL_USERNAME=your_gmail@gmail.com
SPRING_MAIL_PASSWORD=your_gmail_app_password
SPRING_MAIL_PROPERTIES_MAIL_SMTP_AUTH=true
SPRING_MAIL_PROPERTIES_MAIL_SMTP_STARTTLS_ENABLE=true
APP_BASE_URL=https://ca-onboarding-xyz123.onrender.com
Set up PostgreSQL on Render (free tier).

Render built and deployed the app using the Dockerfile.

🔗 Live URL:
https://ca-onboarding-xyz123.onrender.com/

🔎 Testing
✅ Filled the form at the deployed URL.

✅ Received the welcome email with UTM link.

✅ Tested the UTM link; it redirects to www.industryacademiacommunity.com.

✅ Viewed the dashboard to check data (name, email, UTM link, clicks).

✅ Verified the PostgreSQL database using pgAdmin 4.

⚙️ Challenges Faced
Initially used H2 database but switched to PostgreSQL for deployment.

Dockerfile issue: maven:3.8.6-openjdk-17 was not found, fixed by using maven:3.8.7-eclipse-temurin-17.

Faced psql command errors, managed using pgAdmin 4.

🚀 Future Improvements
🔐 Add login/authentication for dashboard.

🔍 Add filters and search in the dashboard.

✉️ Improve the design of welcome emails.

📜 License
This project is for educational and demo purposes only.

yaml
Copy
Edit

---

## ✅ Next Step:
Save this as `README.md` in your project folder and push it to your GitHub repo.

If you'd like, I can generate this as a downloadable file for you. Want that? 😊
