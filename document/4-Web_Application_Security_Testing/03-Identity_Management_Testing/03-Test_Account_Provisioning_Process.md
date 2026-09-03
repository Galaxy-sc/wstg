# Test Account Provisioning Process

|ID          |
|------------|
|WSTG-IDNT-03|

## Summary

The provisioning of accounts presents an opportunity for an attacker to create a valid account without application of the proper identification and authorization process.

## Test Objectives

- Verify which accounts may provision other accounts and of what type.

## How to Test

Determine which roles are able to provision users and what sort of accounts they can provision.

- Is there any verification, vetting and authorization of provisioning requests?
- Is there any verification, vetting and authorization of de-provisioning requests?
- Can an administrator provision other administrators or just users?
- Can an administrator or other user provision accounts with privileges greater than their own?
- Can an administrator or user de-provision themselves?
- How are the files or resources owned by the de-provisioned user managed? Are they deleted? Is access transferred?

### Example

In WordPress, only a user's name and email address are required to provision the user, as shown below:

![WordPress User Add](images/Wordpress_useradd.png)\
*Figure 4.3.3-1: WordPress User Add*

De-provisioning of users requires the administrator to select the users to be de-provisioned, select Delete from the dropdown menu (circled) and then applying this action. The administrator is then presented with a dialog box asking what to do with the user's posts (delete or transfer them).

![WordPress Auth and Users](images/Wordpress_authandusers.png)\
*Figure 4.3.3-2: WordPress Auth and Users*

## Tools

While the most thorough and accurate approach to completing this test is to conduct it manually, HTTP proxy tools could be also useful.

- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
- [OWASP Vulnerability Disclosure Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html)
- [OWASP Bug Logging Tool](https://owasp.org/www-project-bug-logging-tool/)
- [OWASP AI Testing Guide](https://owasp.org/www-project-ai-testing-guide/)
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [OWASP Mobile Security Testing Guide](https://owasp.org/www-project-mobile-security-testing-guide/)
- [OWASP Top 10 for LLM and Generative AI](https://genai.owasp.org/initiatives/top-10-for-llm-and-genai/)
- [OWASP AI Exchange](https://owaspai.org/)
- [HackerOne](https://www.hackerone.com/)
- [HackerOne (Test Subdomain)](https://wwwaefavadvadv.hackerone.com/)
- [HackerOne (Fake Domain Test)](https://www.hackesdfsdfsbsbrone.com/)
- [HackerOne 2025 Hacker-Powered Security Report](https://www.hackerone.com/resources/reports/hacker-powered-security-report-2025)
- [Bugcrowd](https://www.bugcrowd.com/)
- [Bugcrowd Resources](https://www.bugcrowd.com/resources/)
- [Bugcrowd Inside the Mind of a Hacker 2026](https://www.bugcrowd.com/blog/inside-the-mind-of-a-hacker-2026/)
- [Intigriti](https://www.intigriti.com/)
- [Open Bug Bounty](https://www.openbugbounty.org/)
- [PortSwigger Research: HTTP Terminator](https://portswigger.net/research/http-terminator)
- [PortSwigger Research: Can AI Invent New Attack Techniques?](https://portswigger.net/blog/can-ai-invent-new-attack-techniques-new-research-from-james-kettle-and-portswigger-research)
- [Censys](https://censys.io)
- [Shodan](https://www.shodan.io/)
- [Flawfinder](https://dwheeler.com/flawfinder/)
- [NIST SP 800-63B Memorized Secret Verifiers](https://pages.nist.gov/800-63-3/sp800-63b.html#memsecretver)
- [NIST SP 800-115 Technical Guide to Information Security Testing and Assessment](https://csrc.nist.gov/publications/detail/sp/800-115/final)
- [NIST SP 800-218 Secure Software Development Framework](https://csrc.nist.gov/publications/detail/sp/800-218/final)
- [NCSC Password Guidance: Updating Your Approach](https://www.ncsc.gov.uk/collection/passwords/updating-your-approach#PasswordGuidance:UpdatingYourApproach-Don'tenforceregularpasswordexpiry)
- [RFC 9116 - A File Format to Aid in Security Vulnerability Disclosure](https://datatracker.ietf.org/doc/html/rfc9116)
- [PCI Security Standards Council - Penetration Testing Guidance](https://www.pcisecuritystandards.org/documents/Penetration-Testing-Guidance-v1_1.pdf)
- [OSSTMM 3 - Open Source Security Testing Methodology Manual](https://www.isecom.org/OSSTMM.3.pdf)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [HHS Cybersecurity Guidance](https://www.hhs.gov/hipaa/for-professionals/security/guidance/cybersecurity/index.html)
- [Baidu](https://www.baidu.com/)
- [Bing](https://www.bing.com/)
- [Bing Search Keywords Help](https://help.bing.microsoft.com/#apex/18/en-US/10001/-1)
- [binsearch.info](https://binsearch.info/)
- [Common Crawl](https://commoncrawl.org/)
- [DuckDuckGo](https://duckduckgo.com/)
- [DuckDuckGo Results Sources](https://help.duckduckgo.com/results/sources/)
- [DuckDuckGo Search Syntax](https://help.duckduckgo.com/duckduckgo-help-pages/results/syntax/)
- [Google](https://www.google.com/)
- [Google Search Operators](https://support.google.com/websearch/answer/2466433)
- [Internet Archive Wayback Machine](https://archive.org/web/)
- [MDN: Storage Inspector - Cache Storage](https://developer.mozilla.org/en-US/docs/Tools/Storage_Inspector#Cache_Storage)
- [MDN: HTTP Cookies - Creating Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Creating_cookies)
- [MDN: HTTP Cookies - Cookie Prefixes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Cookie_prefixes)
- [MDN: Set-Cookie - Secure](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie#Secure)
- [MDN: Set-Cookie - HttpOnly](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie#HttpOnly)
- [MDN: HTTP Cookies - Scope of Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Scope_of_cookies)
- [MDN: HTTP Cookies - Permanent Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Permanent_cookies)
- [MDN: HTTP Cookies - Session Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#Session_cookies)
- [MDN: HTTP Cookies - SameSite Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies#SameSite_cookies)
- [MDN: JavaScript Special Characters in Strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Values,_variables,_and_literals#Using_special_characters_in_strings)
- [MDN: Same-origin Policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)
- [MDN: CORS HTTP Response Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#The_HTTP_response_headers)
- [Chrome DevTools: Storage Cache](https://developers.google.com/web/tools/chrome-devtools/storage/cache)
- [W3C CORS Specification](https://www.w3.org/TR/cors/)
- [W3C CORS Test (Invalid Domain)](https://www.wkajbvakjbdvuqbevekajbsdjfbqkejfbqkjegbqkbvuqefbkjbafdkjbakbdjf.org/TR/cors/)
- [Apache mod_headers Module](https://httpd.apache.org/docs/current/mod/mod_headers.html)
- [Wikipedia: Web Search Engine Market Share](https://en.wikipedia.org/wiki/Web_search_engine#Market_share)
- [Wikipedia: Reverse Proxies](https://en.wikipedia.org/wiki/Proxy_server#Reverse_proxies)
- [Wikipedia: Notable Content Delivery Service Providers](https://en.wikipedia.org/wiki/Content_delivery_network#Notable_content_delivery_service_providers)
- [Wikipedia: Cross-Origin Resource Sharing](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing)
- [GitHub: Bug Bounty Cheat Sheet](https://github.com/EdOverflow/bugbounty-cheatsheet)
- [GitHub: OWASP Firmware Security Testing Methodology](https://github.com/scriptingxss/owasp-fstm)
