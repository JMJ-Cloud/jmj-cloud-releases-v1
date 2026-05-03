# JMJ Qyrena - public releases (test channel)

This repository hosts the downloadable installers for **JMJ Qyrena**, a
desktop SQL workshop for Oracle Fusion Cloud. Source code is private; only the
built artifacts and release notes live here.

> This is the **test release channel**. Once the product reaches general
> availability, releases will move to a different public repository. Bookmark
> the new location when announced.

## Download

See the [latest release](../../releases/latest). Two files; pick the one for
your OS:

| OS | File | Notes |
|----|------|-------|
| **macOS** (Apple Silicon) | `JMJ.Qyrena-VERSION-arm64.dmg` | Signed + notarised. Open the DMG, drag the app to Applications. |
| **Windows** (any architecture - recommended default) | `JMJ.Qyrena-VERSION-portable.exe` | Multi-arch native portable. Runs natively on x64 and ARM64 - no emulation overhead. One file, no install, no admin rights. |
| **Windows ARM64** (smaller native build) | `JMJ.Qyrena-VERSION-arm64-portable.exe` | ARM64-only portable. Smaller download (~82 MB vs ~155 MB) for users who know they're on ARM and want the trim option. |

## First-launch warnings

**macOS**: the DMG is signed with a Developer ID Application certificate and
notarised by Apple, so it opens cleanly with no Gatekeeper warning.

**Windows**: SmartScreen will warn the first time you run an unsigned
executable. Click **More info** -> **Run anyway**. The warning won't
reappear on subsequent launches. (A Windows code-signing cert is in flight;
once it lands, SmartScreen will accept the app silently.)

## Trial limits

The current builds run in **trial mode** - 200 rows per query, up to 5
successful Deploys, and a fixed expiry from build time. To unlock those
limits, contact JMJ Cloud for a license key (paste it under Settings ->
License inside the app).

## Where data goes

- Your Fusion sign-in cookies and JWT live only on your machine.
- Your SQL queries are sent to your own Fusion pod and nowhere else.
- If you enable the optional AI assistant, your prompts go directly to the
  LLM provider you configured (using your own API key) - never to JMJ.

See the in-app **Help -> Legal Documents** for full EULA, privacy policy
and refund policy.

## Contact

- jmjcloud.com
- support@jmjcloud.com
