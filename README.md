# Duolingo case appendix — evidence and references

HCGCC 2026 case appendix, version 2026-10-30-v2. Includes review evidence and the case bibliography. Review collection remains frozen; source references reflect the recorded case research cutoff.

Open https://athaillahbagas.github.io/duolingo-review-dashboard/

All 1,951,045 collected unique review IDs are represented by 29,117 mutually exclusive aggregate cells. Data collection stopped on 30 October 2026 at 04:41:55 WIB. Review dates span 29 May 2013 through 28 October 2026. This is a partial, voluntary historical collection, not all Google Play reviews or a population survey.

The default comparison uses 2026 reviews with text of at least 20 characters: 5,399/17,080 ad-keyword matches versus 55,810/558,905 dictionary nonmatches give 1–2 stars. Keyword presence is not a complaint classifier or a causal treatment. Request locale does not identify reviewer residence. Ratings describe the app, not isolated ad sentiment.

Sixteen illustrative contextual examples appear as anonymized English paraphrases. Original review text, reviewer identifiers, usernames, avatars, the raw database and the case brief are not published.

Sources & references provides a searchable, filterable bibliography with publisher, dates, original links, use in the case, and claim limits. Company/official sources are distinguished from industry research, methods, benchmarks, case-provided information and team analyses. Some source pages are dynamic or access-restricted; historical access notes are retained rather than claiming every source is freshly verified. References can also be downloaded from references.csv. No private design access links or case files are published.

The multilingual lexical dictionary is in dictionary.json. The complete reviewed aggregate snapshot is the content-addressed snapshot JSON. The build manifest records exact checksums. This version is frozen for consistency with the deck. No automatic scraping or refresh runs here.

The dashboard does not establish causal churn, UK advertiser demand, CPM, paid repeat or the assumed +12% global ad-yield increase. Company experiments and gates shown are proposed, not executed.

## Inspect the published bundle

Start with [data-app-build.json](data-app-build.json): its `html` and `snapshot` entries identify the paired files, byte sizes and SHA-256 checksums. The snapshot named by that manifest is the release companion; another snapshot file in the repository is not automatically interchangeable.

- [dictionary.json](dictionary.json) records the lexical patterns and sampling notes.
- [references.csv](references.csv) is the downloadable bibliography.
- The manifest's `runtimeSha256` is separate from the complete HTML file checksum; use `html.sha256` when checking `index.html`.

After downloading the complete repository, compare the two file hashes with the manifest:

```sh
shasum -a 256 index.html snapshot.41d48163002e1dfcada924b92f31d02dc2664810cbeea2302d3a76f01975aed1.json
```

For a local preview, run `python3 -m http.server 8000` from the repository root and open `http://localhost:8000/`. Keep the companion JSON files beside the HTML. Stop the preview with Ctrl+C.

A matching hash checks file integrity, not the accuracy, representativeness or causal interpretation of the research. This procedure serves the frozen publication; it does not recollect reviews.
