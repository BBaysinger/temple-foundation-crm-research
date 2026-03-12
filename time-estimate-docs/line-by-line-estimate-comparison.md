# Line-by-Line Estimate Comparison (First Pass)

Date: March 12, 2026  
Source rows: `time-estimate-docs/required-items-difficulty-time-codex.md` and `time-estimate-docs/required-items-difficulty-time-gpt.md`  
Platform feasibility basis: `evaluation-matrix.md` (Pipedrive, Neon CRM, Givebutter + Bloomerang columns)

## Legend

- `0` = natively available with no material extra build effort beyond normal setup
- `hours` = rough implementation effort estimate for that platform
- `X` = not feasible for this line item in current platform shape
- `🔴❓` = unknown first-pass estimate (defer to next pass)

## Table

| Line Item                           | Codex Estimate | GPT Estimate | Pipedrive  | Neon CRM  | Givebutter + Bloomerang |
| ----------------------------------- | -------------- | ------------ | ---------- | --------- | ----------------------- |
| Core contact model                  | `16-32h`       | `16-32h`     | `0`        | `0`       | `0`                     |
| Basic data administration           | `8-16h`        | `8-16h`      | `0`        | `0`       | `0`                     |
| Basic communications setup          | `8-16h`        | `8-16h`      | `0`        | `0`       | `0`                     |
| Basic event setup                   | `16-24h`       | `16-24h`     | `X`        | `8-24h`   | `8-24h`                 |
| Usability baseline                  | `8-16h`        | `8-16h`      | `0`        | `🔴❓`    | `0`                     |
| Budget validation                   | `4-8h`         | `4-8h`       | `8-16h`    | `X`       | `X`                     |
| Donation flow baseline              | `32-56h`       | `32-56h`     | `24-56h`   | `0`       | `0`                     |
| Campaign and fundraising operations | `24-40h`       | `24-40h`     | `16-40h`   | `0`       | `0`                     |
| Event automation                    | `24-40h`       | `24-40h`     | `16-40h`   | `0`       | `0`                     |
| Volunteer and membership baseline   | `32-56h`       | `32-56h`     | `24-56h`   | `16-40h`  | `24-56h`                |
| Donor intelligence baseline         | `16-32h`       | `16-32h`     | `8-24h`    | `0`       | `0`                     |
| Quality and reliability baseline    | `16-32h`       | `16-32h`     | `8-24h`    | `8-24h`   | `8-24h`                 |
| Embedding path                      | `16-24h`       | `16-24h`     | `8-16h`    | `0`       | `0`                     |
| Portal and self-service             | `40-80h`       | `40-80h`     | `🔴❓`     | `0`       | `80-200h`               |
| Fund accounting model               | `80-160h`      | `80-160h`    | `120-320h` | `80-200h` | `120-320h`              |
| Volunteer automation depth          | `80-160h`      | `80-160h`    | `40-120h`  | `40-120h` | `40-120h`               |
| Finance integrations                | `80-160h`      | `80-160h`    | `🔴❓`     | `🔴❓`    | `🔴❓`                  |
| API integrations                    | `40-80h`       | `40-80h`     | `0`        | `24-80h`  | `80-200h`               |
| Operations hardening                | `40-120h`      | `40-120h`    | `0`        | `8-24h`   | `8-24h`                 |
| Platform risk controls              | `80-160h`      | `80-160h`    | `16-40h`   | `8-24h`   | `X`                     |
| Advanced accounting edge case       | `80-200h`      | `80-200h`    | `80-200h`  | `40-120h` | `40-120h`               |
| SMS program at scale                | `80-160h`      | `80-160h`    | `24-80h`   | `24-80h`  | `0`                     |
| Optional: Headless architecture     | `120-240h`     | `120-240h`   | `120-320h` | `40-120h` | `120-320h`              |

## Next-Pass Items (Intentionally Deferred)

- Finance integration hours where `[#]`/external workflow assumptions dominate (`Cashapp/Venmo`, accounting sync path details)
- Pipedrive portal/self-service final effort range after selecting exact external portal stack
- Any rows currently set to `🔴❓`
