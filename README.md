# Artemis-Financial-Practices-for-Secure-Software-Report

Briefly summarize your client, Artemis Financial, and their software requirements. Who was the client? What issue did they want you to address?

Artemis Financial is a consulting company that develops individualized financial plans for their customers. The financial plans include savings, retirement, investments, and insurance. Artemis Financial wants to modernize their operations. As a crucial part of the success of their custom software, they also want to use the most current and effective software security. Artemis Financial has a RESTful web application programming interface (API). They are seeking consultation in how to protect the organization from external threats.

What did you do very well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall wellbeing?

Working with AES encryption was one of the most enjoyable parts of this project. It is incredibly important to code with security in mind. Considering the potential vulnerabilities that each line of code may present and being intentional with the code that is written can protect companies, users, and any other unintended party that may fall victim due to a breach of security. A breach could result in financial, reputational, or life altering consequences. In severe cases, it may be an irrecoverable loss for the company that could lead its total collapse.

What part of the vulnerability assessment was challenging or helpful to you?

The most challenging part of the vulnerability assessment was implementing the certificate that was created. I was unable to get my server and my browser to recognize the correct key, leaving me with an unsecure connection.

How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use? How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?

First, I reconfigured the code to add AES encryption algorithm using a hash function and bit levels. I ensured that the encryption was in by performing a checksum verification. Once encryption was in place, I created a self-signed certificate using the Java Keytool and exported the certificate. Next, I reconfigured the application.properties file to include the correct settings to implement the self-signed certificate I created. The security of the new https protection was then tested by opening a new browser page with the https://localhost:8443/hash address. The page is intended to show a secure connection.

After the code had been refactored, I performed an OWASP Dependency-Check Maven to determine that the refactored code did not introduce any new security vulnerabilities. Once the secondary testing was completed, I performed functional testing by manually reviewing the code for proper functionality and any remaining possible vulnerabilities. I used this step to perform a final check to ensure the code runs without errors.

In future projects I can assess the systems current encryption method and decide if additional encryption methods may be more impactful. I can then perform and OWASP Dependency-Check to determine the vulnerabilites that exist, while being mindful of false positives and false negatives. Servicing the necessary vulnerabilities will help to narrow the chances of a breach. After the automated testing is complete functional testing should be performed to manually detect security risks that may exist. This step can be challenging as it requires the developer to consider many avenues that may be used to gain entry to the system, closing those openings as they are discovered.

What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?

This class introduced many new tools and practices that should be carried into future projects. First and foremost, the persistent focus on security throughout the developing process, rather than only in the later stages as though it were an afterthought. Holding security in mind throughout development changes the perspective of the entire system and closes vulnerabilities before they are even created.

Tools and resources such as dependency checks and encryption ensure that data is stored and transmitted securely, which is just as important as preventing any other kind of potential breach, if not more.

Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?

If future employers were interested in this assignment, I would showcase my work with AES encryption and assessing dependency checks. Even though I was not able to create a secure connection, I'm still quite pleased that I learned to create both JKS and p12 certificates.
