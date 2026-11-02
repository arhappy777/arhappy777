# LLM Pentesting: AI Red Teaming Reports and Prompt Injection Reference

Security assessments of LLM applications and AI agents: assessment reports, CTF write-ups mapped to the OWASP Top 10 for LLM Applications 2026, and a reference of prompt injection techniques with their primary sources. Reports state the conditions under which each finding was observed and the control that stops it.

The material is built for defenders: AI security engineers, red teams working under an agreed scope, and developers who want to check their guardrails and permission boundaries.

## What's inside

| Section | What it contains | Path |
| --- | --- | --- |
| Reports | Assessments in advisory format: threat model, reproduction, evidence, impact, recommendations, and retest | [`reports/`](https://github.com/arhappy777/llm_pentesting/tree/main/reports) |
| CTF write-ups | Five hego.red Jackpot challenges mapped to the OWASP Top 10 for LLM Applications 2026 | [`CTF/hego.red/`](https://github.com/arhappy777/llm_pentesting/tree/main/CTF/hego.red) |
| Prompt Injection Atlas | Bilingual (EN/RU) reference app: 14 walkthroughs and a catalog of 2,202 entries from eight sources. [Open the site](https://arhappy777.github.io/llm_pentesting/) | [`learning/prompt-injection-atlas/`](https://github.com/arhappy777/llm_pentesting/tree/main/learning/prompt-injection-atlas) |

### Reports

| Report | Finding | Classification |
| --- | --- | --- |
| [Nord Office: an analysis agent places an order](https://github.com/arhappy777/llm_pentesting/tree/main/reports/nord-office-procurement-agent) | Two chat messages, the second claiming manager approval, led an agent that may only compare quotes to place a 7,140 EUR order against a 1,300 EUR budget. A server-side permission check blocked the same call: 3 of 3 orders without it, 0 of 3 with it. Sample report on a synthetic target. | LLM01:2026 Prompt Injection, LLM03:2026 Excessive Agency, ASI01 Agent Goal Hijack |

## Responsible use

- Data in the reports is synthetic unless a report says otherwise. Companies, suppliers, prices, and orders are invented, and no client material is used.
- Test only systems you own or are explicitly authorized to assess.
- Reports record the model, the inputs, the number of runs, and the scope of each observation rather than general claims. Each report includes the control that closes the weakness.
- Vulnerability reporting and disclosure of findings in third-party products follow [SECURITY.md](https://github.com/arhappy777/llm_pentesting/blob/main/SECURITY.md).

## AI security audits

I'm Artem Surmylo, an AI red team pentester and the maintainer of this repository. I audit LLM applications, AI agents, RAG pipelines, and MCP integrations for prompt injection, data exposure, broken access control, and excessive agent permissions, and I retest after fixes.

**Telegram: [@ceo_foreign](https://t.me/ceo_foreign)** · **LinkedIn: [Artem Surmylo](https://www.linkedin.com/in/artem-surmylo-197b06231/)**

## License

Copyright (c) 2026 Artem Surmylo. The repository uses two licenses:

- **Code** (HTML, CSS, and JavaScript of the Prompt Injection Atlas in `learning/`) is licensed under the [Apache License 2.0](https://github.com/arhappy777/llm_pentesting/blob/main/LICENSE).
- **Original written content** (reports, write-ups, catalog notes, and evidence files) is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://github.com/arhappy777/llm_pentesting/blob/main/LICENSE-CC-BY-4.0). You may share and adapt it, including commercially, with attribution to Artem Surmylo, a link to the original material and the license, and an indication of any changes.

Third-party screenshots, quoted material, logos, and trademarks are excluded from both licenses and remain subject to their respective rights.
