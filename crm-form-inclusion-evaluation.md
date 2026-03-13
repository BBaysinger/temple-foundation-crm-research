# CRM Form Inclusion Evaluation

This document compares the current Temple Foundation CRM shortlist from the perspective of public-facing form implementation.

Scope of comparison:

- donation forms
- event registration forms
- volunteer signup forms
- newsletter / interest capture forms
- membership-related public forms

Important distinction:

- This is about how forms are delivered on the website and how much control Temple Foundation would have over them.
- It is not just a score for "does the CRM have forms."

## Key

- `High`: strong / favorable
- `Medium`: workable with notable constraints
- `Low`: limited / weak
- `Easy`: low setup burden
- `Medium`: moderate setup burden
- `Hard`: higher setup burden
- `Yes`: clearly supported / likely true
- `No`: clearly unsupported / likely false
- `Sometimes`: possible in some flows, plans, or integrations, but not the default first-class path

## 1. Form Evaluation Structure

This table applies the broader evaluation model across the current options.

| CRM option              | Styling freedom | Behavior freedom | Initial setup effort | Ongoing maintenance | Data mapping quality | Workflow / automation depth | Analytics friendliness | Payment flexibility | Website-stack fit | Exit flexibility | Practical read                                                                                          |
| ----------------------- | --------------- | ---------------- | -------------------- | ------------------- | -------------------- | --------------------------- | ---------------------- | ------------------- | ----------------- | ---------------- | ------------------------------------------------------------------------------------------------------- |
| CiviCRM                 | High            | High             | Hard                 | Medium              | High                 | High                        | High                   | High                | High              | High             | Best when Temple wants deep ownership and custom site behavior.                                         |
| Pipedrive               | Low             | Medium           | Hard                 | Medium              | Medium               | Medium                      | Medium                 | Low                 | Medium            | Medium           | Better as CRM backend than as native public-form platform.                                              |
| Zeffy                   | Low-Medium      | Low-Medium       | Easy                 | Easy                | Medium               | Low-Medium                  | Low-Medium             | Medium              | Medium            | Low              | Strong for fast fundraising launch, weaker for custom website experience.                               |
| DonorView               | Medium          | Medium           | Medium               | Medium              | Medium-High          | Medium                      | Medium                 | Medium              | Medium            | Medium           | Practical middle-ground hosted/embed approach without deep frontend control.                            |
| Givebutter              | Medium          | Medium           | Easy                 | Easy-Medium         | Medium               | Medium                      | Medium                 | Medium-High         | Medium            | Low-Medium       | Strong low-friction public fundraising and events, but bounded by platform patterns.                    |
| Bloomerang              | Medium          | Medium           | Easy-Medium          | Easy-Medium         | Medium-High          | Medium                      | Medium                 | Medium              | Medium            | Medium           | Good operational fundraising fit, but frontend control is not its strongest differentiator.             |
| Givebutter + Bloomerang | Medium          | Medium           | Medium               | Medium-Hard         | High                 | Medium-High                 | Medium                 | Medium-High         | Medium            | Medium           | Stronger combined operationally, but system boundaries increase implementation discipline required.     |
| Neon CRM                | Medium          | Medium-High      | Medium               | Medium              | High                 | High                        | Medium                 | Medium-High         | Medium-High       | Medium           | Broad all-in-one coverage with better custom path than most SaaS tools, but still not fully open-ended. |

## 2. Temple-Specific Decision Questions

These are the most decision-relevant questions framed directly against the shortlist.

| CRM option              | Can we make it look truly on-brand without fighting the tool? | Can we control behavior enough for real donation / event / volunteer workflows? | Can a non-developer maintain routine changes? | Does submission land in the CRM cleanly? | Can we track conversions and attribution well? | Does it fit a future custom website architecture? | Is there a credible API-first fallback if widgets become limiting? |
| ----------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------- | ---------------------------------------- | ---------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------ |
| CiviCRM                 | Yes                                                           | Yes                                                                             | Sometimes                                     | Yes                                      | Yes                                            | Yes                                               | Yes                                                                |
| Pipedrive               | No                                                            | Sometimes                                                                       | Sometimes                                     | Sometimes                                | Sometimes                                      | Sometimes                                         | Sometimes                                                          |
| Zeffy                   | Sometimes                                                     | Sometimes                                                                       | Yes                                           | Sometimes                                | Sometimes                                      | Sometimes                                         | No                                                                 |
| DonorView               | Sometimes                                                     | Sometimes                                                                       | Yes                                           | Yes                                      | Sometimes                                      | Sometimes                                         | Sometimes                                                          |
| Givebutter              | Sometimes                                                     | Sometimes                                                                       | Yes                                           | Sometimes                                | Sometimes                                      | Sometimes                                         | Sometimes                                                          |
| Bloomerang              | Sometimes                                                     | Sometimes                                                                       | Yes                                           | Yes                                      | Sometimes                                      | Sometimes                                         | Sometimes                                                          |
| Givebutter + Bloomerang | Sometimes                                                     | Sometimes                                                                       | Sometimes                                     | Yes                                      | Sometimes                                      | Sometimes                                         | Sometimes                                                          |
| Neon CRM                | Sometimes                                                     | Yes                                                                             | Sometimes                                     | Yes                                      | Sometimes                                      | Yes                                               | Sometimes                                                          |

## 3. Specific Form Inclusion Options

This table is the practical form-mode view.

Definitions used here:

- `Hosted page`: vendor-hosted form or campaign page on the CRM / fundraising platform domain or a mapped hosted page path.
- `Iframe embed`: embed a hosted form/page in an iframe.
- `JavaScript widget`: embed with a script snippet; may still be iframe-backed internally.
- `CMS plugin / module`: WordPress, Drupal, or equivalent site integration path.
- `API-first / headless`: Temple builds the frontend and submits through API or integration middleware.
- `Manually authored form`: Temple creates the form markup / UX and handles submission mapping through API, webhook, middleware, or custom backend.

| CRM option              | Hosted pages | Iframe embed | JavaScript widget | CMS plugin / module | API-first / headless | Manually authored custom form path | Multiple practical options?       | Requires vendor site builder? | Practical note                                                                                                            |
| ----------------------- | ------------ | ------------ | ----------------- | ------------------- | -------------------- | ---------------------------------- | --------------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| CiviCRM                 | Yes          | Sometimes    | Sometimes         | Yes                 | Yes                  | Yes                                | Yes                               | No                            | Strongest ownership model; commonly CMS-attached, but not dependent on vendor-hosted site builder.                        |
| Pipedrive               | Sometimes    | Sometimes    | Sometimes         | Sometimes           | Sometimes            | Sometimes                          | Yes, but often via external tools | No                            | Public-facing donation / event / membership forms usually come from adjacent tools rather than Pipedrive itself.          |
| Zeffy                   | Yes          | Yes          | Yes               | No                  | No                   | No                                 | Yes                               | No                            | Hosted fundraising pages and embeddable widgets are the default path; custom frontend ownership is limited.               |
| DonorView               | Yes          | Yes          | Yes               | No                  | Sometimes            | Sometimes                          | Yes                               | No                            | Practical hosted and embedded forms; deeper custom behavior typically needs integration work.                             |
| Givebutter              | Yes          | Yes          | Yes               | No                  | Sometimes            | Sometimes                          | Yes                               | No                            | Gives Temple quick hosted pages and embed tools without requiring a separate site builder.                                |
| Bloomerang              | Yes          | Yes          | Sometimes         | No                  | Sometimes            | Sometimes                          | Yes                               | No                            | Common path is hosted or embedded fundraising forms/pages, not fully custom frontend control.                             |
| Givebutter + Bloomerang | Yes          | Yes          | Yes               | No                  | Sometimes            | Sometimes                          | Yes                               | No                            | In practice Temple would usually use Givebutter for public forms and Bloomerang for CRM/fundraising operations.           |
| Neon CRM                | Yes          | Yes          | Yes               | No                  | Sometimes            | Sometimes                          | Yes                               | No                            | Stronger all-in-one public form coverage than most SaaS CRMs; custom paths exist but are still more bounded than CiviCRM. |

## Practical Summary

- None of the current shortlist options appears to require Temple Foundation to adopt the vendor's own website builder just to publish forms.
- Several platforms strongly encourage their hosted page or widget path as the default easiest route.
- The real dividing line is not "can it embed" but whether Temple can escape the default widget model later without replacing the CRM.
- On that question, `CiviCRM` is the clearest high-control option, `Neon CRM` is the strongest all-in-one SaaS compromise, and `Givebutter` / `Zeffy` are strongest for fast launch with less frontend ownership.

## Notes

- `Pipedrive` is the weakest native fit for nonprofit public-form workflows in this shortlist. It can participate in a working architecture, but usually as the CRM backend rather than the public form layer.
- `Givebutter + Bloomerang` should be read as a combined operating model, not a single native product surface.
- `CiviCRM` is not headless-native in the way some modern API-first products are, but it provides the most credible route here for custom forms, custom portals, and deeper website ownership.
- `Neon CRM` offers one of the stronger built-in combinations of hosted forms/widgets plus broader nonprofit workflow coverage.
