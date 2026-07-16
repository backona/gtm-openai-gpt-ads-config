# OpenAI ChatGPT Ads Configuration GTM Tag Template by [Backona](https://backona.com)

Google Tag Manager template to initialize the [OpenAI Ads Measurement Pixel](https://developers.openai.com/ads/measurement-pixel) (`oaiq`) for ChatGPT ad conversion tracking. Built by [Backona](https://backona.com).

Release history: [CHANGELOG.md](./CHANGELOG.md).

This repository publishes **OpenAI ChatGPT Ads Configuration**, the first step in a small template family:

| Template | Purpose |
|----------|---------|
| **OpenAI ChatGPT Ads Configuration** | Load the SDK, run `oaiq('init', …)`, and optionally pass user data for matching |
| [OpenAI ChatGPT Ads Event](https://github.com/backona/gtm-openai-gpt-ads-event) | Send `oaiq('measure', …)` conversion events |

> **Not in the Community Template Gallery yet.** This template has been submitted to Google for gallery listing, but approval can take time. Until it appears in the gallery, install by importing [`template.tpl`](./template.tpl) from this repository (see below). Do not rely on searching the [Community Template Gallery](https://tagmanager.google.com/gallery) for now.

## Install

**Preferred method: import [`template.tpl`](./template.tpl)**

1. In Google Tag Manager, go to **Templates** → **Tag Templates** → **New**.
2. Open the menu (⋮) → **Import** → select [`template.tpl`](./template.tpl) from this repository → **Save**.
3. Create a tag using **OpenAI ChatGPT Ads Configuration**.
4. Enter your **Pixel ID** from OpenAI Ads Manager → Conversions ([JavaScript Pixel docs](https://developers.openai.com/ads/measurement-pixel)).
5. Optional: expand **User data (Optional)** to pass email, external ID, country, city, or ZIP on init for conversion matching ([Send user data](https://developers.openai.com/ads/measurement-pixel#send-user-data)). For email and external ID, choose **Plain (hash it in template)** or **SHA-256 (already pre-hashed)**.
6. Optional: turn on **Debug mode** while you test (logs SDK activity in the browser console).
7. Set the trigger to **Initialization - All Pages** so the pixel loads before event tags fire.

**Later (after Google approval):** you will also be able to add the template from the [Community Template Gallery](https://tagmanager.google.com/gallery). Until then, use the `template.tpl` import above.

## GTM preview

In **Tag Assistant preview/debug mode**, when **Debug mode** is enabled and the configuration tag fires successfully, the preview console logs the resolved `oaiq('init', …)` payload — only fields that were actually sent (pixel ID, debug flag, and user data after hashing). These logs are not written on the live site or when debug mode is off.

## Consent

On each tag, open **Advanced settings → Consent settings** and consider these types when using [Consent Mode v2](https://support.google.com/tagmanager/answer/10718549):

- `ad_storage`
- `ad_user_data`
- `ad_personalization`
- `analytics_storage`

For consent banners and defaults, see [Backona Cookie Consent Management](https://backona.com/product/cookie-consent-management).

## Content Security Policy (CSP)

If the OpenAI GPT Ads script is blocked by CSP, you may see console errors and no events from the pixel. Ask your developer or hosting provider to follow these instructions:

| Directive | Source |
|-----------|--------|
| `script-src` | `https://bzrcdn.openai.com` |
| `connect-src` | `https://bzr.openai.com` |
| `img-src` | `https://bzr.openai.com` |

Details: [OpenAI CSP guidance](https://developers.openai.com/ads/measurement-pixel#configure-a-content-security-policy).

## Support

Report bugs or request features via [GitHub Issues](https://github.com/backona/gtm-openai-gpt-ads-config/issues) on this repository.
