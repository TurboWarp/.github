# Reporting a vulnerability

Report security vulnerabilities to [contact+security@turbowarp.org](mailto:contact+security@turbowarp.org) instead of the public issue tracker. All emails sent here will be triaged by Thomas Weber, TurboWarp's maintainer.

If you don't get a response within 48 hours, post a GitHub issue asking for an update. It may have been flagged as spam. (do not post any details publicly, just ask if your email was seen)

## Bug Bounty

We don't have a large budget, but we take security very seriously. I will pay out a **$20 USD bug bounty** for high severity bugs like these (non-comprehensive):

 - A bug in the editor, compiler, [official extension gallery](https://github.com/TurboWarp/extensions/tree/master/extensions) (including unlisted extensions), or anywhere else that allows a project to execute arbitrary JS (XSS) without loading a custom extension.
 - Sandbox escape in the desktop app (such as arbitrary file read/write) under the assumption that XSS has already been achieved (so running any code in a custom extension or in developer tools is fair game)
 - Code execution/memory corruption/etc. on any of our backend services.
 - Tricking a GitHub Actions workflow into performing sensitive actions that it is not intended to perform or leaking a secret.

These types of bugs may be eligible for a reduced bounty (non-comprehensive):

 - Scratch.canFetch(), Scratch.canOpenWindow(), etc. bypass in extensions in the [official extension gallery](https://github.com/TurboWarp/extensions/tree/master/extensions) (including unlisted extensions)
 - Security bugs in deprecated or low-priority subprojects such as the TurboWarp Desktop legacy builds for old operating systems or old experimental branches.
 - Open redirect on any TurboWarp website

Guidelines:

 - Participation in this program is contigent upon you acting in good faith.
 - No bounties for bugs you created yourself.
 - The bug needs to work on the latest version in git at the time of reporting.
 - The bounty can be paid in almost any format you desire or be donated to a charity of your choice. If you choose a charity, any reduced bounty will be increased to the full $20 USD.
 - Quality of report is a factor in bounty sizes. We can tell when you send us unreviewed AI slop and it makes you look like a fool, though it is still bounty-eligible.
 - The decision about whether you get a bounty and its size is ultimately up to me.

Examples of bugs that might not be eligible for a bounty:

 - Bugs in upstream projects such as Scratch, Scratch Addons, Electron, Chromium, etc. Please report these to the appropriate upstreams.
   - Exception: For some projects, such as Paper.js, we maintain a downstream fork due to upstream lack of maintenance of other reasons. Those forks are in scope for the bug bounty.
 - Missing "security headers" such as X-Frame-Options or Content-Security-Policy without demonstrated impact.
 - Self-XSS.
 - Vulnerable code that is in a TurboWarp repository but does not actually run anywhere in TurboWarp, for example, extensions that have compatibility code that doesn't run in TurboWarp.
 - Anything along the lines of "loading a crafted project in the editor can cause an infinite loop or use a lot of memory". TurboWarp is a programming language. Of course it can.

Please also prefix your email subject with "[TW-SEC]" and tell us what AI model you used (if any). This helps us know that you've read this far down and helps you not get ignored. Note that we can tell when you used an AI, so just be honest. Not disclosing that tends to result in lower bounties.
