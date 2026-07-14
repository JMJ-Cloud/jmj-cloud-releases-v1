# JMJ Cloud desktop apps - downloads

This repository hosts the installers for the JMJ Cloud desktop apps for Oracle
Fusion. Source code is private; only the built binaries live here.

Two apps, both free to use until **2 October 2026** (see [Licensing](#licensing)):

- **[JMJ Qyrena](#jmj-qyrena)** - write and run SQL against a Fusion pod, and get the results out.
- **[JMJ Relay](#jmj-relay)** - browse the BI catalog and move reports between Fusion environments.

They are separate apps. Install either, or both.

> This is the **test release channel**. When the products reach general
> availability, releases move to a permanent public repository and this one
> retires. Watch this page for the announcement.

---

## Downloads

Latest versions: **Qyrena 0.4.2** and **Relay 0.2.4**.

| App | macOS (Apple Silicon) | Windows (x64 and ARM64) |
|-----|----------------------|-------------------------|
| **JMJ Qyrena** | [Download the .dmg](https://github.com/JMJ-Cloud/jmj-cloud-releases-v1/releases/download/v0.4.2/JMJ.Qyrena-0.4.2-macOS-arm64.dmg) | [Download the .exe](https://github.com/JMJ-Cloud/jmj-cloud-releases-v1/releases/download/v0.4.2/JMJ.Qyrena-0.4.2-Windows-portable.exe) |
| **JMJ Relay** | [Download the .dmg](https://github.com/JMJ-Cloud/jmj-cloud-releases-v1/releases/download/relay-v0.2.4/JMJ.Relay-0.2.4-macOS-arm64.dmg) | [Download the .exe](https://github.com/JMJ-Cloud/jmj-cloud-releases-v1/releases/download/relay-v0.2.4/JMJ.Relay-0.2.4-Windows-portable.exe) |

- **macOS**: open the .dmg and drag the app to Applications. The builds are
  signed with a JMJ Cloud Developer ID certificate and notarised by Apple, so
  they open with no Gatekeeper warning. Apple Silicon only (M1 and later).
- **Windows**: one portable .exe. No install, no admin rights, nothing to
  uninstall - just run it. The single file carries both x64 and ARM64, so it
  runs natively either way.

Full release notes are on the [releases page](../../releases).

---

## JMJ Qyrena

**Write SQL, run it against Oracle Fusion, and get the answer out.**

Fusion makes ad-hoc querying harder than it should be. Qyrena is a SQL
workshop that talks to your pod through BI Publisher, so you can ask a question
and get an answer without building a report first.

- **SQL editor** with syntax highlighting, multiple tabs, and a results grid
  that handles tens of thousands of rows.
- **Exports in one click**: Excel, Excel transposed, CSV, XML, and an
  auditor-friendly PDF stamped with the pod and the user who ran it.
- **Query library** of ready-made Fusion queries organised by module (GL, AP,
  AR, Projects, Purchasing, Inventory), plus your own saved queries.
- **Query history**, so you can find the thing you ran last Tuesday.
- **Deploy any SELECT as a BI Publisher report** and data model, when you want
  to keep it.
- **Optional AI assistant**: bring your own Anthropic or OpenAI key and have it
  draft SQL. Your prompts go straight to your chosen provider, never to JMJ.

For finance and IT people who know SQL and are tired of waiting on a report
request.

## JMJ Relay

**Move BI content between Fusion environments without hand-carrying files.**

Promoting a BI Publisher report from TEST to PROD usually means exporting,
re-importing, re-pointing the data model, and hoping you did not miss a layout.
Relay makes it a repeatable, auditable step.

- **Catalog browser** for /Custom and My Folders, showing what an object is
  actually made of: linked data model, layouts, SQL, parameters, LOVs,
  bursting, security grants.
- **Codepacks**: bundle the objects you want to promote into one ordered,
  portable file, with a ticket reference if you track changes.
- **Compare before you deploy**: see exactly what is new, what is changed and
  what is identical on the target pod before anything is written.
- **Import with a safety net**: existing objects are backed up first, and every
  run writes a results log plus a Git-committable bundle of the source, so you
  have a record of what changed.
- **Recent Changes and History** views, so you can see what moved and when.

For anyone who owns BI content across more than one Fusion environment.

---

## Signing in

Both apps sign in through an embedded browser window: you log in to Fusion
itself, exactly as you would in Chrome. The apps never see or store your
password, and the session token stays on your machine.

Your Fusion user needs the **BI Author** and **BI Publisher Data Model
Developer** roles, or a custom role that wraps them.

## Licensing

**Both apps are free and fully unlimited until 2 October 2026.** No key is
needed before then.

From that date, an unlicensed install falls back to free-tier limits:

| App | Free tier from 2 October 2026 |
|-----|-------------------------------|
| **JMJ Qyrena** | 200 rows per query, 5 successful Deploys |
| **JMJ Relay** | 3 codepack Imports |

A license key removes the limits, and **one key covers both apps**. Paste it
under **Settings -> License** in either app. To get a key, contact
support@jmjcloud.com.

## Where your data goes

- Your Fusion sign-in and session token stay on your machine.
- Your SQL and your catalog content go to your own Fusion pod and nowhere else.
- JMJ Cloud does not receive your data, your queries, or your credentials.
- If you turn on the optional AI assistant in Qyrena, your prompts go directly
  to the LLM provider you configured, using your own API key. Do not paste
  sensitive data values into AI prompts.

Both apps ask you to accept the EULA, privacy policy and refund policy on first
launch. You can reread them any time: in Qyrena under **Help -> Legal
Documents**, in Relay under **Settings -> Legal**.

## First-launch warnings

- **macOS**: none. The builds are notarised by Apple.
- **Windows**: SmartScreen warns the first time you run the .exe, because it is
  not yet signed with a Windows code-signing certificate. Click **More info**,
  then **Run anyway**. It will not ask again. A Windows certificate is on the
  list.

## Contact

- [jmjcloud.com](https://www.jmjcloud.com)
- support@jmjcloud.com
