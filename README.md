# JMJ Cloud Query - public releases (test channel)

This repository hosts the downloadable installers for **JMJ Cloud Query**, a
desktop SQL workshop for Oracle Fusion Cloud. Source code is private; only the
built artifacts and release notes live here.

> This is the **test release channel**. Once the product reaches general
> availability, releases will move to a different public repository. Bookmark
> the new location when announced.

## Download

See the [latest release](../../releases/latest). Pick the right file for your
machine:

| OS | Recommended | Why |
|----|-------------|-----|
| Windows 11 (Intel/AMD x64) | `JMJ Cloud Query-VERSION-x64-portable.exe` | No install, just run |
| Windows 11 (ARM, e.g. Surface, Snapdragon, Parallels on Apple Silicon) | `JMJ Cloud Query-VERSION-arm64-portable.exe` | No install, just run |
| Windows - prefer a real installer with Start Menu entry | `*-x64-setup.exe` or `*-arm64-setup.exe` | NSIS installer |

The `-portable.exe` files are the easiest path - one file, no install, no
admin rights needed. Delete the file when you're done.

## First-launch warnings

On Windows 11, SmartScreen will warn the first time you run an unsigned
executable. Click **More info** -> **Run anyway**. The warning won't reappear
on subsequent launches. (Code-signing certificates are in flight; once they
land, SmartScreen will accept the app silently.)

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
