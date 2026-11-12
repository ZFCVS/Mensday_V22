# V23 — Complete email packaging

Adds an explicitly labelled optional Download complete email action. It creates a MIME .eml file containing an RFC 2047 UTF-8 subject, plain/HTML alternatives, View your card and Create another card HTML anchors, and both PNG/GIF file attachments. It sets X-Unsent: 1 to request draft handling. No sender email address is invented and no mail is sent automatically. Recipient is selected in Outlook.

The previous no-download device sharing path is retained as an alternative. Its subject and attachment handling remain controlled by the selected app. Copying the formatted body alone still does not copy files or subject.

The new action downloads an email file only when selected; it does not automatically launch Outlook. Microsoft documents opening EML files, but editable-draft handling varies by version, and some new Outlook versions have had body/attachment handling issues with X-Unsent. The delivered MIME contents have been independently parsed and checked; a ZF Outlook end-to-end test is still required before go-live. If a client opens the file read-only, inspect its edit/forward options and verify all contents, or use the retained manual/device route. No claim of guaranteed Outlook draft behavior is made.

Prior security-audit findings are not remediated in this sharing-only release.
