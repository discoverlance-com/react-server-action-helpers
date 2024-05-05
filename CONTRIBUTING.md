# Contributing

Thanks for your interest in contributing to react-server-action-helpers.vercel.app. We're happy to have you here.

Please take a moment to review this document before submitting your first pull request. We also strongly recommend that you check for open issues and pull requests on github to see if someone else is working on something similar.

If you need any help, feel free to reach out to [@Discoverlance](https://twitter.com/Discoverlance).

## About this repository

This repository is a monorepo.

- We use [pnpm](https://pnpm.io) and [`workspaces`](https://pnpm.io/workspaces) for development.
- We use [Turborepo](https://turbo.build/repo) as our build system.
- We use [changesets](https://github.com/changesets/changesets) for managing releases.

## Structure

This repository is structured as follows:

```txt
apps
└── website
    ├── docs
    ├── src

examples
└── next
└── vite-react

packages
└── with-zod-form-hooks
└── with-zod-form-action
```

| Path                            | Description                                        |
| ------------------------------- | -------------------------------------------------- |
| `apps/website`                  | The Docusaurus for the website.                    |
| `examples/next`                 | The example built with nextjs.                     |
| `examples/vite-react`           | The example built with vite and react              |
| `packages/with-zod-form-action` | The package built with zod for form actions        |
| `packages/with-zod-form-hooks`  | The package built with zod for ui with react hooks |

## Development

### Fork this repo

You can fork this repo by clicking the fork button in the top right corner of this page.

### Clone on your local machine

```bash
git clone https://github.com/your-username/react-server-action-helpers.git
```

### Navigate to project directory

```bash
cd react-server-action-helpers
```

### Create a new Branch

```bash
git checkout -b add-my-new-branch
# or
git checkout -b fix-my-new-branch
# or
git checkout -b update-my-new-branch
```

### Install dependencies

```bash
pnpm install
```

### Run a workspace

You can use the `pnpm --filter=[WORKSPACE]` command to start the development process for a workspace. Example: `pnpm --filter=@rsah/with-zod-form-action`

#### Examples

1. To run the `react-server-action-helpers` website which has the documentation:

```bash
pnpm --filter=website dev
```

2. To run the `zod-with-form-action` package:

```bash
pnpm --filter=@rsah/zod-with-form-action dev
```

3. To run the `zod-with-form-hooks` package:

```bash
pnpm --filter=@rsah/zod-with-form-hooks dev
```

## Documentation

The documentation for this project is located in the `website` workspace. You can run the documentation locally by running the following command:

```bash
pnpm --filter=website dev
```

Documentation is written using [Docusaurus](https://docusaurus.io/). You can find the documentation files in the `apps/website/docs` directory.

## Commit Convention

Before you create a Pull Request, please check whether your commits comply with
the commit conventions used in this repository.

When you create a commit we kindly ask you to follow the convention
`category(scope or module): message` in your commit message while using one of
the following categories:

- `feat / feature`: all changes that introduce completely new code or new
  features
- `fix`: changes that fix a bug (ideally you will additionally reference an
  issue if present)
- `refactor`: any code related change that is not a fix nor a feature
- `docs`: changing existing or creating new documentation (i.e. README, docs for
  usage of a lib usage)
- `build`: all changes regarding the build of the software, changes to
  dependencies or the addition of new dependencies
- `test`: all changes regarding tests (adding new tests or changing existing
  ones)
- `ci`: all changes regarding the configuration of continuous integration (i.e.
  github actions, ci system)
- `chore`: all changes to the repository that do not fit into any of the above
  categories

  e.g. `feat(zod-hooks): add status to useFields return type` or `fix(zod-action): memoize return results`

If you are interested in the detailed specification you can visit
https://www.conventionalcommits.org/ or check out the
[Angular Commit Message Guidelines](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines).

## Requests for new validation library integrations

If you have a request for a new validation library like _yup_, please open a discussion on GitHub. We'll be happy to help you out.

## Testing

Tests are written using [Vitest](https://vitest.dev). You can run all the tests from the root of the repository.

```bash
pnpm test
```

Please ensure that the tests are passing when submitting a pull request. If you're adding new features, please include tests.
