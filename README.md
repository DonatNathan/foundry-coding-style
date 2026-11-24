# Palantir Foundry Coding Style

A shared coding style for teams building on Palantir Foundry.

Foundry's documentation gives a lot of information about the different applications but also leaves many conventions undefined, such as how to name things, how to organize them, and when to split them. Each team fills these gaps with its own habits, which makes projects inconsistent. This repository defines one consistent way to fill them. Each guide combines the **official** recommendations, where they exist, with the **house** rules we agree to follow, and gives every rule a code so it can be cited in reviews.

The guides are written for Foundry builders and Forward Deployed Engineers. Their goal is that any builder can open a project they did not build and understand it quickly.

## Applications

| Application | Rule prefix | Guide |
|---|---|---|
| Workshop | `W-` | [workshop.md](workshop.md) |

## How to Read the Guides

### Rule Codes

Every rule has a code you can reference in reviews, comments and commit messages:

```
<Application>-<Category><Number>        e.g. W-N3
```

- **Application**: the prefix in the table above (`W` for Workshop).
- **Category**: a letter defined in each guide (`N` for Naming, `L` for Layout, ...).
- **Number**: the rule's number within its category.

Codes are never reused. When a rule is removed, its code is retired.

### Rule Sources

Each rule is tagged with its source:

- **Official**: a best practice published in the [Palantir Foundry documentation](https://www.palantir.com/docs/foundry/). The rule links to its source.
- **House**: a rule that is not in the documentation but that we enforce. The rule gives its reason.

### Severity Levels

| Level | Meaning |
|---|---|
| 🔴 **Major** | Blocks a release. Fix it before the work is shared with users. |
| 🟡 **Minor** | Should be fixed. Acceptable temporarily with a note in the review. |
| 🔵 **Info** | Recommendation. Use your judgment. |

### Justified Exceptions

You may break a rule if you provide a **complete, relevant and accurate justification with a long-term view** (clarity, maintainability, performance). The reviewer decides whether the justification is acceptable, so make a strong argument or follow the rule.

### Implicit Rules

There are many ways to build something unclear, and no guide can list all of them. Bad practices that are not written down still count. They are treated as 🔵 **Info**.

## Code

For code (TypeScript, Python, React), we follow the standard style guides and only document Foundry-specific additions:

- Python: [PEP 8](https://peps.python.org/pep-0008/)
- TypeScript: [ts.dev style guide](https://ts.dev/style/)
- React: [Human Made React standards](https://engineering.hmn.md/standards/style/react/)

For React applications, we recommend [Blueprint](https://blueprintjs.com/), Palantir's official UI toolkit, so that custom applications look consistent with Foundry.
