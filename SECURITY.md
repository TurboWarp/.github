# Reporting a vulnerability

Report security vulnerabilities to [security@turbowarp.org](mailto:security@turbowarp.org) instead of the public issue tracker.

Follow up if you don't get a response within 48 hours.

## Bug Bounty

<!-- Inspired by the SerenityOS bug bounty program: https://serenityos.org/bounty/ -->

We don't have a large budget, but we take security very seriously. I will pay out a bug bounty for bugs like these:

 - XSS in places such as the compiler or any extension in the [official extension gallery](https://extensions.turbowarp.org/).
 - Sandbox escape in the desktop app (such as arbitrary file read/write) assuming that XSS has already been achieved (so running any code in developer tools is fair game).
 - Code execution/memory corruption/etc. on any of our backend servers. DoS bugs may also be considered.
 - This list is non-comprehensive.

The size of the bounty depends on the severity. Bounties start at **$25** but range up to **$50** or possibly more. The bounty can be sent in almost any form you desire or donated to a charity of your choice. The decision about whether you get a bounty and the size is ultimately up to me.

Guidelines:

 - Participation in this program is contigent upon you acting in good faith.
 - No bounties for bugs you created yourself.
 - The bug needs to work on the latest version on GitHub at the time of reporting.

Examples of bugs that might not be eligible for a bounty:

 - Bugs in upstream projects such as Scratch, Scratch Addons, Electron, Chromium, etc. Please report these to the appropriate upstreams.
 - Missing "security headers" such as X-Frame-Options or Content-Security-Policy without demonstrated impact.
 - Self-XSS.
