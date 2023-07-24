# SOAP
> The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?
## Solution
When an instance is created, this page is shown:
![A webpage with the title: "Computer Science" and subtitle "We have been ranked to be among the best universities int he world!" It shows three panels titled Carnegie Mellon University Africa, Pico CTF, and CyLab Africa, each with a button that says "Details."](https://github.com/still-in-beta/CTF_Writeups/blob/master/2023/picoctf/SOAP/Screenshot%202023-07-23%20at%205.24.00%20PM.png?raw=true)
When “Details” is clicked for any of the panels, the following appears, with differing text in front of the “Special Info::::”
![Special info Created by security and privacy experts](https://github.com/still-in-beta/CTF_Writeups/blob/master/2023/picoctf/SOAP/Screenshot%202023-07-23%20at%205.24.11%20PM.png?raw=true)
The problem is tagged XXE, which suggests that a XML external entity injection must be utilized (the hint confirms this). Burpsuite is recommended for this to track and modify the XML requests. In Burp, the XML request looks something like this, with 1, 2, and 3 showing in the request for the panels from left to right:
![A burp suite request containing a header and an xml request with the number 1 enclosed in ID tags, which are enclosed in data tags](https://github.com/still-in-beta/CTF_Writeups/blob/master/2023/picoctf/SOAP/Screenshot%202023-07-23%20at%205.24.25%20PM.png?raw=true)
The request is in a very clear XML format, with the input between the ID tags being what we wish to insert a payload into, which is accessing specific sensitive files. I tried a few known sensitive directories such as /etc/shadow and /etc/group, but /etc/passwd was the one that returned the flag.
![A burpsuite request with a similar request, except the 1 is replaced with ampersand X.X.E and outside of the data tags it says "!DOCTYPE d [<!ENTITY  xxe SYSTEM "file:///etc/passwd">]](https://github.com/still-in-beta/CTF_Writeups/blob/master/2023/picoctf/SOAP/Screenshot%202023-07-23%20at%205.24.37%20PM.png?raw=true)
