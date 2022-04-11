# Computer-Security-Study

All about Computer Security Concepts + Logics 

## Index
##### 1. Basic Computer Security 
##### 2. Steganography 
##### 3. Cryptography
##### 4. Password Cracking
##### 5. Information Security Management 
##### 6. Access Control 
##### 7. Denial of Service Attack 
##### 8. Seucirty Risk Management 
##### 9. Law and Ethics

## Basic Computer Security Information 

### Data vs. Information

Data:
  - Raw Facts 
  - Unorganized 
  - Un processed
  - Chaotic or Unsorted
  - Input to a Process 

Information: 
  - Useful & Relevant 
  - Organized
  - Processed
  - Ordered or Sorted
  - Output of a Process 

### CIA of Information Security 

**C.I.A Triangle** - 3 Key characteristics of information that must be protected by information security </br>

- **Confidentiality** - only authorized parties can **view private information** 
- **Integrity** - **information is changed** only in a specified and authorized manner (by authroized users)
- **Availability** - **information is accessible** to authroized users whenever needed 

### Data Fonidentiality: Student grade (an information asset of high importance for studnet)

- In US, release of such information is reulated by Family Educational Rights and Privacy Act (FERPA) </br>
- In Canada, the same issue is regulated by Personal Information Protection and Electronic Documents Act </br>

Solution:
- Strong access control
- limiting number of places where data can appear 

### Data Integrity: Patient information in a hospital (the doctor should be able to trust that the information is correct)  

- In US, Health Insurance Portability and Accountability Act
- In Canada, Ontario's Personal Helath Information Protection Act -PHIPA

Solution:
- Strong access control 
- Cryptography (Hashing) 
- Documenting system activity (logs)

### Data Availability: Accessible and properly functioning web site (a key asset for an e-commerce company) 

- In US, Computer Fraud and Abuse Act (CFAA) applies to DoS-related attacks 
- In Canada, DoS activities are regulated under Criminal Code of Canada, Section 342: Unauthorized Use of Computer 

Solution: 
- Anti-DDoS System (Content distribution) 
- Well established backup procedure 

![image](https://user-images.githubusercontent.com/79100627/162499862-f2be5297-1f98-47a9-9e79-77406db210d2.png)

### McCumber Cube 

Rubik's cube-like detailed model for estabilishment & evaluation of Info. Security </br>
- To develop a secure system, one must consider not only **key security goals (CIA)** but also how these goals related to various states in which information resides and full range of aviable **security measures** 

![image](https://user-images.githubusercontent.com/79100627/162500154-a9e3cdc0-5a7d-4db8-8212-116a2b52357a.png)

### Information States 

- Storage - aka **'data at rest'**, such as data sotred in memory or on a disk 
- Transmission - aka **'data in transit'** - data being transferred between systems, in physical or electronic form 
- Processing - aka **'data in use'** - data being actively examined or modified 

### The cube expanded 

![image](https://user-images.githubusercontent.com/79100627/162500727-70e035b4-6c07-41d8-844b-cfd6c9b0aa47.png)

### Data In Use "Most Challenging to Protect"

Items in "Data at Rest" & "Data in Transit" can be some how protected with Cryptography, however Data in Use, item must be decrypted </br>
When the data that has been loaded into a process and is in the memory of the program that is running </br>
The data stored there for a while and become a "weak state" </br>

Solution:
- Clear and cleanse memory before releasing it 
- Full memory encryption incorporated in hardware designs 
- Enclaves - protected user-level code memory regions from processes running at higher privilege levels 
- Cyrptographic protocols (homographic encryption) 

### Homomorphic Encryption

Outsourcing Computation Privately: Encrypt the file and server provides a function and Encrypt F(x) and give it to client 

### Data Loss Precention System (DLP System)

Data Loss Prevention identifies, monitors, and protects data transfer through **deep content injection** and analysis of transaction parameters (source, destination, data object, and protocol) with a centralized management </br>

- Protecting Data in Use -> accomplished by protecting 'Data at Rest' and 'Data in Transit' 


### Threats 

Security Threat: any action/inaction that could cause disclosure, alteration, loss, damage or unavilability of a company's / individual's **assets**

- Three main components of a security threat:
  - **Target** (Asset with Vulnerability): organization's asset that might be attacked 
  - **Agent** (May or May not be present): people/ organizations originating the threat - intentional or non-intentional 
  - **Event**: Action that exploits target's vulnerability 

Threats with no Event != threat </br>

Threat without Agent = Data on a server is not backed up (Assets with V) + Flood or fire in the server (Event) </br>

Therefore, Assets (with vulnerability ) + Agent (outsider or insider) + Event (deliberate or accidental) = **Threats**

The definition of **Attack** = Assets w Vulnerability + Agent + Event (deliberate) 

### Main group of Threat Events

![image](https://user-images.githubusercontent.com/79100627/162503536-bcab1f6d-2d31-495b-add9-6fe468cb21a2.png)

### Intentional Attacks 

**Passive Attack** : attempts to learn to make use of info. from the system but does not affect system resources 
- Compromises Confidentiality 
- Generally hard to detect !!!
- Example: release of message content and traffic sniffing 

**Active Attack** : attempts to alter system resources or affect their operation 
- Compromises Integrity or Availability 
- Examples: masquerade, data modification and DoS 

### Deliberate Software Attacks 

A deliberate action aimed to violate / compromise a system's security through the use of specialized software </br>

Types of Attacks:
- Use of Malware
- Password Cracking
- DoS and DDoS 
- Spoofing
- Sniffing
- Main in the Middle 
- Phishing
- Pharming

### Use of Malware 

**Malware:** a program that is inserted into the victim system, susually covertly, with the intent of compromising the CIA of the Victim's data </br>

**Malware Types**:
- Virus
- Worms
- Trojan Horse
- Logic Bomb
- Rootkit
- Information Stealer 
- Ransomware 
- Scareware 
- Spyware 

Malware based on **How it Spreads/Propagates**:
- Carreid/ Speard by **'Carriers' + replicate** = Virus
- Spread over a network on **their own + replicate** = Worms
- Use **Social Enginnering** to Sneak in = Torjans 

Malware based on **What it Does**:
- corruption of system of data files - virus & worms 
- turning the victim into a zombie - botnet/bot for DDoS
- Theft information (login, password) - key loggers & Spyware 
- Hiding of its presence - Backdoor & rootkits 

### Virus 

a piece of software that can 'infect' other programs executable by modifying them 

**Phases of virus lifetime**:
- **propagation phase**: the virus places a copy of itself into other programs - each infected program will contain a clone of the virus which will itself enter a propagation phase 
- **dormant phase**: the virus is idle and eventually gets activated by some event (date, presence of another program or file, ... ) 
- **triggering phase**: the virus is activated to perform the function for which it was intended - again, it can be caused by a variety of system events 
- **execution phase**: the malicious function is performed and can be harmless/harmful 

**Classification of viruses by target**:
- boot sector infector: infects a master boot record
- file infector: infect executable file
- macro virus: infect file with macro or scripting code
- multipartite virus: uses multiple attack vectors 

**Classification of viruses by concealment strategy**:
- Polymorphic virus: use of cipher to encryp the main malware code and each iteration it can change the encryption. The decryption module also changes itself at each iteration
- Encrypted virus: a portion of the virus creates a random key and encrypts the remainder special case of polymorphic virus 
- Stealth virus: uses special technqiues to conceal its presence on the OS 
- Metamorphic virus: mutates and changes its "code" while retraining the same behaviour 

### Worm 

malware actively seeks out more machines to infect and then each infected machine serves as an automated launching pad for attacks on other machines</br>
- worms exploit software vulnerabilities in client or server programs to gain access to a new system (**worm** = power of virus + convenience of Interent) 
- Important: **virus vs worms**
  - viruses **need a carrier medium** (document or program to 'attach' itself to) and then require user action to propagate 
  - wroms **do not always need a carreir** (can some-times 'move' on their own), are typically spread through the Interent, and **NEVER rely on use action to replicate**

**Classification of worms by replication strategy**
- electronic mail or instant messaging: worm emails a copy of itself to other systsm or sends itself as an attachment via an instant message service 
- file sharing: worm copies itself on removable media USB
- remote execution capability: worm exploits a flaw in a remote execution facility 
- remote file access or transfer capability: worm uses a remote file access or transfer service to another system to copy itself 
- remote login capability: worm logs onto a remote system as a user and then uses commands to copy itself from one system to another 

**Classification of worms by target discovery**
- random: each compromised host probes random addresses in IP address space 
- hit list: the attacker compiles a long list of potentially vulnerable machines, each infected machin uses a part of this list 
- topological: worm uses information contained on the infected machine to find more hosts to scan 
- local subnet: worm uses the subnet address to find other vulnerable machine on the same network 

**State of Worm technology**
- multiplatfrom: target a variety of platforms 
- multi-exploit: penetrate systems in a variety of ways 
- ultrafast spreading: use various techniques to identify as many vulnerable machines in a short period of time 
- polymorphic 
- metamorphic 
- multi 'transport vehicle': can carry a variety of payloads (rootkits, spam generatros, bots, etc) 
- zero-day exploit - try to exploit new/unknown vulnerabilities 

### Zero-Day Attack 

Attack that exploits a previously unknown vulnerability in a computer application or OS 

### Trojan Horse 

malware that looks legitimate and is advertised as performing one activity but actually does something else; **it does NOT SELF REPLICATE** </br>

**Common Types of Trojans:** 
- remote access - designed to give an attacker control over a victim's system (client - server model) 
- data sending - designed to capture and redirect data (keystrokes, passwrods, to an attacker) to an attacker 
- destructive - designed to destroy data or kill the system 
- Denial of Service - designed to conduct a DoS attack on a predefined IP address
- FTP - designed to set up the infected system to serve as an FTP server for illegal software 

### Logic Bomb 

malware typically installed by an authroized user; lies dormant until triggered by a specific logical event; once triggered, it can perform any number of malicious activities </br>

- trigger events:
  - a certain date reached on the calendar check for organization payroll data
  - a person was fired 

### Rootkit 

stealthy software with root/administrator privileges - aims to modify the operation of the OS in order to facilitate a nonstandard or unauthorized functions </br>

- unlike virus, rootkit's goal is not to damage computer directly or to spread, but to hide the presence and / or control the function of other (malicious) software 
- Since rootkits change the OS, the only safe and foolproof way to handle a rootkit infection is to reformat the hard drive and reinstall the OS 

### Information Stealer 

malware that steals information such as: passwords, financial credentials, intellectual property, etc 
- subcategories of information stealers, based on their implementation, include: 
   - Software Keyloggers: capture keystrokes in a compromised system 
   - Memory (RAM) Scripaer : steals data when processed in memory 

### Ransomware

holds data or access to systems containing data until the victim pays a ransom
  - subcategories of ransomware based on implementation
    - CryptoLockers: encrypts victim's data or entire hard-drive get encrypted 
    - ScreenLockers: user is locked out and denied login to the system 

### Scareware

malicious programs that aim to scare users into installing a program 
  - program is 'supposed' to solve a problem that does not exist

### Spyware 

software that spies on users by gathering information without their consent, thus violating their privacy 

### Adware 

software that delivers advertising content in a manner that is unexpected and unwanted by the user 

### Denial of Service (DoS) 

Attacker sends a large number of requests to target </br>
- target gets overloaded and cannot respond to legitimate requests 

Distributed DoS = DDoS - a coordinated stream of requests is launched from many locations (zombies) simultaneously 
- zombie/bot: a compromised machine that can be commanded remotely by the master machine
- botnet: network of bots + master machine 

### Spoofing 

Insertion of forged (but trusted) identification data in order to gain illegitimate advantage 

- IP Spoofing: creation of IP packets with a forged source IP address,e.g. for the purpose of 'passing through a firewall' 
- Email Spoofing: creation of email messages with a forged sender address, e.g. for the purposes of social enginnering and data phising 
- Referrer Spoofing: creation of HTTP requests with a forged referrer URL, in order to gain access to a protected website
- DHCP Spoofing (active/passvie attack): Dynamic Host Configuration Protocoal (DHCP) server assigns an IP address and other network configurations to each device on a network 
  - An adversary can offer DHCP service to newly joined device and introduce spoofed default gateway and/or DNS server 

### Sniffing

use of program or device that can monitor data traveling over a network 
 
 - unauthroized sniffers can be very dangerous - they cannot be detected, yet they can sniff/extract cirtical information from the packets traveling over the network 
 - wireless sniffing is particularly simple, due to the 'open' nature of the wirelss medium 

### Man in the Middle Attack 

gives an illusion that two computers are communicating with each other, when actually they are sending and receiving data with a computer between them 
- spoffing and / or sniffing can be invovled 

Examples: 
- passive: attacker records, alters and resends data at a later time 
- active: attacker intercepts, alters and sends data before the orginal arrives to the recipient 

### Social Enginnering 
  
  process of using social skills to manipulate people into revealing vulnerable information 
    - either by believing that an email came from a legitimate person or believing that a web-site is the real web-site or both !

### Phishing 
 
 attempt to gain sensitive personal information by posing as a legitimate enitty
 - Simple Phishing: an email is sent tot he victim informing them of a problem and asking them to provide their username and password 

### Pharming 

pharming redirects user to false website without them even knowing it - typed in or clicked on URL looks OK 


## Steganography 

### Information Encryption vs Information Hiding 

#### Information Encryption

- The presence of information is 'obvious', but the content is **'scrambled'** using a crypto-key, so it becomes meaningless 
- No matter how 'unbreakable', encrypted message will arose suspicion

#### Information Hiding 
- The goal is not just to prevent others from accessing hidden information but **to make others unware of the very existence of the hidden information**


### Information Protection

![image](https://user-images.githubusercontent.com/79100627/162640260-ea75f32d-c192-4c2b-aeb3-1ed3e47465f5.png)

### Techniques of Information Hiding 

**Steganography**

- **Steganography **
  - Greek word for "concealed writing" 
  - Art and science of hiding information in some cover media for the purpose of protecting **information confidentiality**
  - **digital steganography - cover media**: image, text, audio, video 

- **Watermarking** 
  - Also aims to make information invisible, but for the purpose of protection of intellectual property 

- **Fingerprinting**
  - embedding user-unique marking to different copies of content for the purpose of tracking of intellectual property 


### Digital Steganography

Process of hiding information in digital multimedia files and in network packets 

Elements of digital steganography system include 
- Cover Media (C) that will hold the hidden data 
- Secret Message (M) - May be in plaintext or any other type of data 
- Stego function (Fe) and its inverse (Fe^-1)
- An Optional Stego-Key(K) or Password to hide and unhide the message 
- Stego Object (S) = Cover media + Secret Message 

![image](https://user-images.githubusercontent.com/79100627/162640782-434dc24d-e292-40c7-99e9-04ca3164b6a9.png)


### What Makes Steganography Work?

Digital Steganography takes advantage of 
- **Space Redundancy** in cover media 
   - Information can be hidden in unused areas of the file / text
- **Data Redundancy** in cover media in combination with inherent weakness of human perception 
   - Information can be embedded in the **Least Significant Bits (LSBs)** of an image 
   - Information can be embedded in high frequencies of audio spectrum

### Image Steganography

Bits in a pixel (Relative importance of different pixels is different)
- LSB - Least Significant Bit (Last Bit) 
- MSB - Most Significant Bit (1st Bit) 

LSB carries the least information - it changes most rapidly 

MSB carries the most information - it changes least rapidly 

### Why we use LSB

easiest and surprising effective way of hiding informaton in an image

LSB of each pixel is/are used to hide the **most significant bits of another image**

Algorithm:
- Load up host image and image to hide 
- Choose the number of bits you wish to hide the secret image in
    - more bit is used => **better quality of hidden image** / BUT **more distortion in cover image**
- To get original image back, pick out the LSBs According to the number used in Previous steps 


### Image with LSB

**Encoding**
- Host Pixel: **1011**0001
- Secret Pixel: **0011**1111
- New Image Pixel: **10110011**

**Decoding** 
- Host Pixel: 1011**0011**
- Bits used: 4
- New image: **00110000**

**Fewer LSB bits** used -> **Hiding capacity low / Better Stego-Image / Worse Recovered Image**

**More LSB bits** used -> **Hiding capacity high / Worse Stego Image / Better recovered Image**

### Pattern of LSB Embedding 

Secret bits can be embedded in LSBs of cover image in two ways </br>

**- Sequentially **
  - Simple embedding & extraction of secret bits 
  - Statistics of cover image abruptly changed - easy to detect 

**- Randomly **
  - The key to generate pseudorandom number must be sent 
  - Secret bits scattered throughout cover image 

### Water Marking vs Steganography

![image](https://user-images.githubusercontent.com/79100627/162642049-0cd0a498-02fb-4609-9111-cfa9ced2078d.png)

## Cryptography

### Process of Breaking a Cipher 
 
 - In modern cryptography encryption/decryption algorithm is not a secret 
 - Hacker probes various keys on the captured ciphertext 

### Factors that Influence Sucess of Crypto-Attack 

  - Time to perform one decryption - **t-one decryption**
  - Number of keys to try - **n-keys**

Crypto-attack speed = **n-keys x t-one decryption**

### Type of Attacks 

![image](https://user-images.githubusercontent.com/79100627/162643856-47c1a942-be93-46aa-9aa1-b1589f6cfe06.png)


### Subsitution Cipher 

Subsitution Cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet 

### Classical Ciphers 

**Cesar Cipher **

Ti - ith character of the plain text </br>
Ci - ith character of the cipher text </br>
i = 0,1,2,..., m </br>
m - length of the alphabet </br> 
k - shift </br>

Encryption: Ci = (Ti + k) mod m </br>
Decryption: Ti = (Ci - k) mod m </br>
</br>
**Polyalphabetic / Vigenere Cipher** </br>
</br>
**Complex subsitution** instead of shifting each character by the same number, characters located at different positions are shifted by different numbers 

### How to break a simple subsitution cipher 

- Frequnecy Analysis (The distribution of letters in a typical sample of English language text)
- Brute Force (Alphabet consist of 26 letters so mod 26)

### Vigenere Cipher 

**Plaintext:** HOW ARE YOU </br>
**Key:** ABC ABC ABC </br>
**Cipher text:** HPY ASG YPW </br>

Vigenere Cipher as an Algorithm </br>

Ti - ith character of the plain text </br>
Ci - ith character of the cipher text </br>
Ki - ith character of the key phrase  </br>
i = 0,1,2,...,m  </br>
m - length of the alphabet </br>
</br>
**Encryption:** Ci = (Ti + Ki) mod m </br>
**Decryption:** Ti = (Ci - Ki) mod m </br>

### Vigenere Cipher Example

Open text: ATTACK AT DAWN </br>
Key Phrase: CAT </br>
Length of Alphabet </br>

![image](https://user-images.githubusercontent.com/79100627/162644446-19fa1721-fd50-46d0-8345-a85d9f7369e4.png)

### Why Polyalphabetic / Vigenere Cipher 

Why is it so strong 

![image](https://user-images.githubusercontent.com/79100627/162644494-23aea2e8-713f-416c-8b9b-c480fb5ca34e.png)

The frequency of english graph is more uniformed and it is hard to guess how much key letter shifted. 

### Modern Cryptography 

**Symmetric-Key Algorithms:** The key used for encryption and decryption is identical and represent a shared secret 

**Aysmmetric-Key Algorithms:** Also known public-key algorithms, is any cryptographic system that uses pairs keys that public may know about one of them 


### Confusion vs Diffusion 

**Confusion:** Obscure relationship of the ciphertext and key: a ciphertext bit should depend on several parts of the key 
  - Subsitution tables 
 
**Diffusion:** Obscure relationship of plaintext and cipher text: each plaintext bit should be affect many cipher text bits 
  - Permutation 

![image](https://user-images.githubusercontent.com/79100627/162644730-8cfa8915-f4fe-492a-96c2-c5f328906ff5.png)

### Symmetric Ciphers 

Private-key encryption - uses the same secret/private key encrypt & decrypt information 

- Symmetric key = shared secret - must only be known to the communicating parties 

- To ensure full confidentiality in a group of N users, each pair of users must share a unique key 

Shared Secret: </br>
**(N*N(-1))/2**

(100*(99))/2 = 4950 keys 

### Symmetric Key Distribution

In system deploying symmetric encryption both the number and **distribution of keys is a problem**.

Solution: **Key Distribution Center (KDC)** - trusted 3rd party/server 

Each entity shares a secret key with KDC - **n keys** in total 

KDC hands out keys to paris of different entities, on demand, to enable confidential communication between them. 

![image](https://user-images.githubusercontent.com/79100627/162645049-519e344d-ea56-4e4b-8fc3-06238253f895.png)

### Symmetric Key Distribution Protocol 

![image](https://user-images.githubusercontent.com/79100627/162645081-34a0f548-4cd3-4340-8c6a-85e1295f41de.png)

- Alice wants to send a message to Bob
- KDC encrypts the Alice, Bob, Session Key with Bob's Key and adds the session key again and encrypts with KA 
- KDC sends the encrypted message back to Alice, Alices decrypts the message with her key and gets the session key and send to bob 
- Bob decrypts the message and gets the session key and know that it's from the Alice 


### Symmetric Ciphers 

Categories of Symmetric Encryption:

- **Stream Cipher**: encrypt digits (bytes) of a message one at a time 
    - Advantage: **Speed of transformation** - each symbol is encrypted as soon as it is read 
    - Disadvantage: **Low diffusion** - All information of a Plaintext symbol is contained in single ciphertext symbol 
    - Disadvantage: **Sensitivity to tampering** - An interceptor can splice together pieces of previous messages and transmit a new message that looks authentic 


### One Time Pad 

Stream Cipher- One Time Pad </br>
Improvement: Pseudo-Randomized Key </br>

![image](https://user-images.githubusercontent.com/79100627/162645390-a86353fd-4cd0-4574-a206-a00e0a549b8c.png)


### Block Cipher 

Data is divided into fixed length blocks </br>
</br>

Block Cipher - data is divided into fixed length blocks 
- All block bits are then acted upon to produce an output
- Advantage: **High Diffusion** - information from one plaintext symbol is diffused into several ciphertext symbols
- Disadvantage: **Slowness of Encryption** - an entire block must be accumulated before encryption / decryption can begin => slows down real-time app.
- DES, 3DES, AES

### DES - Data Encryption Standard 

- One of the first widely used symmetric-key block ciphers 
- Initially proposed by IBM (1974) latter modified and adopted by US National Bureau of Standards (1977) as an official Federal Information Processing Standard (FIPS)
- Takes a 64 bit block of plaintext and a 56-bit key to produce to a ciphertext block of 64 bits 
- In 1999, Electronic Frontier Foundation managed to break DES in 22 hours and 15 min 

### Triple DES (3DES) 

Symmetric-key block cipher which applies **DES 3 times** to each data block = Encrypt + Decrypt + Encrypt 

Ciphertext = Ek3(Dk2(Ek1(P))))

Triple DES Keying Options 

- Option 1: all three keys are independent 
  - Total Key Size = 168 bits 
  - Effective Security = 112 bits 
  - Strongest 

- Option 2: K1 and K2 are independent, K3 = K1
  - Total Key Size = 112 bits 
  - Effective Security = 80 bits 
  - moderately Secure 

- Option 3: All three keys are the same 
  - Weak No difference doing normal DES 

### Triple DES Pros and Cons 

- 3 DES, **Key option 1** is considered to be safe until 2030 
- DES was designed for efficient hardware implementation- **software implementation is very slow**, 3DES even slower 
- DES and 3 DES use 64-bit block size - to improve efficiency and security larger block sizes would be perferable 

### AES - (Advanced Encryption Standard) 

NIST issued call for a 3DES replacement in 1997 with requirements:
  - Sysmmetric Block Cipher 
  - Block size 128 
  - Key lengths 128, 192, or 256 
![image](https://user-images.githubusercontent.com/79100627/162646659-d02a3a16-1b00-492b-967c-4e593263805f.png)






