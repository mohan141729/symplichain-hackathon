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
