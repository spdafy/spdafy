# SPDAFY Social Redirects

This repository hosts static HTML entry points used to customize Open Graph and Twitter Card metadata for external links.

## Purpose
The primary function of this repository is to resolve thumbnail rendering limitations inherent to the main CMS (Squarespace). By serving a lightweight static page first, we ensure social media platforms (Facebook, X, LinkedIn) scrape the correct specific imagery before redirecting the user to the destination content.

## Functionality
1.  **Metadata Definition:** Explicitly defines `og:image`, `og:title`, and `twitter:card` tags for individual content pieces.
2.  **Client-Side Redirection:** Executes an immediate JavaScript window location change (`window.location.href`) to the target URL on `spdafy.com`.
3.  **Fallback Support:** Includes a standard HTML link for users with JavaScript disabled.

## Usage
These assets are deployed via GitHub Pages to serve as the sharing URL for social media campaigns.

## Contact
For technical inquiries or bug reports, please refer to the official website:
[https://www.spdafy.com](https://www.spdafy.com)
