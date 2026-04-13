# 1. MQTT vs AMQP

| Feature | MQTT | AMQP |
|--------|------|------|
| **Power Usage** | Very low, lightweight headers, minimal bandwidth, ideal for IoT devices | High, heavy protocol, more data overhead, not suitable for low-power devices |
| **Security** | Supports TLS/SSL, username/password, but depends on broker configuration | Enterprise-grade security, built-in authentication, authorization, TLS |
| **Message Persistence** | Strong. QoS levels (0,1,2), retained messages, handles unstable connections well | Very strong. Message queues, acknowledgments, guaranteed delivery mechanisms |

---

# 2. MQTT vs HTTP/HTTPS

| Feature | MQTT | HTTP / HTTPS |
|--------|------|-------|
| **Power Usage** | Very low, persistent connection, small packets | Higher, repeated request/response cycles, large headers, connection overhead |
| **Security** | Supports TLS/SSL, username/password, but depends on broker configuration, but less standardized than HTTPS | HTTPS is widely adopted, supports OAuth, API keys, mature ecosystem |
| **Message Persistence** | Strong. QoS ensures delivery even with connection loss |  No built-in persistence, requires manual retry logic |
