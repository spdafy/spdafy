# Social Media Redirection Layer

* **Domain:** `share.spdafy.com`
* **Host:** GitHub Pages
* **Stack:** Static HTML5 / JavaScript

## 1. Overview
This repository serves as a middleware layer for external link sharing. It hosts static HTML entry points designed to define specific Open Graph Protocol (OGP) and Twitter Card metadata before redirecting the client to the primary application.

## 2. Problem Statement
The primary content management system (Squarespace 7.1) restricts granular control over social sharing assets (thumbnails, titles) for specific sub-pages. Direct linking often results in generic or improperly cropped preview images on platforms like Facebook, LinkedIn, and X (formerly Twitter).

## 3. Technical Implementation
Each directory in this repository represents a distinct shareable route containing an `index.html` file. The file performs two functions:

1.  **Metadata Declaration:**
    Populates `<meta property="og:image">`, `<meta property="og:title">`, and `<meta name="twitter:card">` tags to ensure the scraping bot indexes the correct asset.

2.  **Client-Side Redirection:**
    Executes a JavaScript redirection to the destination URL immediately upon page load.
    ```javascript
    window.location.replace("[https://www.spdafy.com/target-path](https://www.spdafy.com/target-path)");
    ```

## 4. DNS Configuration
* **Source:** `spdafy.github.io`
* **CNAME Record:** `share` points to `spdafy.github.io`
* **Enforce HTTPS:** Enabled

## 5. Usage
To create a new share link:
1.  Create a new directory with the desired slug (e.g., `/new-campaign`).
2.  Add an `index.html` file.
3.  Configure the OGP tags and the destination URL in the script.
4.  The public link will be: `https://share.spdafy.com/new-campaign`

## 6. Contact
For technical inquiries regarding this infrastructure:
[https://www.spdafy.com](https://www.spdafy.com)
