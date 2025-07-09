
 📡 Traceroute Lab – Analyzing the Path to Facebook.com
 
🧪 Objective
Use the traceroute command to analyze the network path from the local machine to facebook.com (157.240.221.35) and understand how packets travel across different nodes.

📜 Command Used

traceroute facebook.com
🖥️ Raw Output

traceroute to facebook.com (157.240.221.35), 30 hops max, 60 byte packets

 1  240.2.112.45 (240.2.112.45)  11.306 ms 240.2.112.12 (240.2.112.12)  9.612 ms 240.2.112.15 (240.2.112.15)  11.752 ms
 
 2  242.6.28.1 (242.6.28.1)  12.007 ms 242.6.29.133 (242.6.29.133)  11.450 ms 242.6.28.7 (242.6.28.7)  10.912 ms
 
 3  peer-as16509.pr01.lhr7.tfbnw.net (157.240.78.41)  11.721 ms  11.399 ms peer-as16509.pr02.lhr7.tfbnw.net (157.240.77.17)  11.096 ms
 
 4  ae7.pr01.lhr7.tfbnw.net (157.240.78.40)  9.310 ms  10.087 ms  11.482 ms
 
 5  po185.asw01.lhr3.tfbnw.net (129.134.104.112)  10.834 ms po186.asw02.lhr3.tfbnw.net (129.134.104.118)  11.807 ms po185.asw01.lhr7.tfbnw.net (129.134.104.124)  12.274 ms
 
 6  psw01.lhr8.tfbnw.net (129.134.57.129)  11.572 ms psw02.lhr8.tfbnw.net (129.134.57.128)  12.242 ms  12.118 ms
 
 7  163.77.195.252 (163.77.195.252)  14.449 ms msw1af.01.lhr8.tfbnw.net (129.134.57.121)  12.045 ms 163.77.195.254 (163.77.195.254)  13.284 ms
 
 8  * * *
🔍 Analysis
Hops 1–2: Local and ISP routing — shows internal network routing and ISP backbone transit.

Hops 3–7: The traffic enters Facebook's infrastructure (hostnames ending in .tfbnw.net, which stands for "The Facebook Network").

Hop 8: Shows * * *, meaning that no ICMP response was received. This is common when firewalls or security filters prevent traceroute replies.

Latency: All hops responded with sub-15ms latency, indicating fast and efficient routing to the destination before hop 8.

✅ Key Takeaways

Traceroute is useful for identifying where delays or blockages occur in the network path.

Facebook's infrastructure uses multiple load-balanced paths, as shown by multiple IPs in a single hop.

Some hops may not respond due to firewalls or security policies — this does not always indicate an issue.



