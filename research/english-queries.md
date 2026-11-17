# English queries for a named transform

Checked 16 November 2026. Search volume is unknown. Nothing below is a recommendation about which page to build. The question is who already occupies the first Google page, and whether that page leaves a capability a new browser-only page could fill.

## How this was checked

Each query was loaded in Google with `hl=en`, `gl=us`, `pws=0`, and `num=10`, after rejecting the cookie dialog. The results footer said the location could not be determined. Order below is the order of the web-result headings on that page. An AI Overview, People also ask, and sometimes Things to know also sat on the page. Those are Google features, not sites, and they are not given a rank.

`ciphertoolbox.com` did not appear in the visible text of any of the seven result pages.

"Runs in the browser" is used only when the page says so, or when the fetched HTML shows the work happening in the page (a local script, `crypto.subtle`, and no form that posts the input). A Next.js bundle that was not read is described as unresolved. Pages that were not opened are marked as snippet only, and the only source for them is the Google result.

## `base64 encode`

Search: <https://www.google.com/search?q=base64+encode&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. An AI Overview sat between the fourth and fifth results. People also ask sat after Wikipedia.

1. [Base64 Encode and Decode - Online](https://www.base64encode.org/). The text form is `method="post"` to `https://www.base64encode.org/`. A separate file form uploads the file to the same host. The page also offers an optional live mode: "the encoding happens in your browser as you type, re-running on every keystroke with nothing sent to our servers," and that mode "works with UTF-8 only." Below the widget is an explanation of character sets, newlines, and URL-safe Base64, plus a character table. The page says uploaded files are deleted after processing, and that with live mode on the text never leaves the browser.
2. [Base64 Encode - Online Tool](https://www.base64encode.net/). The form is `method="post"` to `/`. The page has ads, a short explanation, the RFC 4648 alphabet table, and links to image, file, PDF, and Base32 tools plus language snippets. The decode control links to a sister host, `base64decode.net`. Nothing on the page says the conversion stays in the browser.
3. [Base64](https://en.wikipedia.org/wiki/Base64). Encyclopedia article: applications, alphabet, examples, and variants. No encoder widget. Opened.
4. [Base64 Encode - Online Tools](https://emn178.github.io/online-tools/base64_encode.html). Static page. The conversion is loaded from local scripts (`js/base64.js`, `js/base64.min.js`). There is no form POST. Controls cover input encoding and format: RFC 4648, URL-safe, MIME, UTF-7, IMAP, and a custom alphabet. The page has an FAQ (Base64 is not encryption), ads, and a share-link field wired to the input.
5. [Base64 encoder/decoder](https://openreplay.com/tools/base64/). The page says: "Encode and decode text with Base64. Processed locally, nothing leaves your browser." It also says Base64 is not encryption. Text only, from the copy on the page.
6. [Base64 - Glossary](https://developer.mozilla.org/en-US/docs/Glossary/Base64). MDN glossary entry. It documents the encoding and the browser `btoa` / `atob` functions. It is not a paste-in tool. Opened.
7. [Base64 Encoder & Decoder, Explained](https://logto.io/base64-decoder). The page says: "Encoding and decoding run entirely in your browser. Nothing you paste is uploaded or logged." The rest of the page is an explanation of the alphabet, padding, and the URL-safe variant, on a site that also sells authentication.
8. [base64 — Base16, Base32, Base64, Base85 Data Encodings](https://docs.python.org/3/library/base64.html). Python standard-library reference. The only forms are documentation search. Opened.
9. [Base64 Encoder and Decoder](https://www.64baser.com/). The page offers text and file encode and decode, and says text is converted to UTF-8 bytes before encoding. There is no HTML form. The converter is a Next.js app. The bundle was not read, so this note cannot show whether a file is uploaded.

Gap: there is no empty slot for a browser text encoder. Results 4, 5, and 7 already encode in the browser, and result 4 already covers the usual alphabets. Result 1 already covers files, character sets, and URL-safe output, but its default path and its file form send the data to the server, and its browser mode is optional and UTF-8 only. A new page would be another text encoder beside ones that already exist on this page. Whether any first-page file encoder keeps the file bytes on the device was not established, because result 9's bundle was not read.

## `base64 decode`

Search: <https://www.google.com/search?q=base64+decode&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. This is not the same list as encode. The encode winner's host is gone, and a sister host is first. An AI Overview sat after the fourth result.

1. [Base64 Decode and Encode - Online](https://www.base64decode.org/). Same family as `base64encode.org`. The text form is `method="post"` to `https://www.base64decode.org/`. The page describes the same optional in-browser live mode and the same file-upload form. Opened.
2. [Base64 Decode](https://emn178.github.io/online-tools/base64_decode.html). The decode half of result 4 above. Static page, local script, no form POST. The Google snippet describes standard and URL-safe alphabets.
3. [Base64 encoder/decoder](https://openreplay.com/tools/base64/). Same local text tool as on the encode page.
4. [Base64 Decode and Encode](https://www.authgear.com/tools/base64-decode-encode/). The page says "100% Client-Side" and "No data is sent to any server. Everything runs safely within your browser." It offers a charset list (UTF-8, ASCII, ISO-8859 variants, and others). The surrounding site is an authentication product.
5. [base64 — Python](https://docs.python.org/3/library/base64.html). Same library page as on the encode query.
6. [Base64 Encoder and Decoder](https://www.64baser.com/). Same unresolved Next.js file-and-text tool.
7. [Base64 Encoder/Decoder](https://jam.dev/utilities/base-64-encoder). The visible copy says to paste text and convert, with no sign-up, and the page is labeled free, open source, and ad-free. There is no HTML form. The converter is a Next.js bundle that was not read, so this note cannot show whether the string stays in the browser.
8. [Base64 - Glossary](https://developer.mozilla.org/en-US/docs/Glossary/Base64). Same MDN glossary entry.
9. [Base64URL Decode](https://base64.guru/standards/base64url/decode). A decoder for the Base64URL variant, not a general Base64 page. The form is `method="post"` to `/standards/base64url/decode`. The site is a large Base64 catalog (files, images, hex, and language examples).

Gap: none that is visible. Decode-in-the-browser is already on the page (results 2, 3, and 4). The encode and decode queries do rank different URLs, but several of those URLs are already a single page that does both directions. Result 9 is a posted Base64URL form, which is a variant, not a missing standard decoder.

## `aes encrypt`

Search: <https://www.google.com/search?q=aes+encrypt&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. An AI Overview sat above the web results. People also ask sat after the third result.

1. [AES Encryption and Decryption Online](https://www.devglan.com/online-tools/aes-encryption-decryption). The page says it supports ECB, CBC, CTR, and GCM, with AES-256-GCM described as the recommended choice, and 128, 192, and 256-bit keys. It also says: "Text, keys and IVs are sent to the DevGlan server for processing." The forms use `@submit.prevent`, so the browser does not do a normal full-page post, but the page's own text says the server does the cryptography. There is a PayPal donate form that is unrelated to the cipher.
2. [AES Crypt](https://www.aescrypt.com/). Downloadable file-encryption software for Windows, Mac, Android, iOS, Linux, and BSD. Not a browser widget. Opened.
3. [AES Encryption](https://emn178.github.io/online-tools/aes/encrypt/). Static page. It says the tool supports AES-128, AES-192, and AES-256, with text, a local file, or a URL, and modes CBC, CTR, CFB, OFB, ECB, GCM, or CCM. A file drop zone says: "It will process locally and won't be uploaded." PBKDF2 is present in the page. No form POST.
4. YouTube, Skill Foundry, "AES Encryption in Action: Encrypt & Decrypt Data in C#", 18:54, "1 year ago." Not opened. The snippet calls it a walkthrough of AES in C#. The watch URL was not in the cite text. Snippet only.
5. [Advanced Encryption Standard](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard). The URL returned that title. The article body was not read. Google's snippet describes it as the AES specification.
6. [AES Encrypt / Decrypt](https://www.w3schools.com/tools/tool_aes_encrypt.php). The page says: "Encrypt and decrypt text securely in your browser using AES-256-GCM with a password-derived key. Runs entirely in your browser." The HTML includes `crypto.subtle`. One mode and a password, not a choice of key size or cipher mode.
7. [Aes Class (System.Security.Cryptography)](https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.aes). .NET API reference for the `Aes` class. Not a tool. The fetched page also showed an authorization notice, and it still included the class definition. Opened.
8. [Online AES Encryption / Decryption](https://anycript.com/crypto). Google's snippet was "No information is available for this page." A direct fetch returned a page whose title was "Redirecting..." and whose body was "Loading." What the tool does was not observable.
9. [What Is AES Encryption And How Does It Work?](https://www.jscape.com/blog/aes-encryption). A JSCAPE blog post explaining AES and its use for files in transit. No encryptor widget. Opened.

Gap: not an empty encryptor. A browser tool with several modes and local file handling is already result 3, and a narrower browser tool (password, AES-256-GCM only) is result 6. The result in position 1 does send the text and the key to a server. The pages that were opened do not describe one shared output: result 3 asks the user to set mode, key, and IV; result 6 derives a key from a password and uses GCM only. That mismatch is the concrete failure, and it is sharper on the decrypt query.

## `aes decrypt`

Search: <https://www.google.com/search?q=aes+decrypt&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. An AI Overview sat between the second and third results. Wikipedia, the Microsoft API page, the JSCAPE post, and the AES Crypt product homepage are not on this page. A Reddit thread and a source repository are.

1. [AES Encryption and Decryption Online](https://www.devglan.com/online-tools/aes-encryption-decryption). Same server-side tool as above. The decrypt snippet adds: "Configure keys, IVs, and encryption."
2. [AES Decryption](https://emn178.github.io/online-tools/aes/decrypt/). The decrypt half of the emn178 tool. Same static host. The snippet says it reverses AES with the same key and compatible parameters, for AES-128, AES-192, and AES-256.
3. [AES encryption – Encrypt & decrypt text](https://openreplay.com/tools/aes-encryption/). The page says: "Encrypt and decrypt text with AES (GCM or CBC, 128 or 256-bit) using a passphrase, in your browser. Keys are derived with PBKDF2; nothing is uploaded." Further down: "AES-CBC is offered for interoperability with systems that expect it. All cryptography runs locally via the Web Crypto API, so your text and passphrase never leave the page." That interoperability sentence is about offering CBC, not about a labeled file format.
4. [AES Encrypt / Decrypt](https://www.w3schools.com/tools/tool_aes_encrypt.php). Same browser AES-256-GCM password tool.
5. [Online AES Encryption / Decryption](https://anycript.com/crypto). Same unavailable page as on the encrypt query.
6. "How to reliably encrypt and decrypt using AES-256", Reddit, r/cryptography. Not opened. Google's snippet says: "I want to encrypt some text using AES-256, then decrypt it again, but using a different program/software. The problem is, all of the AES-256 ..." and a related line in the AI Overview's source card says online AES-256 tools often produce incompatible ciphertext because they use different parameters. The full thread URL was not in the cite. Snippet only, from the search above.
7. [kiro6/AES-encryption-decryption-tool](https://github.com/kiro6/AES-encryption-decryption-tool). The README describes a Python command-line tool for files (`python3 aes.py`), ECB mode, with a hex key of 32, 48, or 64 characters. It is not a browser page. The README's example key is not repeated here.
8. [aes256 encrypt & decrypt online](https://encode-decode.com/aes256-encrypt-online/). The form is `method="post"` and is named `encryption`. The page is a menu of cipher names, including `aes-256-cbc`, `aes-256-gcm`, `aes-256-ctr`, `aes-256-ecb`, and many others, plus non-AES ciphers. The string is submitted.
9. [AES Crypt on Windows](https://www.aescrypt.com/windows_aes_crypt.html). Instructions for the desktop program: a file dialog, a password dialog, and output written next to the original file with a `.aes` extension when encrypting. Not a browser decryptor. The product homepage is <https://www.aescrypt.com/>.

Gap: the missing thing is not a browser decryptor. Results 2, 3, and 4 already decrypt in the browser, and they do it under different contracts (explicit key and mode, passphrase with PBKDF2 and GCM or CBC, password and GCM only). Result 1 decrypts on a server. Result 8 posts the string into a long cipher menu. The Reddit snippet on this same page is a person who cannot move AES-256 ciphertext from one program to another. None of the tool pages that were opened hand back one self-describing ciphertext that the others claim to open. That is a gap in what the ranking pages do. It is not evidence that a new domain would be ranked for `aes decrypt`.

## `caesar cipher`

Search: <https://www.google.com/search?q=caesar+cipher&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. People also ask sat after the third result, then an AI Overview. At the bottom Google showed: "Some results may have been removed under data protection law in Europe."

1. [Caesar cipher: Encode and decode online](https://cryptii.com/pipes/caesar-cipher). The page says the app does "modular conversion, encoding, and encryption, all performed directly in your browser with no server interaction," and that the project is open source under the MIT license. It is a pipe for a known shift, not a write-up of the history.
2. [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher). The URL returned that title. The article body was not read. Google's snippet says each letter is replaced by the letter a fixed number of places down the alphabet.
3. [Caesar Cipher (Shift) Translator](https://www.dcode.fr/caesar-cipher). An online decoder and encoder. The decoder form is `method="post"`, the ciphertext field is a textarea, and the button is marked `data-post`. The page offers "Test all possible shifts (26-letter alphabet A-Z)" and a brute-force decrypt, plus a manual shift, ROT13, and instructions for encrypting and decrypting. The form is built to submit the ciphertext. The request itself was not traced.
4. [The Caesar cipher (video)](https://www.khanacademy.org/). Not opened. Google showed a Khan Academy video dated 2 April 2014, 2:36, described as a substitution cipher that shifts letters. The full path was truncated in the cite. Snippet only.
5. [Caesar Cipher Encoder and Decoder](https://raw.org/tool/caesar-cipher). A "classical cryptography" laboratory. The UI is loaded from `/js/caesar-cipher-ui.js`. There is no form POST. The page describes shift controls, an alphabet wheel, ROT13, and English frequency analysis, and it says a brute-force attack can generate every candidate immediately. It also says the cipher must not be used to protect secrets.
6. [The Caesar Cipher, Explained](https://www.splunk.com/en_us/blog/learn/caesar-cipher.html). The URL returned that title. Google's snippet, dated 3 September 2024, calls it one of the simplest and earliest encryption methods. The article body was not read past the title.
7. "Cryptography : The Caesar Cipher", YouTube, Zach's Math Zone, 3:31. Not opened. The snippet says the video shows an encryption example and a decryption example. Snippet only.
8. [Caesar Cipher in Cryptography](https://www.geeksforgeeks.org/). Not opened. Snippet dated 23 July 2025: a substitution cipher used by Julius Caesar. The path was truncated. Snippet only.
9. "Caesar Cipher Lab", University of Texas at Austin. Not opened. Google showed `cs.utexas.edu` and a programming exercise: walk the message, shift letters, build a result of the same length. Snippet only.

Gap: none for a browser page that shifts by a known key, and none for seeing every shift. Result 1 is a browser encoder with no server, and result 5 is a browser page that talks through generating every candidate. Result 3 already brute-forces all 26 shifts, and it submits the ciphertext. Videos and explainers occupy the rest of the page. A new page would be another shifter.

## `rsa encrypt`

Search: <https://www.google.com/search?q=rsa+encrypt&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. An AI Overview sat above the web results. People also ask sat after Wikipedia. Most of the page is explanation. Three results are tools.

1. [RSA Encryption and Decryption Online](https://www.devglan.com/online-tools/rsa-encryption-decryption). The page says it can generate a key pair and encrypt and decrypt, with key sizes from 512 to 4096 bits, OAEP with SHA-256, OAEP with SHA-1, and PKCS#1 v1.5. It also says: "Keys and operations are processed on the DevGlan server; use test data here." Public key is labeled X.509 and private key PKCS#8.
2. [RSA cryptosystem](https://en.wikipedia.org/wiki/RSA_cryptosystem). The URL returned that title. The article body was not read. Google's snippet lists key generation, key distribution, and the public-key operation.
3. [RSA Encryption](https://emn178.github.io/online-tools/rsa/encrypt/). Static page, no form POST. It encrypts with the recipient's public key. The page says it supports PKCS#1 v1.5 and OAEP with SHA-1, SHA-224, SHA-256, or SHA-384, and it states the OAEP message-size limit. The encrypt page that was opened does not generate the key pair. It tells the reader to use a trusted public key.
4. Cohesity, "RSA Encryption." Not opened. A fetch of the glossary path Google's cite suggested returned 403, so the page itself was not read. Google's snippet, dated 7 October 2026, defines encrypting with a public key. Snippet only. The cite was `cohesity.com › glossary › rsa-encryption`.
5. [RSA](https://cryptography.io/en/latest/hazmat/primitives/asymmetric/rsa/). pyca/cryptography documentation. The opened page is an API reference: key generation, loading, serialization, signing, verification, encryption, decryption, and padding. Not a browser tool. Google's snippet says the public key encrypts and the private key decrypts.
6. "RSA Algorithm - How does it work? - I'll PROVE it with an Example!", YouTube, Practical Networking, 15:48, "5 years ago." Not opened. A math example of generating keys and encrypting with the public key. Snippet only.
7. [RSA Encryption Tool - Generate Keys & Encrypt/Decrypt](https://www.toolkitpub.com/tools/rsa-encrypt-decrypt). The HTML includes a "Generate RSA public/private key pair" control and a Generate Keys button. A feature list on the page says "Client-side processing ensuring data privacy and security." The script that runs on that button was not read, so the client-side claim is the page's own statement, not a traced request.
8. Splunk, "RSA Algorithm in Cryptography: Rivest Shamir Adleman ..." Not opened. The cite was truncated after `splunk.com › en_us › blog › learn › rsa-al`. Google's snippet, dated 26 November 2024, is an explainer of RSA. Snippet only.
9. American Mathematical Society blogs, "RSA Encryption – Keeping the Internet Secure." Not opened. The cite was `blogs.ams.org › mathgradblog › 2014/03/30 › rsa`, and a fetch of one guessed path timed out, so the page was not read. Google's snippet is dated 30 March 2014. Snippet only.

Gap: no empty browser tool was visible. Result 1 already generates keys and encrypts, and it tells the reader not to use real keys because the server sees them. Result 3 already encrypts in the page from a public key, with the paddings a caller has to match. Result 7 already claims in-page key generation. The rest of the page explains RSA rather than running it. A new page would be another RSA widget next to those three.

## `SHA-256`

Search: <https://www.google.com/search?q=SHA-256&hl=en&gl=us&pws=0&num=10>

`ciphertoolbox.com` was absent. An AI Overview sat above the web results. People also ask sat after the first result. This query returns definitions more than calculators. People also search for "SHA-256 decrypt"; the AI Overview's text says the function cannot be reversed. That overview is Google's, not a ranking site.

1. [SHA256 - Online Tools](https://emn178.github.io/online-tools/sha256.html). Static calculator on the same host as the other emn178 tools. The fetched HTML has no form. The description says it calculates SHA-256 or HMAC-SHA-256 for text, with UTF-8, UTF-16, hex, Base64, and other input encodings. The page was not executed.
2. [SHA-256 Cryptographic Hash Algorithm](https://www.movable-type.co.uk/scripts/sha256.html). The title is "SHA-256 Cryptographic Hash Algorithm implemented in JavaScript." The hash form is `<form name="f">` with no `method="post"`. A separate PayPal donate form does post, and it is not the hasher. Opened.
3. [SHA-2](https://en.wikipedia.org/wiki/SHA-2). The URL returned that title. The article body was not read. Google's snippet mentions SHA-256 for Debian packages and DKIM, and SHA-512 for archival video.
4. Encryption Consulting, "What is SHA-256?" Not opened. The cite was truncated after `encryptionconsulting.com › education-center`. A guessed path under that prefix returned 404. Google's snippet, dated 24 July 2026, calls it a SHA-2 hash with a 256-bit digest. Snippet only.
5. [SHA-256](https://csrc.nist.gov/glossary/term/sha_256). The URL responded with a page that said JavaScript was required and that the view was an unauthorized frame, so the glossary body was not in the fetch. Google's snippet, from the NIST Computer Security Resource Center, defines it as a hash algorithm whose digests show whether a message has changed.
6. "Trouble understanding something about sha256", Reddit, r/algorithms, "2 years ago." Not opened. The snippet contrasts SHA-256 with encryption: you run an input through the hash. Snippet only.
7. "How does SHA-256 work? (full explanation)", YouTube, Boot dev, 19:24, "3 years ago." Not opened. Snippet only.
8. [Generate SHA256 Hash](https://tools.keycdn.com/sha256-online-generator). The form is `method="post"`. The textarea is named `value`. The page says it generates a SHA-256 hash of a string. The string is submitted.
9. N-able, "SHA-256 Algorithm Overview." Not opened. The cite was truncated under `n-able.com › Blog › Security`. A guessed blog path returned 403. Google's snippet calls SHA-256 a hashing function and mentions US government use. Snippet only.

Gap: none for a browser hasher. Result 1 is already a static calculator with no form posting the input, and result 2 is a JavaScript implementation with an in-page form. Result 8 is a hasher that does send the string to a server. The rest of the page explains a one-way function. A new page that only computes SHA-256 would repeat result 1.

## Across the seven queries

Browser-only pages are already on the first page for every family that was checked:

- Base64 text: [emn178](https://emn178.github.io/online-tools/base64_encode.html), [OpenReplay](https://openreplay.com/tools/base64/), [Logto](https://logto.io/base64-decoder), [Authgear](https://www.authgear.com/tools/base64-decode-encode/).
- AES: [emn178](https://emn178.github.io/online-tools/aes/encrypt/) (several modes, local files), [W3Schools](https://www.w3schools.com/tools/tool_aes_encrypt.php) (AES-256-GCM and a password), [OpenReplay](https://openreplay.com/tools/aes-encryption/) (passphrase, PBKDF2, GCM or CBC).
- Caesar: [Cryptii](https://cryptii.com/pipes/caesar-cipher) and [raw.org](https://raw.org/tool/caesar-cipher).
- RSA: [emn178](https://emn178.github.io/online-tools/rsa/encrypt/) encrypts from a public key in the page. [toolkitpub](https://www.toolkitpub.com/tools/rsa-encrypt-decrypt) claims client-side key generation; that script was not traced.
- SHA-256: [emn178](https://emn178.github.io/online-tools/sha256.html) and the [movable-type JavaScript implementation](https://www.movable-type.co.uk/scripts/sha256.html).

The first result is often still a server. `base64encode.org` and `base64decode.org` post by default. DevGlan's AES page sends the text, key, and IV to its server, and its RSA page says to use test data for the same reason. KeyCDN posts the string to be hashed. dCode's Caesar form is `method="post"`.

Encode and decrypt are different result lists where both were checked. `base64 encode` and `base64 decode` do not share a winner. `aes encrypt` and `aes decrypt` share DevGlan and emn178, and then diverge: the decrypt page adds OpenReplay, the Reddit incompatibility thread, encode-decode.com, and the AES Crypt Windows instructions, and it drops Wikipedia.

The one visible gap is on AES, and it is not "nobody offers a browser AES tool." The tools on the decrypt page describe different parameters, and the Reddit result is about ciphertext that will not decrypt in a second program. A new page could attach the mode, the IV, and the key derivation to the ciphertext. The ranking pages that were opened do not do that for each other. No such hole showed up for Base64 text, Caesar, RSA, or SHA-256: a browser page for each of those is already on the first page.

`ciphertoolbox.com` was absent from all seven. That says it was not on these result pages on this date. It does not say whether a new URL would enter them.
