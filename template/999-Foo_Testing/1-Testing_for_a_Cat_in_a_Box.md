# Testing for a Cat in a Box

|ID          |
|------------|
|WSTG-FOO-001|

## Summary

A [box](https://en.wikipedia.org/wiki/Box) is a tangible object, typically made up of six rectangular sides. It typically has the ability to be open or closed, and to contain things. Boxes are often used to transport other objects, or to store objects temporarily or permanently. Boxes can be constructed from various materials, such as cardboard, wood, or steel.

A box may or may not contain a [cat](https://en.wikipedia.org/wiki/Cat).

If a box has a cat in it and the box owner does not know, the box owner is vulnerable to surprise or shock if they discover the cat unexpectedly.

## Test Objectives

Assess whether a box contains a cat.

## How to Test

To test for a cat in a box, use any of the following methods.

### Open the Box and Observe its Interior

These instructions assume the box is constructed of cardboard. You may need to modify the steps slightly to accommodate other materials.

[![Box](images/box.jpg "An empty box made of corrugated fiberboard")](https://en.wikipedia.org/wiki/Box)\
*Figure 999.1-1: Image of an Empty Open Cardboard Box*

Use the following steps to open the box.

1. If the box is taped shut, use a knife to cut the tape. Be cautious of putting the knife too far into the box, just in case it does contain a cat.
2. If the box is not taped shut, grasp each cardboard flap and open it.

Once the box is open, observe the interior of the box to determine if there is a cat inside.

### Compel the Cat to Reveal Itself

This test is based on observing a reaction from the cat in the box, if there is one. While it is a valid method, it is not as definite as the first test method.

A reaction may be:

- Sounds of mewing or the shuffling of tiny cat paws.
- The appearance of various parts of a cat, such as ears, tail, or paws, from any holes or open areas of the box.
- A cat exiting the box.

Attempt to compel a reaction from the possible cat in the box by using any of these tactics:

- Scratch gently on the exterior of the box.
- Place catnip near the box.
- Using a bowl and some corn kernels, replicate the sound of dry cat food being poured into a cat bowl.

If no cat reveals itself, it is unlikely there is a cat in the box. However, this test is indefinite. It may be possible to say that there both is and is not a cat in the box.

[![GHZ state](images/ghz-state.svg "An equation for GHZ state in quantum computing")](https://en.wikipedia.org/wiki/Schr%C3%B6dinger%27s_cat)\
*Figure 999.1-2: Equation for Quantum Computing "Cat State" or GHZ State*

### Use a Box Camera

Set up a wireless camera inside the box to continuously monitor for cats inside. This test requires the following steps.

#### 1. Acquire a Camera

The camera must:

1. Fit inside the box.
2. Leave enough room in the box for a cat to also fit in the box.
3. Have the ability to wirelessly display its video feed.

#### 2. Set Up Camera

Mount the camera inside the box using provided hardware, or duct tape. Follow the manufacturer's instructions to set up the camera and make the video feed available. For example, you may be able to view the video feed on your local network at an address beginning with `https://localhost:`.

#### 3. Monitor the Video Feed

Manually view the video feed at periodic intervals to determine if there is a cat in view. Alternatively, use image recognition software to monitor the feed and send an alert if it detects a cat. Here is some tangentially related [TensorFlow code for defining a model](https://www.tensorflow.org/tutorials/images/segmentation#define_the_model):

```py
base_model = tf.keras.applications.MobileNetV2(input_shape=[128, 128, 3], include_top=False)

# Use the activations of these layers
layer_names = [
    'block_1_expand_relu',   # 64x64
    'block_3_expand_relu',   # 32x32
    'block_6_expand_relu',   # 16x16
    'block_13_expand_relu',  # 8x8
    'block_16_project',      # 4x4
]
layers = [base_model.get_layer(name).output for name in layer_names]

# Create the feature extraction model
down_stack = tf.keras.Model(inputs=base_model.input, outputs=layers)

down_stack.trainable = False
```

If you observe a cat on the video feed, it is highly likely that there is a cat in the box.

## Capture Output Including a Cat

Here is some appropriately abbreviated capture output that includes a cat.

```http
 HTTP/1.1 200
 [...]
 <!DOCTYPE html>
 <html lang="en">
     <head>
         <meta charset="UTF-8" />
         <title>Apache Tomcat/10.0.4
 [...]
 ```

## Related Test Cases

- [Template Explanation](2-Template_Explanation.md)
- [Formatting for HTTP Requests and Responses](3-Format_for_HTTP_Request_Response.md)

## Remediation

Do not make a habit of putting cats in boxes. Keep boxes away from cats as much as possible.

## Tools

- The box
- A camera

## References

- [Schrödinger's cat](https://en.wikipedia.org/wiki/Schr%C3%B6dinger%27s_cat)
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
