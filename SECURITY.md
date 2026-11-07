# DarqlineMP Security Policy

Version: 1.0. Effective date: 2026-11-07.

DarqlineMP welcomes security research done in good faith. This policy says what is in scope, which methods are
allowed and how to report a vulnerability. It is the Security Policy referred to in the DarqlineMP Client License
Agreement.

## Reporting

Email `security@darqline.com` with:

- the affected component and version;
- the steps to reproduce, and a proof of concept if you have one;
- the impact you expect;
- whether and how you want to be credited.

Do not report vulnerabilities in public issues, chats or social media. DarqlineMP is developed by one person: you get
an answer within 7 days, and we agree on a fix and a disclosure date together. Unless we agree otherwise, you may
publish your findings 90 days after your report, or earlier once a fix is released. There is no bug bounty.

## In scope

- the DarqlineMP Client, the Official Launcher and its installer, and their update process;
- the DarqlineMP server and the Lua SDK;
- the services at `*.darqline.com`, including the official server `play.darqline.com`.

## Out of scope

- servers run by third parties: report to their operators;
- SA DE itself and its rights holders' services;
- the platforms DarqlineMP uses, such as GitHub, Cloudflare and its hosting and email providers: report to them under
  their own programs;
- denial-of-service and load testing, spam, social engineering and physical attacks;
- reports without a security impact, such as missing hardening headers on static pages.

## Allowed methods

- Reverse engineering, decompiling, disassembling and debugging the Client and the Official Launcher, to the extent
  needed to find and demonstrate a vulnerability.
- Running your own DarqlineMP server and clients, which is the preferred way to test.
- On the official server: only your own clients and only at a rate an ordinary player could produce.

You must not:

- access, change or delete data of other players or servers beyond what is needed to show the vulnerability; if you
  reach such data, stop and report it;
- disrupt the game of other players or degrade the official services;
- publish or share a working cheat, an exploit or a way around the protective checks of the Client or of servers
  before it is fixed;
- demand payment in exchange for your report.

## Safe harbor

If you follow this policy, we consider your research authorized: we do not take legal action against you and do not
treat it as a breach of the DarqlineMP Client License Agreement. We cannot authorize research against third parties,
such as other server operators or the platforms listed above. If you are unsure whether an action is allowed, ask at
`security@darqline.com` first.
