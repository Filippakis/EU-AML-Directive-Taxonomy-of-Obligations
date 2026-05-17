# EU-AML-Directive-Taxonomy-of-Obligations
Machine-readable XML taxonomy of AMLD (EU Directive 2015/849) obligations for obliged entities for use in RAG and AI compliance tools
A structured, simplified XML taxonomy of all obligations imposed on **obliged
entities** under the EU Anti-Money Laundering Directives. Designed for use in
AI-assisted compliance tools, RAG (Retrieval-Augmented Generation) systems, and
regulatory mapping exercises.

## Covered Legislation

| Directive (EU) 2015/849 | 4th Anti-Money Laundering Directive (AMLD4) |
| Directive (EU) 2018/843 | 5th Anti-Money Laundering Directive (AMLD5) — amends AMLD4 |
| Directive (EU) 2024/1640 | 6th Anti-Money Laundering Directive (AMLD6) — amends AMLD4 |

## Purpose and Design Philosophy

This taxonomy was built with the following goals:

- **AI/RAG optimisation**: each article is encoded as a self-contained XML
  element so that it can be retrieved, chunked, and interpreted independently
  by a language model without requiring the full document as context
- **Obligation-focused**: only provisions that impose direct duties on obliged
  entities are included; Member State transposition instructions, Commission
  reporting mandates, ESA guideline deadlines, and inter-institutional
  procedural text are stripped out unless directly relevant to how an obliged
  entity must act
- **Simplified language**: legislative drafting conventions are replaced with
  plain, structured obligation statements while preserving legal accuracy

### XML Document Structure

<AMLD4_ObligedEntity_Obligations>
├── <Chapter>                          # Mirrors directive chapter structure
│     └── <Article>                   # One element per article
│           ├── <Paragraph>           # Used where paragraphs have distinct
│           │                         # obligation scopes (e.g. Art. 18a, 19b)
│           └── <Context>             # Optional — explains relationship to
│                                     # related articles where ambiguity exists
├── <Annexes>
│     └── <Annex>                     # Risk factor lists (Annexes I–III)
└── <ObligationIndex>
└── <Category>                  # Obligations grouped by type
└── <Ref>                 # One-line summary per article
