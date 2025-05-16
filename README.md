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
4. Open your browser and go to: [http://kedaipakkarim.hstn.me](http://kedaipakkarim.hstn.me/)
5. Let the page load completely.
6. Stop the capture by clicking the **red square** icon.

**📸 Screenshot:**
<p align="center">
Figure 1: Launch Wireshark <br/>
<img src="https://i.imgur.com/Mba1Cqw.png" height="80%" width="80%" alt="Wireshark Basic Project"/>
<p align="center">
Figure 2: Captured HTTP traffic showing a successful HTTP 200 OK response with content type text/html <br/>
<img src="https://i.imgur.com/4SvoAbU.png" height="80%" width="80%" alt="Wireshark Basic Project"/>
</p> 
  
**✅ Expected Output:**
> A capture file containing multiple packets.  
> Look for TCP packets with `HTTP GET` requests and HTTP responses such as `HTTP/1.1 200 OK`, preferably to a known HTTP site (e.g., `http://kedaipakkarim.hstn.me`).

---

### 🔍 Exercise 2: Filter HTTP Traffic

**Step-by-Step Instructions:**
1. In Wireshark, locate the filter bar at the top.
2. Enter the filter: `http`
3. Press Enter to apply.

**📸 Screenshot:**
<p align="center">
Figure 3:  HTTP Traffic Captured After Applying Filter in Wireshark <br/>
<img src="https://i.imgur.com/k7WhIZf.png" height="80%" width="80%" alt="Wireshark Basic Project"/>
</p>

**✅ Expected Output:**
> Only HTTP packets should be visible in the capture, helping to identify web-related traffic such as GET and response headers.

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

