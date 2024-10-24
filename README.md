Project Overview
In this project, I configured basic firewall rules using Windows Firewall. The goal was to block incoming HTTP traffic (port 80) while allowing HTTPS traffic (port 443). This demonstrates how to control network traffic to improve security by only permitting secure communications over HTTPS.

Steps I Followed
1. Allow HTTPS Traffic
First, I allowed incoming HTTPS traffic on port 443 so that secure communications could continue. Here’s how I did it:

I opened Windows Firewall and went to Advanced Settings.
Under Inbound Rules, I created a new rule for HTTPS (port 443).
I configured the rule as follows:
Rule Type: Port
Protocol: TCP
Port: 443
Action: Allow the connection
Here’s a screenshot of the rule I created:
![image](https://github.com/user-attachments/assets/eedf836e-b8ae-4538-a2fd-693951820b31)



2. Block HTTP Traffic
Next, I blocked all HTTP traffic coming into the system by configuring a rule to block port 80. Here’s the process I followed:

Again, I opened Windows Firewall and went to Inbound Rules.
I created a new rule for HTTP (port 80).
I configured the rule as follows:
Rule Type: Port
Protocol: TCP
Port: 80
Action: Block the connection
Here’s a screenshot of the blocked HTTP traffic rule:
![image](https://github.com/user-attachments/assets/90f710dd-8e40-436c-baad-8aca32864915)



3. Testing the Firewall Rules
After creating the rules, I tested them by trying to access websites using both HTTP and HTTPS:

When I tried to access http://example.com, it failed as expected because HTTP traffic was blocked.
![image](https://github.com/user-attachments/assets/fad46495-2b72-49c3-8b76-ce376a47e438)

When I accessed https://example.com, it worked perfectly since HTTPS traffic was allowed.
![image](https://github.com/user-attachments/assets/02691020-16ff-4cbb-b157-d79981811955)

Conclusion
This project shows a simple yet effective way to manage incoming traffic using Windows Firewall. By allowing only secure traffic over HTTPS and blocking insecure HTTP, I improved the security of the system.
