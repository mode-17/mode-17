<div align="center">

# Modestu Osinachi

**Offensive security · web, API, mobile and cloud penetration testing**

I find the gap between what an application *claims* to enforce and what it actually
enforces — then prove it with a reproducible request and write it up so it gets fixed.

[Portfolio](https://github.com/mode-17/security-portfolio) · [HackerOne](https://hackerone.com/kmode001) · [Projects](https://github.com/mode-17?tab=repositories)

</div>

---

## What I do

- **Access control** — IDOR, BOLA, BFLA, tenant and role boundaries, object ownership
- **Authentication** — OTP/MFA flows, session lifecycle, token handling, account takeover chains
- **API security** — GraphQL BFFs, REST, mass assignment, SSRF, rate-limit design
- **Mobile** — Android client credential extraction, native-library analysis, JNI surfaces
- **Client-side** — DOM sinks, postMessage, CSP and bot-defence behaviour
- **Engagement engineering** — scoping, blueprints, test matrices, multi-identity harnesses, evidence discipline

I work on public bug bounty programs (HackerOne, Bugcrowd) and authorized
assessments. Everything I publish is redacted: no client names, no live
credentials, no other users' data, and no unpatched exploitation detail.

---

## Selected engagements

Names are withheld under program rules. Sector and platform are accurate.

| Sector | Platform | Window | Work | Result |
|---|---|---|---|---|
| Multi-chain stablecoin issuer | HackerOne | 2026 | Solidity role and bridge-accounting review | **NO-GO at blueprint** — my own preflight reversed before I built a harness |
| Identity-verification SDK | HackerOne | 2026 | Browser SDK internals, liveness and tamper controls | Defence held — 2 info-level, no report |
| Regional payments platform | YesWeHack | 2026 | Android client credentials, API misconfiguration | Secret recovered — no reachable impact, no report |
| Global apparel retail | HackerOne | 2026 | GraphQL BFF mapping, account-change step-up auth, OTP attempt controls | 1 report filed — closed as duplicate |
| Online travel | HackerOne | 2026 | Access-control matrix across two identities, DOM XSS sink instrumentation, postMessage review | No report — every lead controlled to a negative |
| Digital-asset exchange | Bugcrowd | 2026 | Auth surface mapping, IDOR/BOLA, mass assignment, SSRF, referral logic | No report — financial surface unreachable on test accounts |

Nine engagements in 2026: one report filed, closed as a duplicate, and eight closed on
judgement rather than on a finding. The write-ups are the point — the decision *not* to report
is the part that takes experience, and it is the part almost nobody publishes.

Full write-ups, including the negatives and what I got wrong:
**[security-portfolio](https://github.com/mode-17/security-portfolio)**

---

## Applications I built

Security software, not just scripts. Source is private; architecture notes and design
trade-offs are in the portfolio.

| Application | What it does |
|---|---|
| **A-WIDS** | Real-time 802.11 intrusion detection: multi-factor threat scoring, honey-handshake deception, SHA-256 hash-chain forensic ledger. Python + Scapy. |
| **SCKMS** | Cryptographic key lifecycle management with a rule engine plus ML anomaly detection for nonce reuse, weak entropy and timing patterns. Python + scikit-learn. |
| **SSMS** | Tamper-evident academic records: every result HMAC-SHA256 signed on write and re-verified on every read, with object-level RBAC and an append-only audit log. Node.js. |
| **GhostPixel** | Offline browser steganography: AES-256-GCM + PBKDF2 payload hidden in PNG LSBs, with integrity checks, expiry and a stated threat model. Vanilla JS. |
| **3SS** | Security services platform: async lead pipeline, client portal, and milestone payments enforced by a Solidity escrow state machine. Flask + Redis + web3. |
| **FUTO NIDS lab** | Docker lab proving that sensor placement decides what a WAF-blocked attack leaves behind. Suricata + ModSecurity + DVWA. |

[Architecture notes for all six →](https://github.com/mode-17/security-portfolio/tree/main/applications)

---

## Engagement tooling

| Project | What it is |
|---|---|
| [engagement-harness](https://github.com/mode-17/engagement-harness) | Scope-guarded, multi-identity request harness. Per-identity sessions, mandatory program headers, and a hard refusal to touch out-of-scope hosts. |
| [signed-api-client](https://github.com/mode-17/signed-api-client) | Client for an API that rejects standard auth schemes. Built to reach IAM role-assumption and policy endpoints the vendor CLI does not expose. |
| [security-portfolio](https://github.com/mode-17/security-portfolio) | Engagement case studies, methodology, and the templates I actually use. |

---

## How I work

**Scope is law.** Every tool I build refuses hosts that are not explicitly allow-listed.
If the scope is ambiguous, I stop and resolve it before sending a request.

**Control before conclusion.** A difference between two responses is a hypothesis, not a
finding. I reproduce with a clean control, measure what I claim, and keep the negative
results so the next session does not repeat them.

**Write for the fix.** A finding is only useful if an engineer can reproduce it, understand
the impact, and verify the remediation. I include the request, the identity, the missing
check, and the smallest proof that demonstrates access.

---

## Toolbox

`Burp Suite Professional` · `Playwright` · `Postman` · `mitmproxy` · `ffuf` · `nuclei` ·
`sqlmap` · `Nmap` · `jadx` · `objdump` · `Scapy` · `Suricata` · `Docker` · `Python` ·
`Node.js` · `Bash` · `PostgreSQL` · `scikit-learn` · `Solidity / Web3` · `R / Shiny` · `Git`

Auth and edge stacks I have worked against: OAuth/OIDC, passwordless OTP, JWT bearer
sessions, GraphQL BFFs, Android JNI credential stores, browser-side liveness and anti-tamper
layers, Fastly / Akamai / DataDome / Vercel challenge layers.

---

<sub>All testing is performed on accounts I own, within published program scope and safe-harbour terms. I do not test third-party systems without written authorization.</sub>
