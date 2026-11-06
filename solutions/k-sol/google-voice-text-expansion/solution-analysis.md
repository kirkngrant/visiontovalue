# Solution analysis

## Requirements
Keep consumer Google Voice; insert repeatable SMS replies; manually review and send; prefer no cost; Windows and Edge.

## Verified
Google Voice help describes typing and sending messages manually and states Voice messaging is for interactive, not bulk, use. No built-in shortcut expansion or saved reply templates documented.

## Alternatives
| Rank | Option | Score (illustrative) | Tradeoff |
|---|---|---:|---|
| 1 | Espanso | 9.1 | Free and Windows-wide; YAML configuration |
| 2 | Text Blaze | 9.0 | Easy GUI, free tier; browser-oriented |
| 3 | PhraseExpress | 8.6 | Desktop GUI; license limitations |
| 4 | AutoHotkey | 8.2 | Free, script maintenance |
| 5 | Clipboard templates | 7.0 | No installation; manual paste |
| 6 | Gmail/ChatGPT/Sheets hybrid | 7.0 | Better contextual drafting; integration effort |

## Architecture
Incoming SMS in Google Voice -> optional Gmail forwarding -> optional ChatGPT classification/Google Sheets logging -> manual selection or text-expansion in Google Voice -> user clicks Send.

## Risk
No native consumer Voice SMS API for automated sending; avoid brittle browser automation and bulk messaging. Verify expansion in Voice composer before committing.

## Sources
- https://support.google.com/voice/answer/115116?co=GENIE.Platform%3DDesktop&hl=en
- https://www.edgedrop.app/blog/best-text-expanders-for-windows
- https://espanso.org/
- https://blaze.today/
