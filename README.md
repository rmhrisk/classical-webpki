# A Deep Dive on the Classical WebPKI

How the Internet decides which public keys to trust.

**Read it: https://rmhrisk.github.io/classical-webpki/**

A companion to EFF's [Deep Dive on End-to-End Encryption](https://ssd.eff.org/module/deep-dive-end-end-encryption-how-do-public-key-encryption-systems-work), picking up where that guide leaves off: Julia and César have verified each other's keys in person, but that cannot scale to the millions of servers a browser talks to. This post covers the system built for that problem — X.509 certificates, certificate authorities, root programs, and the governance machinery around them.

The argument, in one line: the WebPKI contains two hierarchies. The cryptographic hierarchy shows which key authorized which other key. The governance hierarchy explains why the browser accepts that authority at all. Nearly every interesting failure in the history of the WebPKI is a story about the gap between them.

Contents: four parts (machinery, governance, divergence, boundaries), sixteen diagrams, and a twenty-question comprehension quiz.

A future post covers the post-quantum WebPKI and the Merkle Tree Certificate architecture replacing this one.

## Files

- `index.html` — the site, self-contained (styles, SVG diagrams, and quiz inline)
- `source.md` — the article in Markdown, with Mermaid versions of the diagrams

## License

Text and diagrams © Ryan Hurst. Originally published on [Unmitigated Risk](https://unmitigatedrisk.com/).
