# scm-gx-ecommerce-notification-service
Notification service for all the microservices send notification via this service only 

# 📧 Notification Service

This is a Spring Boot microservice responsible for sending **email notifications** within the SCM GX Ecommerce system.

---

## 🚀 Features

- Send transactional emails
- Templated email support (e.g., HTML emails)
- Easy integration with other microservices
- Configurable SMTP server via `application.yml`

---

## 🛠️ Tech Stack

- Java 17+
- Spring Boot
- Spring Mail
- Maven
- (Optional) Thymeleaf or FreeMarker for email templates

---

## 📬 How It Works

1. The service exposes REST endpoints to receive notification requests.
2. It constructs an email message (plain or HTML).
3. Sends the email using the configured SMTP server.

---

## 📦 API Example

### `POST /api/notifications/email`

```json
{
  "to": "user@example.com",
  "subject": "Welcome to SCM GX!",
  "body": "<h1>Thanks for signing up!</h1>",
  "isHtml": true
}

