# Wireshark-Packet-Capture-lab

![Wireshark Logo](https://github.com/Lantyy/WireShark-Packet-Capture-lab/assets/122828853/ffe14e63-5e78-428c-b14f-0f92237f214f)

# This Project
This is a instructional step by step process to using the packet capture tool **Wireshark** for Defensive Security and Analyzing Network Traffic.

My purpose for this lab is to learn more about Analyzing Network Traffic and Security Monitoring.

# Virtual Machines / Tools
This lab consists of a Linux virtual machine and Wireshark.

  ~ **Kali Linux** ~ Used a Kali Linux virtual machine with the Wireshark tool that came prepackaged.
  
  ~ **Wireshark** ~ Used this tool to capture packets on a certain interface, then use various filters to observe website traffic.

# Lab Creation Steps

Installed and set up a Kali Linux virtual machine.
![Screenshot 2023-08-21 (1)](https://github.com/Lantyy/WireShark-Packet-Capture-lab/assets/122828853/f8c6a686-ee69-49f7-ab5b-ac8945e09196)


Captured and saved packets on a detected interface using Wireshark.
![Screenshot 2023-08-21 (2)](https://github.com/Lantyy/WireShark-Packet-Capture-lab/assets/122828853/dcf7736f-3133-4fa6-8570-03f30f531b0f)


Used a display filter to observe a certain packet protocol.

~ Filtered for only packets with 'TCP port 80'; tcp.port == 80

![Screenshot 2023-08-21 (3)](https://github.com/Lantyy/WireShark-Packet-Capture-lab/assets/122828853/4e57c032-99bd-4106-ae49-3bedbd3e62f9)


Employed a display filter to detect a certain IP address in the capture.

~ Filtered for any IP address that is '8.43.85.97'; ip.addr == 8.43.85.97

![Screenshot 2023-08-21 (4)](https://github.com/Lantyy/WireShark-Packet-Capture-lab/assets/122828853/4ea62707-47f8-4021-b550-6fbc8c945d8b)


Used a conditional filter to locate certain packets in the capture.

~ Filtered for any IP address but '8.43.85.97' and include all other packets; !(ip.addr == 8.43.85.97) and (tcp.port == 443 or tcp.port == 80)


![Screenshot 2023-08-21 (5)](https://github.com/Lantyy/WireShark-Packet-Capture-lab/assets/122828853/e420149b-3e28-4ed4-8e1a-bb975b14ecd0)


# Lab Thoughts & Takeaways
In creating and deploying this lab I learned that Wireshark is an advantageous tool. Capturing, saving and filtering packets can be very helpful in analyzing network traffic so appropriate action can be taken if needed in a network security monitoring situation. 

Credit: This lab was provided by Coursera, I followed the steps used in the course to create and replicate this lab. 
  
~ Link ~ https://www.coursera.org/projects/wireshark-for-beginners-capture-packets#outcomes
