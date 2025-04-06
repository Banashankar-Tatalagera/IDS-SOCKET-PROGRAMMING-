
# 🛡 IDS-SOCKET-PROGRAMMING

This is a simple Intrusion Detection System (IDS) built using Python and socket programming, with an interactive Streamlit interface. It detects basic DoS-style attacks like SYN, UDP, and ICMP floods.

---

## 📦 Features

- Real-time detection of:
  - SYN Flood
  - UDP Flood
  - ICMP Ping Flood
  - Excessive request-based DoS
- IP blocking based on request thresholds
- Streamlit-powered GUI for:
  - Server control
  - Traffic simulation (attacks)
  - Live log monitoring

---

## 🧰 Requirements

- Python 3.8+
- Streamlit

Install dependencies:

```bash
pip install streamlit
```

---

## 🚀 Getting Started

### 1. Start the IDS Server

```bash
python ids_server.py
```

This launches a Streamlit UI where you can start/stop the server and view logs.

### 2. Launch the Attack Simulator

```bash
python attack_client.py
```

Use this to simulate different types of traffic from a GUI. It can:
- Send normal traffic
- Simulate SYN, UDP, and ICMP flood attacks at predefined rates

---

## 📡 How It Works

- The server listens on port `9999` for incoming TCP connections.
- Each client message is checked:
  - If it's one of the known flood types, it's flagged.
  - If too many requests come in from the same IP within 5 seconds, it’s temporarily blocked.
- Logs are streamed live in the GUI.

---

## 📁 File Structure

```
.
├── ids_server.py        # Main IDS with Streamlit dashboard
├── attack_client.py     # Traffic generator/attacker UI
└── README.md
```

---

## 🧠 Concepts Covered

- Socket programming
- Threading for concurrent connections
- Basic DoS detection logic
- GUI using Streamlit
- Rate-limiting + IP blocking

---

## ⚠️ Disclaimer

This project is for educational and simulation purposes **only**. Do not use it for unauthorized testing or attacks.

---

## 👨‍💻 Author

Made by [Banashankar Tatalagera](https://github.com/Banashankar-Tatalagera)
