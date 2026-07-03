# OpenAI ChatGPT Ads Configuration GTM Tag Template by [Backona](https://backona.com)

Google Tag Manager template to initialize the [OpenAI Ads Measurement Pixel](https://developers.openai.com/ads/measurement-pixel) (`oaiq`) for ChatGPT ad conversion tracking. Built by [Backona](https://backona.com).

Release history: [CHANGELOG.md](./CHANGELOG.md).

This repository publishes **OpenAI ChatGPT Ads Configuration**, the first step in a small template family:

| Template | Status | Purpose |
|----------|--------|---------|
| **OpenAI ChatGPT Ads Configuration** | Available | Load the SDK, run `oaiq('init', …)`, and optionally pass user data for matching |
| [OpenAI ChatGPT Ads Event](https://github.com/backona/gtm-openai-gpt-ads-event) | Available | Send `oaiq('measure', …)` conversion events |

## Install

1. Open the [Community Template Gallery](https://tagmanager.google.com/gallery) in Google Tag Manager and add **OpenAI ChatGPT Ads Configuration**, or import this repository’s template export.
2. Create a tag using the template.
3. Enter your **Pixel ID** from OpenAI Ads Manager → Conversions ([JavaScript Pixel docs](https://developers.openai.com/ads/measurement-pixel)).
4. Optional: expand **User data (Optional)** to pass email, external ID, country, city, or ZIP on init for conversion matching ([Send user data](https://developers.openai.com/ads/measurement-pixel#send-user-data)). For email and external ID, choose **Plain - hash in template** or **SHA-256 (pre-hashed)**.
5. Optional: turn on **Debug mode** while you test (logs SDK activity in the browser console).
6. Set the trigger to **Consent Initialization - All Pages** so the pixel loads before event tags fire.

## Consent

On each tag, open **Advanced settings → Consent settings** and require these types when using [Consent Mode v2](https://support.google.com/tagmanager/answer/10718549):

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
