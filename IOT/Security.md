---
onenote-id: 0-4244bc4b65f240a38a57ea136b94e31a!1-D084F068F621FF9!3928
---
- More sensitive information
	- Coverage & depth of personal data
- Actuate over physical world

- Confidentiality
	- Only released to authorised persons
- Integrity
	- Always correct and not altered
 
- Availability
	- Whenever needed

![Identify and assign values to all assets Asset Val...](../../../../img/OneNote/Security%20image%205aa5fea01cd26abc.png)

Sensitive Information
 
- Sensor data
- Server commands
- IoT service info
	- Control instructions
- Stored traces

![Machine generated alternative text UserEnvironment...](../../../../img/OneNote/Security%20image%209aa2894faf064cd4.png) ![Machine generated alternative text Authenticated d...](../../../../img/OneNote/Security%20image%20127e83b869e2e909.png)

Threats
 
Service disruption, privacy leaks, system misbehaviour

Wider Security Measures

- Authenticity
	- Robust authentication
	- Robust trust
	- Software & System certification
	- Complicated handshakes
		- Consumes more power
	- Client provides secret info
		- Could be compromised
- Confidentiality
	- Strong encryption
		- Stronger uses more power
		- Trust may rely on recommendations
			- More communications
- Proper behaviour
	- Monitoring/detection
		- Each abnormal activity detection requires different method to detect
			- Additional load

Frameworks
 
- Evolving
- No one solution

Hash  
One-Way Function
 
- Variable length input
	- Fixed length output
- Publicly available process
- Verifying information
- Mod operator
	- Number to a power
	- Remainder after division
		- Could be anywhere
			- Collisions
				- Need stronger function

Cryptography
 
- Symmetric
	- Same key used
	- AES
		- Zigbee
			- Would prefer more lightweight option
- Asymmetric
	- Public/private key
	- RSA
- Processes public

Digital Signatures
 
- Stamp data
- Data cannot be changed
	- Can tell
- Message digest
- Hash & Encrypt with private key
	- Need to validate public key
	- Use certificates
		- CA

Authentication
 
- Who they claim to be
- IoT authenticates devices
- Provide
	- Is
		- Biometrics
	- Has
		- Key
	- Knows
		- Password
- Username/password
	- Protect over the wire
- Key exchange
	- Diffie-Helman

|   |   |   |   |   |
|---|---|---|---|---|
||**Roles**|**Threats**|**Vulnerabilities**|**Securing**|
|**Device**|- Generate sensor data<br>- React to actuator commands|- Loss of device<br>- Tampering|- Embedded<br>    - Tiny<br>    - Hidden<br>- Can be tampered with without noticing|- Require authentication<br>- Prevent tampering<br>    - Monitor possible misbehaviour<br>    - Don't store personal data on device<br>- Implementation<br>    - Silicon<br>        - Strongest<br>        - Specialised equipment required<br>    - Firmware<br>    - Software<br>        - Weakest|
|**Network**|- Transports sensor data & actuator commands|- Sniffing<br>- Intercepting<br>- Jamming|- Wireless<br>    - Easy to join<br>        - Sniff<br>        - Intercept<br>        - Jam channel|- Sniffing<br>    - Encryption<br>- Manipulation<br>    - Authentication<br>    - Integrity checks<br>        - MACs<br>- Interception<br>    - Authentication<br>- Jamming<br>    - Monitor channel activity<br>    - Backup channel|
|**System**|- Collect & process sensor data<br>- Generate actuator commands<br>- Produces traces|- Server intrusion|- OS & Software modules<br>    - Contain bugs for exploitation<br>- Complicated configs<br>    - Misconfiguration|- Host compromise<br>    - Proper functioning OS<br>    - Protect physical machines<br>    - Adequate config<br>- IoT software modules<br>    - High quality control<br>    - Monitoring|
|**User**|- Access to info and controls over IoT system|- Unauthorised users|- Inadequate user practice<br>    - Compromised|- Strong authentication<br>- Good security practice<br>- Thorough onboarding process|

|   |   |   |
|---|---|---|
||**Symmetric**|**Asymmetric**|
|**Computational Speed**|Fast|More complex, thus slow|
|**Key Reusability**|Cannot reuse|Yes|
|**Key Exchange**|Over secure channel|Public key in public|
|**Example**|DES, RC5, AES, Blowfish|RSA, ECC|

![To Sign Ill pay 2300 for the item. Hash Function A...](../../../../img/OneNote/Security%20image%205f0ccf5a56f11ca7.png) ![2 I The CA is trustworthy. CAs public key 4 2 Appr...](../../../../img/OneNote/Security%20image%2094eeae22eae3e25d.png)

Diffie-Hellman
 
Non-secret values in blue, and secret values in **red**
 
1. Alice and Bob publicly agree to use a modulus _p_ = 23 and base _g_ = 5 (which is a primitive root modulo 23).
2. Alice chooses a secret integer **a** = 4, then sends Bob _A_ = _g_**a** mod _p_
	- _A_ = 5**4** mod 23 = 4
3. Bob chooses a secret integer **b** = 3, then sends Alice _B_ = _g_**b** mod _p_
	- _B_ = 5**3** mod 23 = 10
4. Alice computes **s** = _B_**a** mod _p_
	- **s** = 10**4** mod 23 = 18
5. Bob computes **s** = _A_**b** mod _p_
	- **s** = 4**3** mod 23 = 18
6. Alice and Bob now share a secret (the number 18).
 
- Used for secure channel to swap a symmetric key
	- Symmetric used for bulk
		- Quicker
- Can be used to establish public & private keys
	- RSA usually used

 [![FileDiffieHellman Key Exchange.svg](../../../../img/OneNote/Security%20image%204245e3b73c2a7834.png)](https://upload.wikimedia.org/wikipedia/commons/4/46/Diffie-Hellman_Key_Exchange.svg)![Both Alice and Bob nave arrived at the same values...](../../../../img/OneNote/Security%20image%20be7533aca64904f4.png)

