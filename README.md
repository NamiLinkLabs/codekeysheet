# CodeKeySheet Code Generator

A simple HTML tool to generate offline authentication code sheets for two-party verification.

## Why CodeKeySheet?

In today's age, deepfakes and AI-generated voices ("deepvoices") have become so convincing that we can no longer fully trust what we see or hear in a video call or phone call. Attackers can impersonate trusted people with alarming accuracy. For sensitive situations—such as verifying someone's identity, confirming a transaction, or sharing confidential information—it's critical to have a secure, offline method of authentication that cannot be faked by digital means.

CodeKeySheet provides a simple, robust solution: a shared sheet of unique, one-time codes. Both parties have a copy. When authentication is needed, the recommended use is:
- The receiver (the person verifying) asks for a code at a random position (e.g., "B3").
- The caller (the person being verified) reads out the **first 3 letters** of the code at that position.
- The receiver then reads out the **last 3 letters** of the code at that position to confirm.
- **If there is any discrepancy in the code exchange, the suspecting party should immediately end the call and redial using a different channel (such as WhatsApp, Signal, etc).**

This method is immune to deepfake attacks, as it relies on a pre-shared, physical or offline artifact.

---

### Prefer a TOTP app?

You can use a TOTP authenticator app (like [Google Authenticator](https://support.google.com/accounts/answer/1066447?hl=en), [Aegis](https://getaegis.app/), or [Authy](https://authy.com/)) for a similar offline code exchange. Click "Create TOTP Secret" in the HTML tool to generate a named TOTP secret (e.g., <code>User 1 - User 2</code>) and scan the QR code into your app. Both parties can then use the current TOTP code for verification (e.g., caller reads first 3 digits, receiver confirms last 3).
- Configurable number of columns and rows
- Customizable code length
- Clean, printable layout
- Download as HTML or print/save as PDF

## How to Use

You can use CodeKeySheet instantly online at [https://codekeysheet.namilink.com](https://codekeysheet.namilink.com).

Or, for full offline use:

1. Open `index.html` in your web browser.
2. Adjust the number of columns, rows, and code length as desired.
3. Click "Generate" to create a new sheet.
4. Use "Download as HTML" to save a copy, or "Print / Save as PDF" to print or export.

No installation or Python required.
