# Archimaid

**Enterprise architecture diagrams as code.** Archimaid is an open-source project for writing ArchiMate® 3.2 diagrams in plain text, checking them in CI, and rendering them through [Mermaid](https://mermaid.js.org/).

Architecture diagrams usually live in binary files that are hard to review, diff, or keep next to the systems they describe. Archimaid treats them like any other source file: written in a readable syntax, reviewed in pull requests, validated before they are published, and rendered wherever Mermaid runs.

![Application components and services supporting an order fulfilment process](https://raw.githubusercontent.com/Archimaid/archimaid/main/examples/order-management.svg)

```text
archimate-beta
  element businessRole clerk "Fulfilment clerk"
  element businessProcess fulfil "Fulfil order"
  clerk @==> fulfil
```

## Projects

| Repository | Description |
| --- | --- |
| [archimaid](https://github.com/Archimaid/archimaid) | The Mermaid diagram plugin, language API and `archimaid` command-line tool. Published on [npm](https://www.npmjs.com/package/archimaid). |
| [playground](https://github.com/Archimaid/playground) | A browser playground for trying the syntax without installing anything. In development. |

## Get started

```sh
npm install archimaid mermaid
npx archimaid validate docs/
```

The [archimaid README](https://github.com/Archimaid/archimaid#readme) covers the syntax, layouts, host integration and the language API. More information is available at [archimaid.org](https://archimaid.org).

## Principles

- **Open source, non-commercial.** Archimaid is free to use under the MIT License. There is no paid edition, hosted service or commercial roadmap.
- **Authoring, not model management.** The focus is writing and reviewing diagrams. Archimaid does not aim to replace modelling tools or model repositories.
- **Grounded in the standard.** Element and relationship types follow the ArchiMate 3.2 Specification, and documentation cites its sources.
- **Built for review.** Plain text, stable IDs and precise diagnostics make diagrams practical to keep in Git and check in CI.

## Contributing

Contributions are welcome, from bug reports and documentation fixes to new syntax proposals. Start with the [contributing guide](https://github.com/Archimaid/archimaid/blob/main/CONTRIBUTING.md) and the [code of conduct](https://github.com/Archimaid/archimaid/blob/main/CODE_OF_CONDUCT.md). For a change to the diagram syntax, open an issue with a proposal before starting work, so the design can be agreed first. Report security issues as described in the [security policy](https://github.com/Archimaid/archimaid/blob/main/SECURITY.md).

## Trademarks

Archimaid is an independent community project and is not affiliated with or endorsed by The Open Group. ArchiMate is a registered trademark of The Open Group in the United States and other countries. Mermaid is a separate open-source project and is not affiliated with Archimaid.
