# Symplichain Hackathon — Conceptual Design

---

## 🔹 Part 1: Shared Gateway Problem

### Fairness (Customer Queues)

```python
# Conceptual logic
user_queues = {
    "Customer_A": [req1, req2, req3],
    "Customer_B": [req1],
    "Customer_C": [req1, req2]
}

def process_fairly():
    for customer in active_customers:
        request = pop_request(customer)
        if request:
            send_to_external_api(request)


---
## 🔹 Part 2: Mobile Architecture

### App Architecture

### Tech Stack

- React Native (Frontend)
- Django REST APIs (Backend)
- AWS S3 (File Storage)
- PostgreSQL RDS (Database)
- CloudFront (CDN)
- JWT (Authentication)

---

### Interaction Model

- Large buttons for easy usage (driver-friendly)
- Minimal steps for quick actions
- Swipe-based navigation
- Voice input (optional, AI-based)
- Offline mode with sync when internet is available

---

### Key Features

- Upload Proof of Delivery (POD)
- Real-time delivery status updates
- Push notifications
- Simple and fast UI

---

### Summary

- React Native enables cross-platform development
- Simple UX improves usability for drivers
- Architecture supports scalability and real-time operations   ## 🔹 Part 3: CI/CD Pipeline

### CI/CD Flow

---

### GitHub Actions Trigger

```yaml
name: Deploy to Staging

on:
  push:
    branches:
      - staging

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
## 🔹 Part 4: Debugging Flow

### System Flow

---

### Step-by-Step Debugging

1. **Check Django API**
   - Verify request is received  
   - Check if image upload to S3 is successful  

2. **Check S3 Storage**
   - Confirm image is stored  
   - If not → issue in backend or credentials  

3. **Check Celery Workers**
   - Verify task is triggered  
   - Check for failed or stuck tasks  

4. **Check Bedrock (AI Service)**
   - Look for timeout or API errors  
   - Check logs in CloudWatch  

5. **Check Database (RDS)**
   - Verify data is saved  
   - Check connection issues  

---

### Debugging Commands

```bash
# Check Django logs
tail -n 100 /var/log/gunicorn/error.log

# Search S3-related errors
grep "S3" /var/log/nginx/error.log
