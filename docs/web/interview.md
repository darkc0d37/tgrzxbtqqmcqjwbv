**Q1. What are the differences between Base64 and Base64URL encoding?**
> In base64url, '+' and '/' characters are replaced by '-' and '_' from base64 encoding to avoid interpretation as URL characters and '=' padding of base64 will be neglected.

**Q2. Name 5 (or more) types of Cross-Site Scripting.**
> DOM, Self, Stored, Reflected, Blind.

**Q3. How does Boolean *Error* Inferential (Blind) SQL Injection work?**
> Boolean Error Inferential (Blind) SQL injection works by using errors vs no errors as a means to determine if the injected statement is true or false. I think that this could be done by 1) induced by the attacker e.g. 1/0 division errors, or 2) based on server handling

**Q4. What is the Same-Origin Policy (SOP) and how does it work?**
> 

**Q5. How does the TE.TE variant of HTTP Request Smuggling work?**
> The transfer encoding header is obfuscated in such a way that only one of the servers ( reverse proxy and the actual server) actually uses it, then, it is exploited the same way a cl:te or te:cl would be depending on which server your obfuscation worked on.

**Q6. What is DOM Clobbering and how can it be used to bypass (some) HTML sanitizers, resulting in XSS?**
> DOM Clobbering is a way to manipulate the DOM using only HTML elements (i.e. no JavaScript). By using the id or name attribute of some elements, it is possible to create global variables in the DOM. This can lead to XSS in some cases. 

> I created a dynamic cheatsheet where you can see how DOM Clobbering works: https://tib3rius.com/dom/ (works best in Chrome)!


**Q7. What is the difference between Web Cache Deception and Web Cache Poisoning?**
> Web Cache Deception involves finding some dynamic page which you can access via a URL a web cache will automatically cache (e.g. if /transactions can be accessed at /transactions.jpg). If an attacker can trick a victim into visiting the cacheable URL, they can then load the same URL and retrieve the victim's information from the cache.

> Web Cache Poisoning involves finding an input which results in some exploitable change in the response, but doesn't form part of the cache key for the request. When an attacker sends their payload, the exploited response will be cached and then delivered to anyone who accesses the page

**Q8. What two criteria must be met to exploit Session Fixation?**
> ession Fixation is not the same thing as Session Hijacking, but rather a type of Session Hijacking attack. The two criteria are:

> 1. Attacker must be able to forcibly set a (syntactically valid but otherwise inactive) session token in the victim's browser (e.g. using XSS / CRLF injection).

> 2. Once the victim authenticates, the application uses the session token already present and does not set a new one.