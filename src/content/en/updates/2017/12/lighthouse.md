project_path: /web/_project.yaml
book_path: /web/updates/_book.yaml
description: New performance audits, a rehaul of the accessibility score, report UX improvements, and bug fixes.

{# wf_updated_on: 2017-12-12 #}
{# wf_published_on: 2017-12-12 #}
{# wf_tags: lighthouse #}
{# wf_featured_image: /web/progressive-web-apps/images/pwa-lighthouse.png #}
{# wf_featured_snippet: New performance audits, a rehaul of the accessibility score, report UX improvements, and bug fixes. #}
{# wf_blink_components: N/A #}

# Lighthouse 2.6 Updates {: .page-title }

{% include "web/_shared/contributors/vinamratasingal.html" %}
{% include "web/_shared/contributors/brendankenny.html" %}
{% include "web/_shared/contributors/kaycebasques.html" %}

[CDT]: /web/tools/lighthouse/#devtools
[Node]: https://github.com/GoogleChrome/lighthouse#using-programmatically
[CLI]: /web/tools/lighthouse/#cli
[CE]: /web/tools/lighthouse/#extension

Lighthouse 2.6 is out! Highlights include:

* New performance audits.
* A rehaul of the accessibility section score.
* Improvements to the report UX.
* Bug fixes.

See the [release notes][RN] for the full list of new features, changes,
and bug fixes coming to Lighthouse in version 2.6.

[RN]: https://github.com/GoogleChrome/lighthouse/releases/tag/v2.6.0

## How to update to 2.6 {: #update }

* NPM. Run `npm update lighthouse`. Run `npm update lighthouse -g` flag if you installed
  Lighthouse globally.
* Chrome Extension. The extension should automatically update, but you can manually update it
  via `chrome://extensions`.
* DevTools. The Audits panel will be shipping with 2.6 in Chrome 65. You can check what version
  of Chrome you're running via `chrome://version`. Chrome updates to a new version about every
  6 weeks. You can run the latest Chrome code by downloading [Chrome Canary][Canary].

[Canary]: https://www.google.com/chrome/browser/canary.html

## New performance audits {: #perf }

### JavaScript boot-up time is high {: #boot-up }

View a breakdown of the time your page spends parsing, compiling, and executing each script.
JavaScript boot-up time is a hidden but important factor in page load time.

<figure>
  <img src="/web/updates/images/2017/12/bootup.png"
       alt="The \"JavaScript boot-up time is high\" audit"/>
  <figcaption>
    <b>Figure 1</b>. The <b>JavaScript boot-up time is high</b> audit
  </figcaption>
</figure>

### Uses inefficient cache policy on static assets {: #caching }

Make sure that the browser properly caches each of your resources to speed up page load time.

<figure>
  <img src="/web/updates/images/2017/12/cache-policy.png"
       alt="The \"Uses inefficient cache policy on static assets\" audit"/>
  <figcaption>
    <b>Figure 2</b>. The <b>Uses inefficient cache policy on static assets</b> audit
  </figcaption>
</figure>

### Avoids page redirects {: #redirects }

Page redirects add an extra network roundtrip, or two if an extra DNS lookup is required.
Minimize redirects in order to speed up page load time.

<figure>
  <img src="/web/updates/images/2017/12/cache-policy.png"
       alt="The \"Uses inefficient cache policy on static assets\" audit"/>
  <figcaption>
    <b>Figure 2</b>. The <b>Uses inefficient cache policy on static assets</b> audit
  </figcaption>
</figure>

## Rehaul of the accessibility section score {: #accessibility }

In Lighthouse 2.6, the aggregate accessibility score is calculated differently. The score weighs
each accessibility audit based on the severity of its impact on user experience, as well as the
frequency of the issue, based on the [HTTP Archive](http://httparchive.org/) dataset. See
[googlechrome/lighthouse/issues/3444](https://github.com/GoogleChrome/lighthouse/issues/3444)
for an in-depth discussion.

## Report UX Improvements {: #report-ux }

### Top-level errors {: #errors }

### Print summary and expanded view {: #print }
