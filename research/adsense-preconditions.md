# What must be true before AdSense serves on a browser tool page?

Question: what Google requires before AdSense will approve a site and fill an ad on one English page where a person runs an encryption or encoding transform, including any policy that touches encryption, encoding, or security tools, and which of those requirements https://ciphertoolbox.com already fails.

This note does not choose which requirements a product spec should treat as a gate.

Sources are Google AdSense and Google Publisher policy pages, current Next.js documentation, the repo on `master` (`e823aba`), and the HTML served by https://ciphertoolbox.com on 17 November 2026.

## 1. What Google requires for approval and for an ad to fill

### Eligibility

To participate, the publisher needs their own content, that content has to meet the program policies, and the applicant has to be at least 18. A parent or guardian may sign up if the applicant is under 18; payments then go to that adult. The publisher must be able to access the HTML of the site they submit. Hosted products (Blogger, YouTube) follow a different signup path and do not apply to this site. Policies can change, and the publisher is responsible for the current ones. [Eligibility requirements for AdSense](https://support.google.com/adsense/answer/9724?hl=en)

Google describes the content bar, before signup, as unique content that is relevant to visitors. Pages should have clear navigation. Original content has to be the publisher's own, not scraped or copyrighted material copied in from elsewhere. Ads on scraped or copyrighted content are a publisher-policy violation. [Make sure your site's pages are ready for AdSense](https://support.google.com/adsense/answer/7299563?hl=en)

### Why an account is not approved

Google reviews the whole site, not only the signup URL. Common content reasons for disapproval are:

- **Insufficient content.** Too little text, or the site looks under construction. Pages need enough high-quality text for a meaningful visit and for relevant ads. Text should be complete sentences and paragraphs, not only headlines. The site should be built and launched. The ad code has to sit on a live page; a test page that is empty except for the code is not approved.
- **Content quality.** Not enough original content that gives someone a reason to visit. Ad code should not go on auto-generated pages or pages with little or no original content. Affiliate pages have to add their own value.
- **Program-policy violations.**
- **Navigation.** Visitors should be able to move through the site. Redirects, login walls, broken links, excessive pop-ups, and unfinished pages are named problems.
- **Traffic sources.** Ads may not be placed on pages whose traffic comes from paid-to-click programs, unwanted email, or a software application.
- **Unsupported language.** If most of the site is in a language AdSense does not support, the account is not approved.

One AdSense account is allowed per publisher. [Your AdSense account wasn't approved](https://support.google.com/adsense/answer/81904?hl=en)

The supported-language list is a separate page from the ones fetched here. These pages are in English (`<html lang="en">` in `src/app/layout.tsx`, and the live document is English). This note does not mark language as a failure.

### Policies that can block ads after signup

Monetizing with Google ad code requires the [Google Publisher Policies](https://support.google.com/adsense/answer/10502938?hl=en). Failure can mean Google blocks ads on the content, or suspends or terminates the account. The policy groups are content, behavioral, privacy-related, and other requirements.

Content rules that apply to any page, including a tool page:

- Illegal content, and copyright infringement or counterfeit goods.
- **Misleading representation:** content that "misrepresents, misstates, or conceals information about the publisher, the content creator, the purpose of the content, or the content itself," or that falsely implies an affiliation or endorsement.
- Deceptive practices, including enticing users under false pretenses and attempting to steal personal information (phishing is the example).
- **Inventory value:** Google-served ads are not allowed on screens without publisher content or with low-value content, on screens that are under construction, or on screens used only for alerts, navigation, or other behavioral purposes. Ads are also disallowed on screens that only embed or copy someone else's content without added value, and on screens with more ads or paid promotion than publisher content.

Other requirements on the same page:

- Do not place Google-served ads on screens that violate Google Search spam policies, that contain abusive experiences, or that do not meet the Better Ads Standards.
- **Malware or unwanted software:** do not place ads on screens that contain malware (viruses, ransomware, spyware, and similar) or that violate Google's Unwanted Software policy.
- **Authorized inventory:** do not place Google-served ads on a domain that uses `ads.txt` unless the publisher is listed there as an authorized seller.
- Publisher products are unavailable in listed sanctioned regions (Crimea, Cuba, the so-called Donetsk and Luhansk People's Republics, Iran, North Korea) and to restricted parties.

### Privacy disclosures and consent

Google's required-content page says Google uses cookies to serve ads on partner sites, and that a cookie may be dropped in the visitor's browser. The site's privacy policy should say that third-party vendors, including Google, use cookies to serve ads based on prior visits; that those cookies let Google and its partners serve ads based on visits to this site and other sites; and that users may opt out of personalized advertising in Ads Settings. [Required content](https://support.google.com/adsense/answer/1348695?hl=en)

For people in the EEA, the UK, and Switzerland, Google's EU user consent policy requires disclosures, and consent for cookies or other local storage where the law requires it, and for the collection, sharing, and use of personal data for ads personalization. Privacy & messaging (Google's CMP) or another certified CMP is how AdSense walks publishers through that message. [About European regulations messages](https://support.google.com/adsense/answer/10961068?hl=en)

### What has to be true before an ad is allowed to show

Ads cannot show until the site has been approved. Connecting the site is part of activation. Google reviews the whole site against the program policies. The review usually takes a few days and can take 2–4 weeks. The publisher also needs payment information on the account. [Connect your site to AdSense](https://support.google.com/adsense/answer/7584263?hl=en)

That page gives three ways to connect:

1. **AdSense code snippet**, pasted in the HTML between `<head>` and `</head>`, on every page where ads should appear.
2. **`ads.txt` snippet**, uploaded at the site root.
3. **Meta tag** `google-adsense-account`, also between `<head>` and `</head>`.

After that, the publisher confirms and clicks Request review. The same flow asks for a CMP choice (Google's, which can create a European regulations message, or a certified third party).

Connection fails if the code is missing or incomplete, not between the head tags, not on the signup site, or not on a page that has content and regular visitors. It also fails if the site is down, behind a login, or if `robots.txt` blocks the AdSense crawler.

For the ad itself, Auto ads need the AdSense code only. An ad unit needs the AdSense code **and** the ad unit code. The Auto ads snippet is pasted between the head tags. The ad unit code is pasted into the page HTML. [Get and copy the AdSense code](https://support.google.com/adsense/answer/9274019?hl=en)

`ads.txt` is not mandatory. If the file exists, the publisher ID has to be in it and formatted as the IAB spec requires, or AdSense can show the site as unauthorized. When `ads.txt` status is Authorized, the site status is Ready, and ads are set up, "ads will start to show," sometimes after up to an hour. [Ads.txt guide](https://support.google.com/adsense/answer/7532444?hl=en)

Publishers must follow the program policies or Google may refuse to display the ads. [How AdSense works](https://support.google.com/adsense/answer/6242051?hl=en)

Nothing fetched here says an approved, policy-clean page with a correct ad unit is guaranteed a filled impression on every request. The documented gates before serving is allowed are eligibility, policy compliance, a connected and approved site, the ad code actually present in the page, the privacy disclosures above, and EEA/UK/Switzerland consent where that policy applies. If the domain publishes `ads.txt`, the publisher must be an authorized seller.

## 2. Policies that touch encryption, encoding, ciphers, or security tools

The publisher-policy page does **not** mention encryption, encoding, ciphers, hashing, or security-tool pages. Neither do the eligibility, page-readiness, disapproval, required-content, EU-consent, site-connection, ad-code, or `ads.txt` pages fetched above.

The closest content rule is under **Enabling dishonest behavior**. Google does not allow content that "promotes any form of hacking or cracking and/or provides users with instructions, equipment, or software that tampers with or provides unauthorized access to devices, software, servers, or websites." The examples on that page are illegal access to phones and other communications or content-delivery systems, bypassing copyright protection and DRM, illegally descrambling cable or satellite signals, and helping people download streaming video when the provider prohibits it. A separate bullet bans covert tracking or monitoring of another person (spyware and surveillance marketed for spying). [Google Publisher Policies](https://support.google.com/adsense/answer/10502938?hl=en)

The malware rule is about screens that contain malicious software, not about pages that explain or run AES, RSA, a Caesar shift, or Base64.

Those examples do not describe a page that encrypts or encodes text the visitor pastes. This note does not treat the cipher tools as a violation of that clause. There is no fetched rule that says an encryption or encoding utility is ineligible for AdSense.

## 3. What this repo and the live site already fail

Checked against the requirements above. Account age, payment profile, and whether Google has approved `ca-pub-9131623089140541` are not visible in the repo or the public HTML, so they are not marked either way.

### The AdSense loader is not in the served HTML

`src/app/layout.tsx` is an App Router root layout. It imports `Head` from `next/head` and puts this in `<Head>`:

`https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-9131623089140541`

The Pages Router documents `next/head` as the component that appends elements to the page `<head>`, and it tells authors to use `next/script` for scripts rather than a manual `<script>` inside `next/head`. [Head component (Pages Router)](https://nextjs.org/docs/pages/api-reference/components/head)

The App Router migration guide says that in the `app` directory, `next/head` is replaced by the built-in Metadata API. [App Router migration, step 3](https://nextjs.org/docs/app/building-your-application/upgrading/app-router-migration)

The App Router script API is `next/script`. A script with `strategy="beforeInteractive"` in the root layout is injected into the initial HTML `<head>`. [Script component](https://nextjs.org/docs/app/api-reference/components/script)

This layout does not use `next/script` for AdSense. The ad unit is a separate client component, `src/components/ad-space.tsx`: an `<ins class="adsbygoogle">` with `data-ad-client="ca-pub-9131623089140541"` and `data-ad-slot="6333536066"`, plus a `useEffect` that calls `window.adsbygoogle.push({})`. `src/components/calculator-layout.tsx` renders that unit on tool pages (three times). The home page and FAQ render it too.

Live HTML on 17 November 2026:

- `https://ciphertoolbox.com` returned HTTP 200. The body includes two `<ins class="adsbygoogle">` elements with that publisher id and slot. The document `<head>` contains no external script URL. `pagead2.googlesyndication.com` and `adsbygoogle.js` do not appear.
- `https://ciphertoolbox.com/base64-encoding` includes three of the same `<ins>` elements and also has no `adsbygoogle.js` request in the HTML.
- There is no `google-adsense-account` meta tag.
- `https://ciphertoolbox.com/ads.txt` returned HTTP 404.

Google's connection instructions require the AdSense snippet in the `<head>`, or an `ads.txt` line, or the meta tag. None of those three are in the live response. The ad unit markup is present, including on a page where someone runs a Base64 transform, but the loader script those units call is not in the HTML. That fails the documented placement for the AdSense code. `ads.txt` being absent is not itself a policy failure: the guide says `ads.txt` is not mandatory, and the authorized-inventory rule applies when a domain uses `ads.txt`.

### The site misstates what it offers and whether it collects data

Misleading representation forbids misstating the content itself. [Google Publisher Policies](https://support.google.com/adsense/answer/10502938?hl=en)

These claims say the site offers hashing tools:

- Home page: "Professional-grade online encryption, encoding and hashing tools" and "encryption, decryption, hashing, encoding and decoding tools." `src/app/page.tsx`
- About page: "a comprehensive suite of cryptographic tools including hashing, encryption and encoding." `src/app/about/page.tsx`
- Default description: "Free online tools for encryption, encoding and hashing. Securely transform text with AES, Base64, SHA, and more." `src/seo/site-config.ts`

The live homepage `<meta name="description">` is that same sentence, including "hashing" and "SHA".

The implemented tools are AES, RSA, Caesar Cipher, and Base64. `ALL_TOOLS` in `src/constants.tsx` is those four. `src/lib/crypto/` contains `aes.ts`, `rsa.ts`, `caesar.ts`, `base64.ts`, and `index.ts`. Nothing there implements SHA, bcrypt, Argon2, or any other hash. The only `bcrypt` / `Argon2` text in `src/` is an FAQ answer.

The FAQ has a "Hashing" section ("Frequently asked questions about hashing") that explains hash functions and says passwords should be hashed with bcrypt or Argon2. `src/app/faq/page.tsx`. That section does not say the site provides a hash tool and does not link to one. The false product claim is on the home page, the about page, and the site description, not in the FAQ.

The home page also says "No registration, no downloads, no data collection." That sentence is in the live homepage HTML. The same layout loads Google Analytics:

```tsx
<GoogleAnalytics gaId="G-N8EBZH5YE6" />
```

`src/app/layout.tsx`. Next.js documents `GoogleAnalytics` as including Google Analytics 4 through `gtag.js`, fetched after hydration, and as automatically sending pageview data, including on client-side route changes. [Third-party libraries, Google Analytics](https://nextjs.org/docs/app/building-your-application/optimizing/third-party-libraries)

The live homepage `<head>` preloads `https://www.googletagmanager.com/gtag/js?id=G-N8EBZH5YE6`, and the page payload includes `gaId` `G-N8EBZH5YE6`. The initial HTML does not contain the `gtag.js` `<script>` itself, which matches the "after hydration" behavior in those docs.

AdSense's required-content page says Google uses cookies to serve ads and may drop a cookie on the partner site. [Required content](https://support.google.com/adsense/answer/1348695?hl=en). The live pages already render the ad units.

"No data collection" misstates the page. The layout is built to load Google Analytics, which Next.js documents as sending pageview data, and to render AdSense units, which Google documents as using cookies.

Related copy the implementation does not carry out: the home page says "We never store your data. All information used in our tools will be deleted after the operation is completed." The about page says "Your data will always be deleted after the operation is completed." The transforms are server functions. Each of `src/lib/crypto/aes.ts`, `rsa.ts`, `caesar.ts`, and `base64.ts` begins with `"use server"`. Client components pass the visitor's text in as an argument, for example `cryptoRouter.base64.encode(data.inputText)` in `src/app/[tool]/_components/base64/base64-encoding.tsx` (`"use client"`). The same pattern is in the AES, RSA, and Caesar encrypt/decrypt components. Next.js says a server function runs on the server and is called from the client through a network request, and that actions use POST. [Server Actions and Mutations](https://nextjs.org/docs/app/building-your-application/data-fetching/server-actions-and-mutations)

So the plaintext leaves the browser. Those four modules do not write it to a database, and they also contain no deletion step. The "deleted after the operation" sentence describes a step the code does not implement. No AdSense page fetched here requires the transform to run in the browser. The relevant policy is the ban on misstating the content, which this privacy copy does.

One narrower misstatement on the home page: `TOOL_INFO` groups Caesar with AES and RSA under "modern cryptographic algorithms" that help "protect sensitive information." `CAESAR_TOOL` itself is "Classical Shift Cipher" with "shift operations." `src/constants.tsx`. The publisher policy does not define Caesar. The page's own labels disagree about what that tool is.

### There is no privacy policy with the disclosures Google lists

The required-content page says the privacy policy should include the Google advertising-cookie disclosures linked above. The repo has no privacy route. `src/app/` pages are the home page, about, FAQ, and `[tool]`. The footer links About and FAQ only (`src/app/_components/footer.tsx`). `src/app/robots.ts` disallows `/privacy` and `/terms`, but those routes do not exist. `https://ciphertoolbox.com/privacy` returned HTTP 404 on 17 November 2026. There is no privacy policy on the site that can carry the disclosures Google asks for.

### EEA, UK, and Switzerland consent is not in the HTML

The fetched homepage and Base64 page contain no Funding Choices or European-regulations markup. The site-connection flow treats a CMP choice as part of requesting review, and the EU user consent policy requires that consent in the EEA, the UK, and Switzerland. [Connect your site to AdSense](https://support.google.com/adsense/answer/7584263?hl=en), [About European regulations messages](https://support.google.com/adsense/answer/10961068?hl=en). That gap is regional. It is not, on these pages, a requirement for every country. The AdSense loader that often brings a CMP along is also missing, so this HTML cannot show a CMP that would have been injected by that script.

### Not marked as failures

- **Encryption and encoding as a category.** No fetched policy mentions them. The hacking-and-cracking examples do not describe AES, RSA, Caesar, or Base64 on text the visitor supplies. `src/lib/crypto/caesar.ts` `bruteForce` tries shifts 1 through 26 on that text. That is not one of the unauthorized-access examples.
- **Malware.** The pages are transform forms, not software that infects a device.
- **Insufficient or low-value content as a demonstrated rejection.** Google decides that in review. The home page, about page, and FAQ contain paragraphs, and tool pages render a calculator plus a learning section (`learning` in `src/components/calculator-layout.tsx`). They are not an empty test page or an under-construction shell, which are the cases the disapproval article names. This note does not call the content bar failed or passed.
- **`ads.txt` 404**, for the reason above. It does mean the `ads.txt` connection method is unused.
- **Language, age, payments, and account approval status.** Not established from these sources.
