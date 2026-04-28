 # JD Codec

 **Privacy-first local MCP proxy for browser-agent tasks.** Compresses page snapshots ~80%+ via a cloud codec; PII never leaves your machine.
 
 JD Codec sits between AI agents and Playwright MCP, redacting personal information on-device before any bytes leave, then compressing the snapshot via a cloud service so
your agent burns far fewer tokens per step.

 ## Where things live

 - **[`jdcodec/connector`](https://github.com/jdcodec/connector)** — the local MCP connector (Apache 2.0). What runs on your machine.
 - **`jdcodec` on npm** — `npm install -g jdcodec` · [npmjs.com/package/jdcodec](https://www.npmjs.com/package/jdcodec)
 - **`jdcodec` on PyPI** — `pip install jdcodec` · [pypi.org/project/jdcodec](https://pypi.org/project/jdcodec/)
 
 ## What's open vs closed 
 
 - **Open** — the local connector. MCP proxy, on-device privacy shield (regex-based PII redaction), cloud client. Apache 2.0. Read it, audit it, fork it.
 - **Closed** — the cloud compression service. The codec running server-side is proprietary; that's what makes the per-step token math work. 

 The split is by design. Privacy and trust depend on a connector you can read; per-customer compute economics depend on a codec we run centrally. 

 ## Contact

 `hello@jdcodec.com` — alpha access, integrations, security reports, anything. 

 [jdcodec.com](https://jdcodec.com)
