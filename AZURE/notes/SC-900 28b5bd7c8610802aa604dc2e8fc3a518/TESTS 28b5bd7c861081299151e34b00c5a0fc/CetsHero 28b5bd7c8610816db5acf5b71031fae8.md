# CetsHero

Which Microsoft Purview data classification type supports the use of regular expressions?

**A**exact data match (EDM)

**B**fingerprint classifier

**C**sensitive information types (SlTs)

**D**trainable classifier

- **Sensitive Information Types (SITs):** SITs are designed to identify specific types of sensitive data (like credit card numbers, social security numbers, passport numbers, etc.) within your content. They primarily use a combination of:
    - **Regular Expressions (Regex):** To define patterns that match the format of the sensitive information.
    - Keyword lists: To find specific words or phrases that often appear near the sensitive information.
    - Checksums: To validate certain numbers (like credit card numbers).
    - Proximity: To ensure supporting evidence is close to the primary element.You can use Microsoft's built-in SITs or create custom SITs using your own regular expressions.

Let's look at why the other options are not the primary choice for using regular expressions:

- **A. Exact Data Match (EDM):** EDM classifiers are used to identify sensitive information based on **exact matches** from a structured database (e.g., a CSV file of customer IDs). While an EDM SIT might use an underlying regular expression for the *primary element* that it's looking for in the content (e.g., "look for something that *looks* like a customer ID first, then cross-reference it with my exact list"), its core strength is the **exact lookup against a database**, not just pattern matching with regex.
- **B. Fingerprint classifier:** A fingerprint classifier is used to identify **exact or near-exact duplicates of documents or files**. You provide a sample document, and Purview creates a "fingerprint" (hash) of it. It doesn't rely on regular expressions to identify patterns within the text; it relies on the unique digital fingerprint of the document itself.
- **D. Trainable classifier:** Trainable classifiers use **machine learning** to identify content based on what the content *is*, rather than what it *contains* in terms of specific patterns or data elements. You train them by providing many examples of content that falls into a specific category (e.g., "financial reports" or "HR documents"). They do *not* use regular expressions as their primary detection mechanism; they learn from the content's context and characteristics.

---

What is a use case for implementing information barrier policies in Microsoft 365?

**A**to restrict unauthenticated access to Microsoft 365

**B**to restrict Microsoft Teams chats between certain groups within an organization

**C**to restrict Microsoft Exchange Online email between certain groups within an organization

**D**to restrict data sharing to external email recipients

Information barriers are supported in Microsoft Teams, SharePoint Online, and OneDrive for Business. A compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams. Information barrier policies can be used for situations like these:

---

What are two capabilities of Microsoft Defender for Endpoint? Each correct selection presents a complete solution.

NOTE: Each correct selection is worth one point.

- [ ]  **A**automated investigation and remediation
- [ ]  **B**transport encryption
- [ ]  **C**shadow IT detection
- [ ]  **D**attack surface reduction

[https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint](https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint)? view=o365-worldwide

---

Which two tasks can you implement by using data loss prevention (DLP) policies in Microsoft 365? Each correct answer presents a complete solution.

NOTE: Each correct selection is worth one point.

- [ ]  **A**Display policy tips to users who are about to violate your organization's policies.
- [ ]  **B**Enable disk encryption on endpoints.
- [ ]  **C**Protect documents in Microsoft OneDrive that contain sensitive information.
- [ ]  **D**Apply security baselines to devices.
- [ ]  https://docs.microsoft.com/en-us/microsoft-365/compliance/dlp-learn-about-dlp?view=o365-worldwide
- [ ]  

---

What can you specify in Microsoft 365 sensitivity labels?

**A**how long files must be preserved

**B**when to archive an email message

**C**which watermark to add to files

**D**where to store files

https://learn.microsoft.com/en-us/purview/sensitivity-labels?view=o365-worldwide