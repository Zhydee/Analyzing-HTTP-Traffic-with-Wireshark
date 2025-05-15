# 🕵️‍♂️ Analyzing HTTP Traffic with Wireshark

## 📝 Introduction

In this project, you'll use **Wireshark** to capture and analyze **HTTP traffic**. This is essential for:
- Understanding how web communications work
- Spotting potential security issues
- Investigating anomalies in network traffic

---

## 🧠 Pre-requisites

- Basic understanding of networking concepts
- Wireshark installed: [https://www.wireshark.org/download.html](https://www.wireshark.org/download.html)
- Any modern web browser (Chrome, Firefox, etc.)

---

## 🔧 Lab Setup & Tools

- **Wireshark**
- **Web Browser**

---

## 🧪 Exercises

---

### 🔍 Exercise 1: Capture HTTP Traffic

**Step-by-Step Instructions:**
1. Open Wireshark.
2. Select the network interface that connects to the internet.
3. Click on the **"Start Capture"** button (blue shark fin).
4. Open your browser and go to: [http://example.com](http://example.com)
5. Let the page load completely.
6. Stop the capture by clicking the **red square** icon.

**📸 Screenshot Example:**
![Step 1 - HTTP Capture](screenshots/step1_http_capture.png)

**✅ Expected Output:**
> A capture file containing multiple packets. Look for TCP packets with `HTTP GET` requests to `example.com`.

---

### 🔍 Exercise 2: Filter HTTP Traffic

**Step-by-Step Instructions:**
1. In Wireshark, locate the filter bar at the top.
2. Enter the filter: `http`
3. Press Enter to apply.

**📸 Screenshot Example:**
![Step 2 - Filter HTTP](screenshots/step2_filter_http.png)

**✅ Expected Output:**
> Only HTTP packets should be visible — making it easier to find web-related requests and responses.

---

### 🔍 Exercise 3: Analyze HTTP GET Requests

**Step-by-Step Instructions:**
1. In the filtered traffic, find a packet labeled `GET`.
2. Click it to view details.
3. Expand the **“Hypertext Transfer Protocol”** section.
4. Observe the requested URL, headers, and parameters.

**📸 Screenshot Example:**
![Step 3 - GET Request](screenshots/step3_get_request.png)

**✅ Expected Output:**
> Details like `GET /`, Host: `example.com`, and user-agent string should be visible.

---

### 🔍 Exercise 4: Analyze HTTP Responses

**Step-by-Step Instructions:**
1. Locate the response packet tied to the `GET` request.
2. Click to expand the **“Hypertext Transfer Protocol”** section.
3. Examine the status code, headers, and content type.

**📸 Screenshot Example:**
![Step 4 - HTTP Response](screenshots/step4_http_response.png)

**✅ Expected Output:**
> You should see `200 OK`, `Content-Type: text/html`, and possibly `Server` header.

---

### 🔍 Exercise 5: Extract and Examine Payload Data

**Step-by-Step Instructions:**
1. Right-click the response packet.
2. Select **Follow > TCP Stream**.
3. View the full HTTP conversation in the stream window.

**📸 Screenshot Example:**
![Step 5 - TCP Stream](screenshots/step5_tcp_stream.png)

**✅ Expected Output:**
> HTML content of the page should be visible, showing what was transferred to the browser.

---

## ✅ Conclusion

By completing these exercises, you've learned how to:
- Capture and filter HTTP traffic
- Analyze web requests and responses
- Extract data for security or troubleshooting

These skills are foundational for SOC analysts, network investigators, and penetration testers.

