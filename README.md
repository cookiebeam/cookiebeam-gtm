# CookieBeam Consent Mode v2 Template for Google Tag Manager

This repository contains the Google Tag Manager (GTM) template for CookieBeam.

With this template you can integrate CookieBeam's consent management platform with Google Tag Manager. It sets Google Consent Mode v2 defaults, restores returning visitors' stored consent for GDPR, CCPA, LGPD and other privacy regulations, and loads the CookieBeam banner.

## About CookieBeam

CookieBeam is a Google-certified consent management platform (CMP). This template sets Consent Mode v2 defaults and restores stored consent choices for Google Analytics and Google Ads tags. It identifies CookieBeam to Google tags with its developer ID, so Google can tell which CMP set the consent signals on your site. No extra configuration is needed.

## Features

-   **Google Consent Mode v2:** Sets consent defaults and sends `ad_storage`, `analytics_storage`, `ad_user_data`, and `ad_personalization` signals.
-   **Stored consent restore:** When a returning visitor has a stored choice, restores it before any queued Google tag fires.
-   **Regional defaults:** Configure consent defaults for different regions (e.g., EEA vs. US). EU, EEA and UK expand to ISO country codes automatically.
-   **Microsoft UET consent default:** Queues an ad_storage default to UET from the regional defaults table so the first hit carries a consent state. The banner sends the visitor's actual choice when it loads.
-   **Microsoft Clarity consent default:** Queues ad_storage and analytics_storage defaults to Clarity from the regional defaults table so no cookies are set before the visitor's choice is known. The banner sends the visitor's actual choice when it loads.
-   **Developer ID:** When Consent Mode is enabled, the template identifies CookieBeam to Google tags with its registered developer ID.
-   **Environment support:** Load the banner from a non-production environment for testing.

## Regulations and frameworks

CookieBeam banners are designed to help you comply with GDPR, UK GDPR, the ePrivacy Directive, CCPA/CPRA, LGPD and PIPEDA. This template connects those banners to Google tags through Consent Mode v2.

Supported frameworks and signals:

-   **IAB TCF v2.4** for websites
-   **IAB GPP** for US state privacy laws
-   **Global Privacy Control (GPC)**
-   **Microsoft UET and Clarity consent defaults**, set by this template; the banner sends the visitor's actual choice
-   **Google Consent Mode v2**, set by this template

## Implementation Guide

1.  Create a **CookieBeam** account if you haven't already.
2.  Get your **Banner ID** from the CookieBeam dashboard.
3.  In Google Tag Manager, search for "CookieBeam" in the Community Template Gallery or import this template manually.
4.  Create a new tag using this template.
5.  Set the trigger to **Consent Initialization - All Pages**.

## Documentation

For a step-by-step setup guide, visit [GTM Integration](https://cookiebeam.com/guides/gtm-integration).

## Support

For bug reports and feature requests, open an issue on [GitHub](https://github.com/cookiebeam/cookiebeam-gtm/issues).

## Repository Structure

-   `template.tpl`: The GTM template definition.
-   `metadata.yaml`: Version history and metadata for the GTM Gallery.
-   `LICENSE`: Apache 2.0 License.

## License

Licensed under the Apache License, Version 2.0.
