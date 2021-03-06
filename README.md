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

### Asymmetric Ciphers 

Public Key Encryption - Invovles the use of Two Separate but related keys: **Public and Private Key** 

- Public key is made public for others to use, private key is known only to its owner 
- Either key can encrypt a message - the other key must be used for decryption 

Asymmetric Encryption

**Protection Confidentiality: Alice receives message **
- Each user genrates a pair of keys 
- Each user places one of the keys in a public register - this becomes the **public key**; the other is **private key**
- If Bob wishes to send a **private message** to ALice, he uses Alice's public key 
- To decrypt Bob's message ALice uses her **private key** 

**Protection of Messages & Sender Integrity** 
- Alice sends a message to Bob - Bob is able to verify that Alice sent the message & data was not changed 

### Symmetric vs. Asymmetric Encryption - Common Misconceptions 

- Public-key encryption is a general purpose technique that has made symmetric encryption obsolete 
   - public-key encryption is **versatile but very slow** - symmetric encryption is still needed for encryption of large messages!
   - Public key encryption is **used for authentication digital signatures, and exchanges of secret keys!** 

- Exchange of asymmetric / public keys is much simpler than exchange of symmetric/secret keys 
  - Both schemes require a well established system and protocols 

### Diffie-Hellman 

![image](https://user-images.githubusercontent.com/79100627/162795377-7e93ce68-a795-4f42-9084-eab6590ed980.png)

### Diffie-Hellman The Basic Math 

- Before establishing a symmetric key, two parties choose **two integer numbers**
  - **p**: large prime number with **1024 bits** (300 decimal digits)
  - **g**: base or generator (primitive root of p) often **2,3,7**
- Alice choose a large random number x (0<= x <= p-1)
  - R1 = g^x mod p (Alice public key)
- Bob chooses a another large random number y ( 0 <= y <= p-1)
  - R2 = g^y mod p (Bob public key) 
- Alice sends Bob R1, Bob sends Alice R2
- Alice calculate K = (R2)^x mod p 
- Bob calculate K = (R1)^y mod p 

**K =g^xy mod p**

### Breaking Diffie-Hellman 

Consider Diffie Hellman Scheme with a common prime p = 11 and a primitive generator g=2 

If Alice has a public key KA+ = 9 what is Alice's private key KA- = X 
```
KA+ = 9 = g^x mod p = 2^x mod 11 

2^x = k * 11 + 9 where k = 1,2,3,...

= 20, for k =1 
= 31, for k =2
= 42, for k =3
= 53, for k =4
= 64, for k =5 

x = 6
```

### RSA 

- Based on practical difficulty of factoring the product of two large prime numbers 
- Diffie Hellman is used to generate a secret key **KEY AGREEMENT**
- RSA is used to exchange a secret key **KEY TRANSPORT**

### RSA Math

- Choose two random large prime numbers p and q 
  - The larger the numbers, the more difficult it is to break RSA, but longer it also takes to perform encoding and decoding 
  - RSA Laboratories recommends that the product of p and q be 1024 bits long 
- Compute **n =** **p*q** and **z = (p-1)*(q-1)**
- Choose a number **e < n** with no common factors with z other than 1 (e - used in encryption, public key) 
- Find a number d such that ed^-1 is exactly divisible by z. That is choose d such that ed mod z =1 

A Encrypts: C = P^e mod n 
B Decrypts: P = C^d mod n = (P^e mod n)^d mod n

### RSA Proof 

P = (P^e mod n)^d mod n 

1. Modulo rules allow 
  
  = (P^ed mod n) mod n = P^ed mod n

2. Theory of large prime numbers allows: 

  = (P^ed mod n) = P 
  
### RSA Important properties 

- Given (e,n) = Kpublic it is/should be impossible to comptue (d,n) = Kprivate 
- The public and private keys are 'commutative' 

![image](https://user-images.githubusercontent.com/79100627/162802776-c10a9d37-5797-4a35-8b2c-0820e6b5785c.png)

### RSA Applications 

- Digital Envelopes: fast exchange of confidential messages (secret message & secreet key sent at once) 
- Digital signature = message integrity + message authentication

### Digital Envelope - Use of Asymmetric Encryption for Fast Exchange of confidential messages 

- Generate random symmetric key Ksymmetric 
- Encrypt message using Ksymmetric - Digital letter 
- ENcrypt K symmetric using receiver's public key K+ - protective digital envelope 
- Send together 

![image](https://user-images.githubusercontent.com/79100627/162803454-fc407691-4d82-49bd-820e-255c7c732d7d.png)

### Digital Signature - Use of Asymmetric Encryption to protect message integrity + message authenticity  

![image](https://user-images.githubusercontent.com/79100627/162803688-5f30702a-3d14-49d4-9a87-aac3abf12ea0.png)


### Public Key / Digital Certificates 

- Rellable Public-Key Distribution: must invovle a truste thrid party 
   - Certificate Authority - A trusted government agency or a for-profit institution that issues Digital Certificates 
   - Digital Certificate - digital document that binds a public key to an identity (Person or organization and contains:
  ![image](https://user-images.githubusercontent.com/79100627/162804124-edf20cf9-a8af-400a-bf4e-4071752e1dce.png)

### Public-Key / Digital Certificates 

- Creation of public-key certificate: creation and use 

![image](https://user-images.githubusercontent.com/79100627/162804281-718711de-97fd-4102-8d0c-6c2af621c067.png)

### Creation & Verification of digital certificate 

![image](https://user-images.githubusercontent.com/79100627/162804396-469595a0-51f5-402f-b1a7-fbd1ccd99483.png)

### Encoding vs. Encryption vs. Hashing 

**Message Encoding**: trnasforms data to another format so that it can be properly /safely consumed by a different type of system 

- does not aim to keep information secret 
- does not require a key 
- encoding scheme is publicly available and relatively simple/fast to perform 

**Message Encryption**: transforms data to another format that cannot be easily consumed by anybody but the intended recipients 

- aims to keep information secret 
- requires a key 
- encryption scheme is publicly available but quite complex to perform / break 

**Message Hashing**: used to validate the integrity of a given content by producing a fixed-length string with following attributes 

- does not require a key 
- hashing algorithms are publically avialble 
- The same input will always produce the same output 
- any modification to the input should result in drastic change to that output 

### Hashing 

Message Integrity - accomploshed through the use of cryptographic hash functions 

- hash function creates a small fixed size digital 'summary' of the message that can be used as a message fingerprint, aka hash or message digest 

Typical hash size: 128,160,256,512 bits 

Popular Standards: 
- Message Digest 5 (MD5) No longer secure 
- Secure Hashing Algorithm 512 (SHA-512) 

![image](https://user-images.githubusercontent.com/79100627/162805479-0831e48d-3fca-4bf1-963a-2342b56f5bea.png)

### Hash Function Criteria 

To be eligible for a hash a function needs to meet 6 important criteria:

- Hash function h can be applied to block of data of any size
- Hash function h produces a fixed-length output.
- h(M) is relatively easy to compute for any given M, making both hardware and software implementation practical 
- **Collision Resistance** 
- **Preimage Resistance**
- **Second Preimage Resistance**

### Collision Resistance or Strong Collision Resistance 

must be extremely difficult to find any two M and M' such that h(M) = h(M') 

if strong collision is possible => digital signatures become meaning less 
![image](https://user-images.githubusercontent.com/79100627/162807879-cc3e7c7e-f575-470e-804c-9c36046b4a1b.png)

### Preimage Resistance or One Wayness

given a hash function h and y=h(M), it must be extremely difficult for Eve to find any message M' such that y=h(M')

- We should not be able to work 'backwards' and (re)create the original message from a given hash 

![image](https://user-images.githubusercontent.com/79100627/162808109-817a612a-6d82-4494-ad08-31c301744ecf.png)

![image](https://user-images.githubusercontent.com/79100627/162808208-010d043b-b9db-4cfb-8709-c177dc007ff6.png)

### Second Preimage Resistance or Weak Collision Resistance 

- given M and its hash h(M) it should be extremely difficult for Eve to find any message M' such that h(M) = h(M') 

- property intended to prevent an adversary from appending a falsified message to a given hash 

![image](https://user-images.githubusercontent.com/79100627/162808395-5fb9b440-96b1-47b1-a5ce-54c6c28eb96d.png)


## Password Cracking


### Passwrod 

A secret word/string of characters used to authenticate a user into a system 

- critical (often only) defense agaisnt intruders 
- Ideal password: easy to reember, hard to 'crack' 

### Password Cracking 

A method of gaining unauthroized access to a computer system by trying different passwords 
  - Cracking difficulty ~ size of password space 

### Brute Force Password Cracking (Exhaustive Password Search) 

Entire password space is tried 

- starts by using simple combinations of characters 

a) on 26 letter Alphabet, password of length 1/2/n: 

```
S-1 Letter = 26 
S-2 Letter = 26 * 26 
S-n Letter = 26 * 26 * ... 26 = 26^n
```

b) on A character Alphabet password of length n = A^n

C) on A character alphabet, passwords up to n characters 

![image](https://user-images.githubusercontent.com/79100627/162809614-f995242c-1cf2-4183-adff-e0e472522967.png)

### Example: Brute Force Password Search Space 

System A allows passwords to be any length (1-16) </br>
System B requires passwords to be at least 8 Characters long ( 8-16) </br>

A= 94

System A: S1-16 = Comb(i=1-16) A^i = A^(16+1) -1 / A-1 = 3.75 * 10^31 

System B: S8-16 = Comb(i=1-16) A^i - Comb(7-i=1) Ai = 3.75 * 10^31

### Example 2: Brute Force Password Search Space 

A system allows passwords consisting of 4 lower-case letters followed by 3 digit numbers 

LLLLDDD -> 26^4 * 10^3 

### Example 3: Brute Force Password Search Space 

If no letter is repeated and password is not case snesitive?

LLL -> A (B-Z) (C-Z)

26 * 25 * 24 

### Biased Attack 

- The search space is further reduced by focusing on most likely combinations of words and / or numbers 

Example: Biased Attack on 4-Digit pins 

Aussme a system requires that access passwords be comprised of 4 digits 

Total unbiased search space: any number between 0-9999 (10,000) serach space: 

### Dictionary Attack 

- Users often create password using common dictionary words 
- instead of tyring every password, dictionary attack probes only common dictionary words 
- **Faster than brute force**, as it uses smaller (more likely) search space
- Still might take considerable time, and might fail in the end 

### Pre- Computed Dictionary Attacks

Achieves Time-Space trade off by pre-computing list of hashes of dictionary words 

- Pre-computed hashes are compared against those in a stolen password file 
- Rainbow tables 
  - pregenerated sets/lists of hashes - n*Gbyte size 
  - allow extremelly rapid searching 

### Rainbow Table 

Is a precomputed table for reversing cryptographic hash functions 

Space time tradeoff 
- It uses less computer processing time and more storate compared to brute force.
- It uses more processing time and less storage than a simple lookup table 

**Rainbow Table Construction**

Main idea: define a reudction function R that maps hash values back into values in P
  - Reduction function is not meant to be "an inverse of the hash function"

![image](https://user-images.githubusercontent.com/79100627/162812981-bed5094a-605d-463b-a7c6-474ea7708102.png)

**Using Rainbow Table**

You got hold of hash "re3xes" and you would like to find 

- Apply reduction function R and check the result with tail column of rainbow 
- No match? apply hash function H and reduction function R and check again 
- Stop once you have found a match OR your have constructed a chain with length L with no match 

![image](https://user-images.githubusercontent.com/79100627/162814931-d86d22c8-88fb-4c16-8cfa-fec465a6bc58.png)


### Password Salting 

Adding unique random value to each password before hashing

- both the hash and salt are stored 
- does not fully prevent against password cracking but makes it harder / more time consuming 

![image](https://user-images.githubusercontent.com/79100627/162815104-5a19a84f-eac7-4138-a433-fd97ea246289.png)

### Password Salting Benefits 

- Dictionary and Rainbow attacks impossible to perform 
- Prevents duplicate passwords from being visible in password file 
- becomes impossible to find out whether a person has used the same password on multiple systems 

### LM Password Hashing (Not really a hash but a cryptographic value 

- user password is converted to **all uppercase**
- password has null characters added to it until it equals 14 characters 
- new password split into two 7 characters (half)
- Two 7 bytes halves are used to create two 64 bit (8 byte) long DES encryption kyes, by inserting a null bit after every seven bits
- each key is used to DES - encrypt the constant ASCII string "KGS!@#$%" , resulting in two 16-byte long ciphertext values 
- finally two 16 byte hashes are concatenated to form the 32 byte long hash 

### LM Drawbacks 

- Case Insensitive - significantly reduces character set that attacker must use (A - from 96 down to 69) 
- 14- character long passwords split into two 7 character long halves - search space is reduced 
- DES encryption is not considered safe anymore 

### NTLM Hashing 

- Applies MD4 hash algorithm 3 times 
- Advantages 
  - allows for distinction between upper and lower case 
  - does not split password into smaller easier to crack, chunks 
- Disadvantages: does not use salting 
  - salt - random combination of 0 & 1 added to a password 
  - every bit of salt => 2X password - cracking demands on storage and/ or computation 

## Management of Infomation Security 

### Goal of Info. Sec vs. Goals of IT

Not always in complete alignment; sometimes in conflict 

IT Professionals focus on: 
  - Cost of system creation & Operation
  - Timelines of System creation
  - Ease of system use for end user 
  - Quality of system performance (Speed, Delay,...) 

Info. Sec. Professionals focus on:
  - Protection of organization's information systems at all cost necessary 

### Info. Sec. within an organization - Option 1: Most Common 
![image](https://user-images.githubusercontent.com/79100627/162851034-df74353e-b8ad-4b73-9e71-c276e488c4db.png)

Most common organizational structure: in 50% of compnaies </br>
Info. Sec. Under (reports to & shares budget with) IT department
- Pros:
  - To whomever Info. Sec. Manager reports to, understands technological issues 
  - Security Staff and IT staff collaborate on day-to-day basis 
  - There is only 'one person' between Info. Sec. Manager and CEO 

- Cons: 
  - CEO are likely to discriminate against Info. Sec. Function as Other IT objectives (e.g. Computer Performance, ease of use, ...) 

### Info. Sec. Within an orgaization - Option 2: When Security Goes Beyond "Computer Security" 

![image](https://user-images.githubusercontent.com/79100627/162851300-cb0ce3a7-0346-4a00-bcbe-0d8c25042df9.png)

Info. Sec. reports to Administrative Service Dep - performs services for all workers in the organization, much like HR.

- Pros:
  - Acknowledges that info. and info. systems are found everywhere throughout the organziation - all employees are expected to 'work with' Info. Sec. Department 
  - Supports efforts to secure information no matter its form (paper, verbal, etc.) rather than viewing info.sec. function as strictly computer-& network-related issues 

- Cons:
  - Administrative Service VP often does not know much about IT and Info. Sec. - may not be effective in communicating with CEO 
  - Often subject to cost-cutting measures 

### Info. Sec. Within an organization - Option 3: When Risk to Computer Security => Risk to Business 

![image](https://user-images.githubusercontent.com/79100627/162851623-421f4570-44ec-45a4-945c-88542066eb0e.png)

Info. Sec. reports to Insurance & Risk Management Dept. This approach typically invovles assessing the extent/likelihood of potential losses in case of weakened info. sec. function

- Pros:
  - brings greater resources and management attention to Info. Sec.
  - Cheif Risk Manager (CRM) is likely to be prevention oriented and adopt a longer-term viewpoint 

- Cons:
  - CRM are often not familiar with information system technology 
  - May over-emphasize strategic issues, and overlook operational and administrative aspects of info. sec. (e.g. change of access privileges when people chage jobs) 

### Info. Sec. in Different Compnaies 

Info Sec within Risk Management (Hospital): should be employed when company's revenues critically depend on CIA of information - if information CIA gets jeopardized, company looses money 

Info Sec within IT (Amazon): should be employed in companies where it is critical to obtain / use latest technology, and bulk of work done by Info. Sec. department is related to that (new) technology

Info Sec within Admin Services (IBM): should be employed in companies that may not worry abotu using the latest technology, but rather about properly securing existing data and whatever technology (info. infrastructure) is currently in place  

### NIST Cybersecurity Framework: 22 Core Functions 

![image](https://user-images.githubusercontent.com/79100627/162852659-b5c5ae27-1eae-4ff8-89c7-b9a075520d11.png)

## Access Control

### NIST Cybersecurity Framework 

Protect...
- Access Control: limit access to information resources and associated facilities to authorized users, processes and devices 


### Stages of Access Controls 

**Identification** - obtain identity of an entity requesting access to a logical or physical area 

**Authentication** - confirm identity of the entity seeking access ...
  - Making sure user's credential are not false - the user 'is' who they claim to be 

**Authorization** - determine whether the authenticated entity is permitted to access a particular system (e.g. OS, firewall, router, database, ...) and its resources (e.g., system's files) 
  - typically implemented by means of access control lists/rules

### Basic Steps in Access Control

![image](https://user-images.githubusercontent.com/79100627/163079931-9aad857d-ca01-4cbe-836d-c2560984c526.png)

### Identification

mechanism that provides info about an unverified entity - aka supplicant - that wants to be granted access to a logical or physical area 

- Must be unique value that can be mapped to one and only one entity within the administered domain 
- In most organizations, identification = name OR (initial + surname) 

### Authentication 

Process of validating a person's supplicant's purported identity 

Types of authentication mechanisms: 
- Something you know: Password
- Something you have: Cryptographic Tokens or smart cards
- Something you are: fingerprints, palm prints, iris scans,...
- Something you produce: pattern recognition of voice, signature/handwriting, typing rhythm 

### Types of Tokens 

**Static Tokens**

**Swipe cards** - ID and ATM cards 
- aka 'dumb cards', transmit same credential every time - the credential (base secret) is impractical to memorize 
- PIN/password not on the card - ATM encrypts PIN provided by user and sends it to a database for verification...

**Smart card** - Swipe cards with a chip
- Chip contains a CPU, memory blocks (RAM, ROM,...) and on chip encryption module 
- Stores 100x data stored on magnetic strip: encrypted PIN & other info about card holder 
- Card checks user's PIN & generates a certificate to authorize transaction process

### Synchronous (One-Time Password) Tokens 

Small LCD device that generates a unique new password periodically 
- Token combines 'base secret' with clock to generate new password 
- Token and authentication server must have their clocks synchronized - which is often a challenge 

![image](https://user-images.githubusercontent.com/79100627/163082253-ed047ae4-8490-4944-9c1e-de130abe6de0.png)

### Synchronous Token example 

![image](https://user-images.githubusercontent.com/79100627/163082598-1d728149-6770-4764-939c-b89990db2ee1.png)


### Asynchronous (Challenge-Response) Tokens 

Instead of time, token uses a challenge/nonce provided by the system to generate the password 

- eg. Token can generate the password by 
- 1. applying a unique hash function to (user's base secret + nonce) 
- 2. encrypting nonce using user's/token's public key 

![image](https://user-images.githubusercontent.com/79100627/163082950-fd5d726a-add6-4080-b53b-ced53cd32e24.png)

### Asynchronous Token example 

![image](https://user-images.githubusercontent.com/79100627/163083042-dbd06ae4-bdb4-4c99-83b7-b3218560c9ef.png)

### Evaluation of Biometric Systems 

Confusion Matrix 
- Also known as Error Matrix, is a table visualization of the performance of statistical classification process

![image](https://user-images.githubusercontent.com/79100627/163083441-59bdb47b-b064-43b1-94ba-224ea482ec1c.png)

### Authentication: Something you are ...

Something you are: Evaluation of Biometic Systems 

False Reject Rate (FRR) , aka False Negative 
- % of authorized users who are denied access
- false negatives do not represent a threat to security but an annoyance to legitimate users 

False Accept Rate (FAR), aka False Positive 
- % of unauthorized / fraudulent users who are allowed access to system 
- Represent serous security breach 

Crossover Error Rate (CER) aka Equal Error Rate 
- point at which FRR = FAR - Operating Point of choice for most biometric systems - provides balance between sensitivity & performance 
- techniques with 1% CER superior to 5% CER 

![image](https://user-images.githubusercontent.com/79100627/163084101-3bb6c06c-f4b8-43d6-8c98-85af9b2efd44.png)
![image](https://user-images.githubusercontent.com/79100627/163084114-25e9d02e-fb32-420e-bbe6-92b329005aed.png)

### Authentication: Something you are 

![image](https://user-images.githubusercontent.com/79100627/163084518-d91d3e09-b122-431e-ae44-23096b3babe8.png)


### Single - and multi-factor authentication

System that use one authentication credential (e.g. something you know) are known as one-factor authetnication systems.

Systems that require strong protection typically combine multiple authentication mechanisms - e.g. something you have and something you know. They are known as two factor authetnciation systems

## Denial of Service Attack 


### Categories of DDoS Attack 

![image](https://user-images.githubusercontent.com/79100627/163085762-c973846f-040c-4445-92b0-0e3d6df7119c.png)

### DDoS Targeting Bandwidth 

Bandwidth = Capacity of network link connecting a server 

Typically, server bandwidth << ISP bandwidth 

Hence, it is always possible to 'congest' server link => degraded / non existent service for (some) legitimate users 

### DoS Targeting Bandwidth 

Flooding - most common type of bandwidth DDoS 

- Network Layer - ICMP Flood 
- Transport Layer - UDP, TCP Flood 
- Application Layer - HTTP Flood


### DoS Targeting System Resources 

Aim to consume limited server's OS-level resources typically by misusing lower-layer protocols (TCP, IP, ...) 

- Buffers holding arriving IP packets 
- Tables of open TCP connections 

### DoS Targeting System Resources Examples

**TCP-SYN Flood**
- Attacker sends a flood of TCP-SYN request in possibly spoofed IP packets => 3-way handshake never completed 
- Half open connections bind server resources - no new connections can be made 

![image](https://user-images.githubusercontent.com/79100627/163087196-b59c7049-4403-41ac-990e-813856e2c7d2.png)


### DoS Targeting Application Resources

Involve valid-looking application requests that 
- consume significant application resources, or 
- cause application to crash 

Example
- HTTP attack requesting large PDF files from a server 
- attack on a web server that amkes database queries using computationally-costly requests 

### DoS vs DDoS Attacks 

DoS attack - one attacking machine

Distributed DoS attack - employ numerous attacking machines - so called botnets 
- direct DDoS attacks 
- reflector DDoS attacks
- amplification DDoS attacks 

### Botnet for DDoS 

Botnet: A network of compromised machines (bots, zombies, or agents) controlled by the attacker 

Attacker/ Master: machine that is physically used by the bot master / herder
- Can be anywhere with any type of interent connection 

Stepping Stone: attacker can use 1 or more stepping stones to hide his or her true identity and location 
- Typically, There is a telnet connection between botnet master and its stepping stones 
- Due to legal issue and physical location, using stepping stones located in foreign countries make it much more difficult to trace the original attacker 

Handler: A computer that have been compromised by the bot master and loaded with special applications to manage agents 
- Handler accepts commands from the attackers by way of stepping stones and relay those commands to waiting agents 
- Each handler is responsible for (only) a group of agents 
- If handlers communicate with their respective agents via TCP connections, they will get. have a list of agents' IP addresses 

Bot / Zombie / Agent: A compromised 3rd party machine with the injected malware 
- Real power of the botnet - capable of launching attack and/or propagating itself to other machines 
- Largest known botnet: Mariposa, 8-12 million bots (2008)

### Bot Net Maps

![image](https://user-images.githubusercontent.com/79100627/163206709-07727eed-1d23-4b33-aa09-ebd93ed47183.png)

### Botnet Propagation 

**Vulnerability Scan**: manual propagation involving systematic scanning / searching for hosts with particular vulnerabilities 

**Worm Exploits**: Automated propagation process via worms that traverse the Internet infecting hosts and installing the agent software 

**Web based malware exploits**: Automated propagation by means of drive by download from compromised web sites

### Botnet: to Build or to Rent?

Building a botnet: "Ready to use" development kits are available on the black market - packages containing C&C software & bot software 

- Dirt Jumper - Sophisticated software with a HTTP C&C server & SQL database for keeping track of infected bots 
- Requires technical expertise and is time consuming 

### Direct DDoS attacks 

Agents conducting the attack are compromised systems running the attacker's program
- The source IP addresses in attacking packets are often spoofed 
- Protocols used: any - ICMP, TCP, UDP, DNS, HTTP

![image](https://user-images.githubusercontent.com/79100627/163210821-223c2320-8cbb-4fe9-819c-b62aa39d213d.png)

### Reflector DDoS attacks 

Indirect attack utilizing innocent uncompromised intermediate nodes and any simple 'request-reply' protocols 
- The source IP address in attacking packet = spoofed victim's IP 
- aims to obscure the identity of attacking machines 

![image](https://user-images.githubusercontent.com/79100627/163211112-a46bd816-67a3-4d11-8960-a048a8a95e42.png)

### Amplified & Reflector DDoS (Is HTTP Reflector DDoS Possible?)

HTTP runs on top of an establiashed TCP connection. It is impossible to send an HTTP reqeust to the Victim without a valid 3-way TCP handshake 

HTTP is not a simple 'request-reply' protocol =? reflector attack not possible 

![image](https://user-images.githubusercontent.com/79100627/163211738-2b430057-2403-40dd-a683-6248e4115781.png)

### Amplified & Reflector DDoS (DNS Reflector DDoS - Possible or not?) 

DNS runs on top of UDP (or TCP), and acts as a simple 'request-reply' protocol => reflector attack possible. 

![image](https://user-images.githubusercontent.com/79100627/163212094-2ecfb615-4aed-4864-b9da-0b9026b559a9.png)


### Amplified DDoS attack

variant of reflector attack: aim to generate multiple reflector packets for each original packet set 
- can be achieved by directing original requests to a broadcast address of a large LAN 
- ICMP ech request to 129.1.0.0 => multiple ech replies 
- TCP cannot be used as it is 'connection oriented' 

### DDoS Defences 

**Classical DDoS Defences**

Attack prevention - before attack 
- Up-to-date anti-malware to prevent the creation of botnets 
- Monitoring of traffic by ISP, or 'cyber-spies', to detect packets between attackers and stepping-stones/ handlers

Attack detection and Filtering - During the Attack 
- Firewall monitors for suspicious (blacklisted) IPs or suspicious packets (SYN flood) and drops them 
- ISP minitors and drops packets with spoofed IP addr 

**Modern Lines of DDoS Defence**

Content Delivery Networks (Akamai)
- Web-site content is placed on multiple / redundant locations
- Users are 'directed' to geographically closeset servers 
- multiple server => no 'Single point of failure'

Scrubbing Centers (Prolexic) 
- Packets destined for an enterprise are routed through , and screened by, a special cloud-based network of routers 
- If an attack pattern is identified => suspicious packets are dropped before reaching the victim 

### Appliiation Layer DDoS Attacks 

fastest growing category of DDoS attacks 
- Hard to distinguish between legitimate & malicious HTTP requests 

### How Browser Works 

based on HTML page retrieve first 
- then HTML page parsed and individual objects are subsequently retrieved 

### Puppetnets 

mechanism of conducting HTTP DDoS by exploiting (hijacking) legitimate/ uninfected machines

![image](https://user-images.githubusercontent.com/79100627/163215519-7523e8e0-4353-408b-b210-47061d5b95d1.png)

### Puppetnets Pros vs Cons 

**Advantages**
- minimal cost 
- puppet-bots are generally trusted with good history - harder to detect, and not subject to black listing or firewall blocking 

**Disadvantage**
- very dynamic bot population
- attacks can not be fully controlled or predicted 

## Risk Management 

### Risk 

likelihood that a chosen action or activity (including the choice of inaction) will lead to a loss (un undesired outcome)

### Risk Management 

Identification, assessment and prioritization of risks followed by coordinated use of resources to monitor, contorl or minimize the impact of risk-related events


### Basic Strategies to Control Risks 

- Avoidance
  - do not proceed with the activity or system that creates this risk 
  - Recommended for vulerabilities with very high risk factor that are very costly to fix 

- Reduced Likelihood (Control) 
  - by implementing suitable controls, lower the chances of the vulnerability being exploited 
  - Recommended for vulnerabilities with high risk factor that are moderately costly to fix 

- Transference 
  - Share responsibility for the risk with a thrid party 
  - Recommended for vulnerabilities with high risk factor that are moderately costly to fix if employing otuside expertise 

- Migitiation
  - reduce impact should an attack still exploit the vulnerability 
  - Recommended for vulnerabilities that are low-risk and moderately costly to fix 

- Acceptance 
  - Understand consequences and acknowledge risks without any attempt to control or mitigate 
  - Recommended when vulnerability risk < cost of any control 


### Risk Assessment 

Provides relative numerical risk ratings (scores) to each vulnerability 
- In risk management, it is not the presence of a vulnerability that really matters, but the associated risk

Risk:
- Possibility that a threat successfully acts upon a vulnerability and 
- How severe the consequences would be R = P * V

**Extended Risk Formula v.1.**

R = Pa * Ps * V

- Pa = Probability that an attack/threat (against a vulnerability) takes place 
- Ps = Probability that the attack successfully exploits the vulnerability 

R = Pa * (1-Pe) * V 

- Pe = Probability that the system's security measures effectively protect against the attack (reflection of system's security effectiveness) 

**Extended Whitman's Risk Formula**

R = Pa * V * [1 - CC + UK]

Pa = probability that certain vulnerability (affecting a particular asset) will / could get exploited 
v = value of information asset [1,100]
CC = current control = percentage / fraction of risk already mitigated by current control 
UK = Uncertainty of knowledge = fraction of risk that is not fully known 

### Risk Determination Example 

![image](https://user-images.githubusercontent.com/79100627/163240643-01667a05-8723-4b38-ac44-2ad337037022.png)


Asset A 
Vulnerability 1 rated as 55 = 50 * (1.0 - 0 + 0.1)
Vulnerability 2 rated as 35 = 50 * (1- 0.5 + 0.2)
Vulnerability 3 rated as 12 = 10 * (1- 0 + 0.2) 


### Risk Analysis 

**Qualitative Risk **
- Scenario based approach - uses labels & relative values (high/low) rather than numbers; blends in experience & personal judgement 

**Quantitative Risk **
- Predicts level of monetary loss for each threat and monetary benefit of controlling the treat 
- Each element is quantified and entered into equations 
  - asset value
  - threat frequency 
  - severity of vulnerability 
  - damage impact 

### Qualitative Analysis vs Quantitative Analysis 

![image](https://user-images.githubusercontent.com/79100627/163241761-1c25c5fe-34c9-4b1e-bd0f-4f2563eda789.png)

### Single Loss Expectancy - most likley loss (in value) from an attack 

SLE = AV * EF 

AV: Asset Value 

EF: Exposure Factor 

### Annualized Rate of Occurrence & Annualized Loss Expectancy 

Annaulized Rate of Occurrence (ARO - indicates how often attack is expected to successfully occur in a year) 
- If an attack occurs once every 2 years => ARO = 0.5 

Annualized Loss Expectancy - Overall loss incurred by an attack 
- ALE = ARO * SLE


### ALE Example 

```
A widget manufacturer has installed new network servers,
changing its network from P2P, to client/server-based network.
The network consists of 200 users who make an average of
$20 an hour, working on 200 workstations.
Previously, none of the workstations involved in the network
had an anti-virus software installed on the machines. This was
because there was no connection to the Internet and the
workstations did not have USB/disk drives or Internet
connectivity, so the risk of viruses was deemed minimal.
One of the new servers provides a broadband connection to
the Internet, which employees can now use to send and receive
email, and surf the Internet.

One of the managers read in a
trade magazine that other widget
companies have reported an
annual 75% chance of virus
infection after installing T1 lines,
and it may take up to 3 hours to
restore the system.
A vendor will sell licensed copies
of antivirus for all servers and
the 200 workstations at a cost
of $4,700 per year.

The company has asked you to determine the annual loss that
can be expected from viruses, and whether it is cost effective
to purchase licensed copies of anti-virus software.
```

Based on the Provided data 

ARO = 0.75

SLE = 200 Users * 20 hours (user-hour) * 3 hours = $12,000

ALE = SLE* ARO = $ 9,000 

ACS = $4700 

### Cost Benefit Analysis Formula 

NRRB = (ALE(Prior) - ALE(Post)) - ACS 

ALE(Prior) - ALE before implementing control

ALE(Post) - ALE after implementing control

ACS - annual cost of safeguard 

### Example of NRRB 

![image](https://user-images.githubusercontent.com/79100627/163243065-d7d29a1a-d721-4154-8dac-688104e88ddf.png)







