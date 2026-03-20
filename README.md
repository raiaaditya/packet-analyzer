# DPI Packet Analyzer

A high-performance **multi-threaded Deep Packet Inspection (DPI) engine** built in C++ for analyzing and filtering network traffic from PCAP files.

---

## 🚀 Features

* Multi-threaded packet processing
* Application detection (YouTube, Facebook, etc.)
* Blocking support (App, IP, Domain)
* PCAP file parsing and analysis

---

## ⚙️ Build

```bash
g++ -std=c++17 -pthread -I include -o dpi_engine src/dpi_mt.cpp src/pcap_reader.cpp src/packet_parser.cpp src/sni_extractor.cpp src/types.cpp
```

---

## ▶️ Run

```bash
.\dpi_engine.exe test_dpi.pcap output.pcap
```

---

## 🔥 Example (with blocking)

```bash
.\dpi_engine.exe test_dpi.pcap output.pcap --block-app YouTube --block-domain facebook
```

---

## 📊 Output

* Packet statistics
* Application breakdown
* Detected domains (SNI)
* Filtered output PCAP

---

## 🛠️ Tech Stack

* C++
* Multi-threading
* Network packet parsing

---

## 📌 Note

Test data can be generated using:

```bash
python generate_test_pcap.py
```
