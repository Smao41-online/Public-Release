# Public Release

Public downloads for [@Smao41-online](https://github.com/Smao41-online) projects.

**This repo holds builds, not source.** The source for each project stays in its
own private repository; only the finished, runnable files are published here, so
a download link can be handed to anyone without opening up any code.

Everything in this repository is visible to the whole internet — that is the
point of it, and the reason nothing but deliberately published builds belongs
here.

## Downloads

| Project | What it is | Latest |
|---|---|---|
| [Math game](math-game/) | Block Math Escape — multiplication 0–10 for ages 5–8, Minecraft styling. Windows installer, portable, browser and iPad builds | [Releases](../../releases?q=math-game) |
| [A-Z App](a-z-app/) | Alphabet learning for ages 3–6, Czech and English | [Releases](../../releases?q=a-z-app) |

## How this repo is organised

GitHub release assets are a flat list, so the separation between projects is
done with **a folder and a matching tag prefix**. Nothing is ever mixed up as
long as both follow the project's short name.

```
Public-Release/
├── math-game/          <- one folder per project: what it is, how to install
│   └── README.md
├── a-z-app/
│   ├── README.md
│   └── build/          <- exception: this project's source was lost, so its
│                          build is kept in version control as well
└── .github/workflows/
    └── publish.yml     <- publishes a build as a release, for any project
```

| Thing | Rule | Example |
|---|---|---|
| Folder | the project's short name, lower-case-hyphens | `math-game/` |
| Tag | `<project>/v<version>` | `math-game/v0.1.0` |
| Release title | `<Project name> <version>` | `Math game 0.1.0` |
| Assets | whatever that version ships | `BlockMathEscape-0.1.0-setup.exe` |

Tags with a `/` in them are perfectly valid and are what makes the releases
page group by project. Filter with `?q=math-game` on the releases page, or
`gh release list | grep math-game`.

## Adding a new project

1. Create a folder named after it, with a `README.md` saying what it is, how to
   install it, and anything the person downloading needs to know (unsigned
   build warnings, system requirements, which file to pick).
2. Add a row to the table above.
3. Publish the first build (below). The tag prefix must match the folder name.

Nothing else is needed — there is no per-project setup, and the publish
workflow takes the project name as an input rather than being hard-coded.

## Publishing a build

### The quick way, no setup

1. Download the build from wherever it was made — for a GitHub Actions build,
   the **Artifacts** box at the bottom of the run's summary page.
2. Unzip it. Actions always wraps artifacts in a zip; publish the files
   themselves, not the wrapper.
3. Here: **Releases → Draft a new release**.
4. Tag: `math-game/v0.1.0` (*Create new tag on publish*). Title: `Math game 0.1.0`.
5. Drag the files in, write what changed, **Publish release**.

Each asset then has a permanent direct link:

```
https://github.com/Smao41-online/Public-Release/releases/download/math-game/v0.1.0/BlockMathEscape-0.1.0-setup.exe
```

That link needs no GitHub account, never expires, and does not reveal the
private repository the build came from.

### The automated way

`.github/workflows/publish.yml` publishes a build here from somewhere else.
**Actions → Publish a build → Run workflow**. It attaches SHA-256 checksums to
the release notes by itself, and takes the build from either of two places:

| Mode | Set | Use for |
|---|---|---|
| **Artifact** | `run_id` + `artifact_name` | anything built by GitHub Actions — the artifact is unwrapped for you |
| **Path** | `source_path` (+ `source_ref`) | a build committed in the repo. A directory is zipped; a single file is taken as-is |

Set `append` when the tag already exists and you are adding another platform to
the same version — the existing notes are kept and the new checksums added, so
a release never lists only some of what is attached to it. Without it, an
existing tag is an error rather than a surprise.

It needs one secret, once:

1. Create a fine-grained personal access token at
   [github.com/settings/tokens](https://github.com/settings/tokens?type=beta) —
   *Only select repositories* → the private repo(s) you build in → repository
   permissions **Actions: Read-only** and **Contents: Read-only**.
2. Here: **Settings → Secrets and variables → Actions → New repository secret**,
   named `SOURCE_TOKEN`.

The token only ever reads; it cannot push to the private repo, and it is never
written into the release.

## A note on unsigned Windows builds

None of the `.exe` files here are code-signed — that needs a paid certificate.
They are perfectly safe to run, but **Windows SmartScreen will show
“Windows protected your PC” the first time**, and the person has to choose
*More info → Run anyway*. Say so when you send someone a link, or they will
reasonably assume the worst.

Each release lists a SHA-256 for every file so a recipient can confirm they got
exactly what was published.
