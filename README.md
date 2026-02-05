# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com

<img width="1864" height="1016" alt="Screenshot 2026-02-05 130539" src="https://github.com/user-attachments/assets/8f0966cf-5e7b-4e1b-876d-b0b3f508d417" />

filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com

<img width="1883" height="1039" alt="Screenshot 2026-02-05 130645" src="https://github.com/user-attachments/assets/ffdb2e45-94a7-46f4-bb21-94e0a7e66ff3" />


intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

<img width="1893" height="1040" alt="Screenshot 2026-02-05 130725" src="https://github.com/user-attachments/assets/cabb82d8-65dc-4774-872c-9a387df313ff" />


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.

<img width="1871" height="1034" alt="Screenshot 2026-02-05 130756" src="https://github.com/user-attachments/assets/92061b9b-5038-41c0-be6d-e757bf507a67" />

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.

<img width="1885" height="998" alt="image" src="https://github.com/user-attachments/assets/8353e411-e181-449c-8ec1-0c67a240a485" />

link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.

w<img width="1891" height="1088" alt="Screenshot 2026-02-05 130945" src="https://github.com/user-attachments/assets/b661015f-0896-4b90-863b-052a1107f981" />

cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

<img width="1885" height="1028" alt="image" src="https://github.com/user-attachments/assets/b7de962c-13b2-4d61-8b7b-8ca7bc5f7e1a" />

 
#DNS Enumeration


##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:

![WhatsApp Image 2026-02-05 at 1 45 42 PM](https://github.com/user-attachments/assets/0720b9fd-2f48-4517-88a9-cc0c2e970992)
![WhatsApp Image 2026-02-05 at 2 11 53 PM](https://github.com/user-attachments/assets/fb35768b-d381-493c-ac44-392f19b27fa1)


![WhatsApp Image 2026-02-05 at 2 12 18 PM](https://github.com/user-attachments/assets/ad9a3b7d-18c4-43a2-9600-f385c2b714a4)




##dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.

![WhatsApp Image 2026-02-05 at 2 12 51 PM](https://github.com/user-attachments/assets/b877394b-49ba-4e04-87ef-412ab4343515)
![WhatsApp Image 2026-02-05 at 2 13 17 PM](https://github.com/user-attachments/assets/dedd2502-488e-4023-91d9-5189c86b078a)


##smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.

![WhatsApp Image 2026-02-05 at 2 13 41 PM](https://github.com/user-attachments/assets/4e7ae6a5-59d7-4bbe-b50a-c0630789b4b7)


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

![WhatsApp Image 2026-02-05 at 2 14 03 PM](https://github.com/user-attachments/assets/e74654da-dd58-4793-9224-1fc53357cd0c)

select any username in the first column of the above file and check the same

![WhatsApp Image 2026-02-05 at 2 15 43 PM](https://github.com/user-attachments/assets/506f75bf-046d-406b-b437-b4f7e774dfc2)



#Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ##Output

 ![WhatsApp Image 2026-02-05 at 2 20 02 PM](https://github.com/user-attachments/assets/2bda0eef-9de8-4fa7-aba8-655bb99fbf5b)


## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:
![WhatsApp Image 2026-02-05 at 2 14 41 PM](https://github.com/user-attachments/assets/08d2544b-f912-4dcc-bd4a-4ec1a59934f3)

## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

