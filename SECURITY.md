# Reporting a vulnerability

Report security vulnerabilities to [security@turbowarp.org](mailto:security@turbowarp.org) instead of the public issue tracker.

You can expect a response within 48 hours.

## Bug Bounty

<!-- Inspired by the SerenityOS bug bounty program: https://serenityos.org/bounty/ -->

We don't have a large budget, but we care about security. We offer a $10 bug bounty for bugs like these:

 - Sandbox escape in the compiler such as a Scratch script being able to call alert().
 - Sandbox escape in the desktop app assuming a renderer thread has been compromised such as arbitrary file read/write through Electron IPC.
 - XSS on any turbowarp.org website.
 - Code execution on the turbowarp.org backend.

Rules:

 - No bounties for bugs you caused yourself.
 - Maximum of 3 bounties per person.
 - The bug needs to work on the latest version on GitHub at the time of reporting.
 - No bounties for bugs that require unreasonable user interaction or social engineering.

Examples of bugs that might not be eligible for a bounty:

 - Bugs in upstream projects such as Scratch, Scratch Addons, Electron, Chromium, etc. Please report these to the appropriate upstreams.
 - Bugs in custom extensions on extensions.turbowarp.org. We still want to know about these, though.
 - Missing headers such as X-Frame-Options or Content-Security-Policy without demonstrated impact.
