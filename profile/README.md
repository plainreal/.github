<picture>
  <source media="(prefers-color-scheme: dark)" srcset="logo.svg">
  <img alt="PlainReal" src="logo-light.svg" width="280">
</picture>

### Cryptographic evidence for what AI agents decide

PlainReal&trade; produces one signed, tamper-evident record per consequential AI
agent decision. Each record is **independently verifiable by anyone**, with no
PlainReal service, no account, and no network access required.

The point is not that you should trust us. The point is that you should not
have to.

---

## What a record proves, and what it does not

This distinction is the product, so it is stated first rather than buried.

A valid signature proves the bytes are the bytes that were signed, and that
nothing has changed since. It does **not** prove:

- **that the decision was correct.** A verified record of a bad decision is
  still a verified record of a bad decision.
- **that the record is complete.** A signature covers what is present. It
  cannot show what a producer chose never to record.
- **write-once custody.** Only the declared retention class is signed.
  Confirming an object is genuinely under a storage lock requires access to
  the storage account.
- **when something happened.** That is a timestamp token's job, and published
  sample records carry none.
- **human non-repudiation.** A record showing that a person approved something
  proves the system recorded that approval tamper-evidently. It does not prove
  the person personally signed anything.

Anyone claiming otherwise about this system is overstating it.

## Verify it yourself

[**verify.plainreal.com**](https://verify.plainreal.com) checks a record's
signature entirely in your browser. It makes no network request and stores
nothing. Open the developer tools and watch.

The page is [open source](https://github.com/plainreal/verify), so you can read
it before you run it, and each release is a signed tag naming the SHA-256 of the
exact page bytes published.

```
RFC 8785 canonicalisation · FIPS 202 SHA3-256 · RFC 8032 Ed25519
```

A genuine, signature-valid [sample record](https://plainreal.com/demo_record.json)
is published. Edit any byte and its signature breaks, which is the point.

## Repositories

| | |
|---|---|
| [**verify**](https://github.com/plainreal/verify) | The public verifier. Verification only, deliberately: it reads one record, canonicalises it, hashes it, and checks a signature. Nothing else. |

## More

- [plainreal.com](https://plainreal.com): what this is for, and who it is not for
- [Regulatory coverage](https://plainreal.com/regulations): OCC, NYDFS, EU AI Act, GDPR, SOC 2, NIST SP 800-53, FDA, HIPAA
- [EU AI Act Article 12](https://plainreal.com/article12): record-keeping requirements and a readiness self-assessment
- [Security](https://plainreal.com/security): OWASP Agentic AI Top 10 mapping
- [llms.txt](https://plainreal.com/llms.txt): for agents reading this

There has been no third-party security audit. Patent pending.

<sub>PlainReal is operated by AgentOS Technologies, Inc., a Delaware corporation.<br>
contact@plainreal.com · security@plainreal.com</sub>
