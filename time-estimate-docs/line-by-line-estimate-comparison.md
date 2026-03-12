# Line-by-Line Estimate Comparison (First Pass)

Date: March 12, 2026  
Source rows: `time-estimate-docs/required-items-difficulty-time-codex.md` and `time-estimate-docs/required-items-difficulty-time-gpt.md`  
Platform feasibility basis: `evaluation-matrix.md` (Pipedrive, Neon CRM, Givebutter + Bloomerang columns)

## Legend

- `0` = natively available with no material extra build effort beyond normal setup
- `days` = rough implementation effort estimate (`8h = 1 day`)
- `X` = not feasible for this line item in current platform shape
- `🔴❓` = unknown first-pass estimate (defer to next pass)

## Easy

| Line Item                  | Codex Estimate | GPT Estimate  | Pipedrive        | Neon CRM                  | Givebutter + Bloomerang |
| -------------------------- | -------------- | ------------- | ---------------- | ------------------------- | ----------------------- |
| Core contact model         | `2-4d`         | `2-4d`        | `0`              | `0`                       | `0`                     |
| Basic data administration  | `1-2d`         | `1-2d`        | `0`              | `0`                       | `0`                     |
| Basic communications setup | `1-2d`         | `1-2d`        | `0`              | `0`                       | `0`                     |
| Basic event setup          | `2-3d`         | `2-3d`        | `X`              | `1-3d`                    | `1-3d`                  |
| Usability baseline         | `1-2d`         | `1-2d`        | `0`              | `🔴❓`                    | `0`                     |
| Budget validation          | `0.5-1d`       | `0.5-1d`      | `1-2d`           | `X`                       | `X`                     |
| **Tier Total**             | **`7.5-14d`**  | **`7.5-14d`** | **`1-2d` + `X`** | **`1-3d` + `🔴❓` + `X`** | **`1-3d` + `X`**        |
| **Cumulative Total**       | **`7.5-14d`**  | **`7.5-14d`** | **`1-2d` + `X`** | **`1-3d` + `🔴❓` + `X`** | **`1-3d` + `X`**        |

## Moderate

| Line Item                           | Codex Estimate | GPT Estimate   | Pipedrive          | Neon CRM                   | Givebutter + Bloomerang |
| ----------------------------------- | -------------- | -------------- | ------------------ | -------------------------- | ----------------------- |
| Donation flow baseline              | `4-7d`         | `4-7d`         | `3-7d`             | `0`                        | `0`                     |
| Campaign and fundraising operations | `3-5d`         | `3-5d`         | `2-5d`             | `0`                        | `0`                     |
| Event automation                    | `3-5d`         | `3-5d`         | `2-5d`             | `0`                        | `0`                     |
| Volunteer and membership baseline   | `4-7d`         | `4-7d`         | `3-7d`             | `2-5d`                     | `3-7d`                  |
| Donor intelligence baseline         | `2-4d`         | `2-4d`         | `1-3d`             | `0`                        | `0`                     |
| Quality and reliability baseline    | `2-4d`         | `2-4d`         | `1-3d`             | `1-3d`                     | `1-3d`                  |
| Embedding path                      | `2-3d`         | `2-3d`         | `1-2d`             | `0`                        | `0`                     |
| **Tier Total**                      | **`20-35d`**   | **`20-35d`**   | **`13-32d`**       | **`3-8d`**                 | **`4-10d`**             |
| **Cumulative Total**                | **`27.5-49d`** | **`27.5-49d`** | **`14-34d` + `X`** | **`4-11d` + `🔴❓` + `X`** | **`5-13d` + `X`**       |

## Hard

| Line Item                  | Codex Estimate  | GPT Estimate    | Pipedrive                      | Neon CRM                       | Givebutter + Bloomerang         |
| -------------------------- | --------------- | --------------- | ------------------------------ | ------------------------------ | ------------------------------- |
| Portal and self-service    | `5-10d`         | `5-10d`         | `🔴❓`                         | `0`                            | `10-25d`                        |
| Fund accounting model      | `10-20d`        | `10-20d`        | `15-40d`                       | `10-25d`                       | `15-40d`                        |
| Volunteer automation depth | `10-20d`        | `10-20d`        | `5-15d`                        | `5-15d`                        | `5-15d`                         |
| Finance integrations       | `10-20d`        | `10-20d`        | `🔴❓`                         | `🔴❓`                         | `🔴❓`                          |
| API integrations           | `5-10d`         | `5-10d`         | `0`                            | `3-10d`                        | `10-25d`                        |
| Operations hardening       | `5-15d`         | `5-15d`         | `0`                            | `1-3d`                         | `1-3d`                          |
| Platform risk controls     | `10-20d`        | `10-20d`        | `2-5d`                         | `1-3d`                         | `X`                             |
| **Tier Total**             | **`55-115d`**   | **`55-115d`**   | **`22-60d` + `2x 🔴❓`**       | **`20-56d` + `🔴❓`**          | **`41-108d` + `🔴❓` + `X`**    |
| **Cumulative Total**       | **`82.5-164d`** | **`82.5-164d`** | **`36-94d` + `2x 🔴❓` + `X`** | **`24-67d` + `2x 🔴❓` + `X`** | **`46-121d` + `🔴❓` + `2x X`** |

## Very Hard

| Line Item                                 | Codex Estimate   | GPT Estimate     | Pipedrive                       | Neon CRM                       | Givebutter + Bloomerang         |
| ----------------------------------------- | ---------------- | ---------------- | ------------------------------- | ------------------------------ | ------------------------------- |
| Advanced accounting edge case             | `10-25d`         | `10-25d`         | `10-25d`                        | `5-15d`                        | `5-15d`                         |
| SMS program at scale                      | `10-20d`         | `10-20d`         | `3-10d`                         | `3-10d`                        | `0`                             |
| **Tier Total**                            | **`20-45d`**     | **`20-45d`**     | **`13-35d`**                    | **`8-25d`**                    | **`5-15d`**                     |
| **Cumulative Total (All Required Tiers)** | **`102.5-209d`** | **`102.5-209d`** | **`49-129d` + `2x 🔴❓` + `X`** | **`32-92d` + `2x 🔴❓` + `X`** | **`51-136d` + `🔴❓` + `2x X`** |

## Maybe (Optional)

| Line Item                                  | Codex Estimate            | GPT Estimate              | Pipedrive                          | Neon CRM                           | Givebutter + Bloomerang         |
| ------------------------------------------ | ------------------------- | ------------------------- | ---------------------------------- | ---------------------------------- | ------------------------------- |
| Optional: Headless architecture            | `15-30d`                  | `15-30d`                  | `15-40d`                           | `5-15d`                            | `15-40d`                        |
| **Tier Total (Optional)**                  | **`15-30d` + `🔴❓`**     | **`15-30d` + `🔴❓`**     | **`15-40d` + `X`**                 | **`5-15d` + `X`**                  | **`15-40d` + `X`**              |
| **Cumulative Total (Required + Optional)** | **`117.5-239d` + `🔴❓`** | **`117.5-239d` + `🔴❓`** | **`64-169d` + `2x 🔴❓` + `2x X`** | **`37-107d` + `2x 🔴❓` + `2x X`** | **`66-176d` + `🔴❓` + `3x X`** |

## Next-Pass Items (Intentionally Deferred)

- Finance integration hours where `[#]`/external workflow assumptions dominate (`Cashapp/Venmo`, accounting sync path details)
- Pipedrive portal/self-service final effort range after selecting exact external portal stack
- Any rows currently set to `🔴❓`
