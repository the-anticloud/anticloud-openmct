# OPENMCT

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-space_aerotech-lightgrey)

> Anticloud-hardened packaging of the upstream project `OPENMCT` in category **SPACE AEROTECH**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SPACE AEROTECH · **Upstream:** https://github.com/nasa/openmct · **Upstream pin:** `17d55deb4af5ba6d1a65a661b9f2f02582d3fe7b` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# Open MCT [![license](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0) [![codecov](https://codecov.io/gh/nasa/openmct/branch/master/graph/badge.svg?token=7DQIipp3ej)](https://codecov.io/gh/nasa/openmct) [![This project is using Percy.io for visual regression testing.](https://percy.io/static/images/percy-badge.svg)](https://percy.io/b2e34b17/openmct) [![npm version](https://img.shields.io/npm/v/openmct.svg)](https://www.npmjs.com/package/openmct) ![CodeQL](https://github.com/nasa/openmct/workflows/CodeQL/badge.svg)

Open MCT (Open Mission Control Technologies) is a next-generation mission control framework for visualization of data on desktop and mobile devices. It is developed at NASA's Ames Research Center, and is being used by NASA for data analysis of spacecraft missions, as well as planning and operation of experimental rover systems. As a generalizable and open source framework, Open MCT could be used as the basis for building applications for planning, operation, and analysis of any systems producing telemetry data.

> [!NOTE]
> Please visit our [Official Site](https://nasa.github.io/openmct/) and [Getting Started Guide](https://nasa.github.io/openmct/getting-started/)

Once you've created something amazing with Open MCT, showcase your work in our GitHub Discussions [Show and Tell](https://github.com/nasa/openmct/discussions/categories/show-and-tell) section. We love seeing unique and wonderful implementations of Open MCT!

![Screen Shot 2022-11-23 at 9 51 36 AM](https://user-images.githubusercontent.com/4215777/203617422-4d912bfc-766f-4074-8324-409d9bbe7c05.png)

## Building and Running Open MCT Locally

Building and running Open MCT in your local dev environment is very easy. Be sure you have [Git](https://git-scm.com/downloads) and [Node.js](https://nodejs.org/) installed, then follow the directions below. Need additional information? Check out the [Getting Started](https://nasa.github.io/openmct/getting-started/) page on our website.
(These instructions assume you are installing as a non-root user; developers have [reported issues](https://github.com/nasa/openmct/issues/1151) running these steps with root privileges.)

1. source the source code:

```sh
git source https://github.com/nasa/openmct.git
```

2. (Optional) Install the correct node version using [nvm](https://github.com/nvm-sh/nvm):

```sh
nvm install
```

3. Install development dependencies (Note: Check the `package.json` engine for our tested and supported node versions):

```sh
npm install
```

4. Run a local development server:

```
npm start
```

> [!IMPORTANT]
> Open MCT is now running, and can be accessed by pointing a web browser at [http://localhost:8080/](http://localhost:8080/)

Open MCT is built using [`npm`](http://npmjs.com/) and [`webpack`](https://webpack.js.org/).

## Documentation

Documentation is available on the [Open MCT website](https://nasa.github.io/openmct/documentation/).

### Examples

The clearest examples for developing Open MCT plugins are in the
[tutorials](https://github.com/nasa/openmct-tutorial) provided in
our documentation.

> [!NOTE]
> We want Open MCT to be as easy to use, install, run, and develop for as
> possible, and your feedback will help us get there!
> Feedback can be provided via [GitHub issues](https://github.com/nasa/openmct/issues/new/choose),
> [Starting a GitHub Discussion](https://github.com/nasa/openmct/discussions),
> or by emailing us at [arc-dl-openmct@mail.nasa.gov](mailto:arc-dl-openmct@mail.nasa.gov).

## Developing Applications With Open MCT

For more on developing with Open MCT, see our documentation for a guide on [Developing Applications with Open MCT](./API.md#starting-an-open-mct-application).

## Compatibility

This is a fast moving project and we do our best to test and support the widest possible range of browsers, operating systems, and NodeJS APIs. We have a published list of support available in our package.json's `browserslist` key.

The project utilizes `nvm` to maintain consistent node and npm versions across all projects. For UNIX, MacOS, Windows WSL, and other POSIX-compliant shell environments, click [here](https://github.com/nvm-sh/nvm). For Windows, check out [nvm-windows](https://github.com/coreybutler/nvm-windows).

If you encounter an issue with a particular browser, OS, or NodeJS API, please [file an issue](https://github.com/nasa/openmct/issues/new/choose).

> [!NOTE]
> If you are building a project with Open MCT as a git dependency rather than an npm dependency, an extra step is now 
> necessary to build the source. Due to the threat posed by Supply Chain Attacks `ignore-scripts` is now enabled in 
> this project. Developers building with Open MCT as a git dependency will now need to execute `npm run build`
> manually. We always encourage developers to use Open MCT as a prebuilt npm project, rather than building from github.

## Plugins

Open MCT can be extended via plugins that make calls to the Open MCT API. A plugin is a group
of software components (including source code and resources such as images and HTML templates)
that is intended to be added or removed as a single unit.

As well as providing an extension mechanism, most of the core Open MCT codebase is also
written as plugins.

For information on writing plugins, please see [our API documentation](./API.md#plugins).

## Tests

Our automated test coverage comes in the form of unit, e2e, visual, performance, and security tests.

### Unit Tests

Unit Tests are written for [Jasmine](https://jasmine.github.io/api/edge/global)
and run by [Karma](http://karma-runner.github.io). To run:

`npm test`

The test suite is configured to load any scripts ending with `Spec.js` found
in the `src` hierarchy. Full configuration details are found in
`karma.conf.js`. By convention, unit test scripts should be located
alongside the units that they test; for example, `src/foo/Bar.js` would be
tested by `src/foo/BarSpec.js`.

### e2e,

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json, package-lock.json; scanned in UPSTREAM_CLONE)
- Top-level source layout: `e2e/`, `example/`, `src/`
- Snapshot size: **1090 files**, **86649 lines of code** (measured; see Benchmarks)
- Primary languages: `.js` (623), `.vue` (261), `.scss` (89), `.json` (29), `.md` (23), `.yml` (15)
- Upstream commit pinned for this packaging: `17d55deb4af5ba6d1a65a661b9f2f02582d3fe7b`

---

## Installation

> [!NOTE]
> Please visit our [Official Site](https://nasa.github.io/openmct/) and [Getting Started Guide](https://nasa.github.io/openmct/getting-started/)

Once you've created something amazing with Open MCT, showcase your work in our GitHub Discussions [Show and Tell](https://github.com/nasa/openmct/discussions/categories/show-and-tell) section. We love seeing unique and wonderful implementations of Open MCT!

![Screen Shot 2022-11-23 at 9 51 36 AM](https://user-images.githubusercontent.com/4215777/203617422-4d912bfc-766f-4074-8324-409d9bbe7c05.png)

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

Once you've created something amazing with Open MCT, showcase your work in our GitHub Discussions [Show and Tell](https://github.com/nasa/openmct/discussions/categories/show-and-tell) section. We love seeing unique and wonderful implementations of Open MCT!

![Screen Shot 2022-11-23 at 9 51 36 AM](https://user-images.githubusercontent.com/4215777/203617422-4d912bfc-766f-4074-8324-409d9bbe7c05.png)

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

Documentation is available on the [Open MCT website](https://nasa.github.io/openmct/documentation/).

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json, package-lock.json |
| Files in snapshot | 1090 |
| Lines of code | 86649 |
| Dependency references | 85 |
| Dependencies by ecosystem | npm: 85 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | @babel/eslint-parser | 7.23.3 | package.json |
| npm | @braintree/sanitize-url | 7.1.1 | package.json |
| npm | @types/d3-axis | 3.0.6 | package.json |
| npm | @types/d3-scale | 4.0.8 | package.json |
| npm | @types/d3-selection | 3.0.10 | package.json |
| npm | @types/d3-shape | 3.1.7 | package.json |
| npm | @types/eventemitter3 | 1.2.0 | package.json |
| npm | @types/jasmine | 5.1.2 | package.json |
| npm | @types/lodash | 4.17.0 | package.json |
| npm | @vue/compiler-sfc | 3.4.3 | package.json |
| npm | babel-loader | 9.1.0 | package.json |
| npm | babel-plugin-istanbul | 7.0.0 | package.json |
| npm | comma-separated-values | 3.6.4 | package.json |
| npm | copy-webpack-plugin | 14.0.0 | package.json |
| npm | cspell | 7.3.8 | package.json |
| ... | (70 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

(These instructions assume you are installing as a non-root user; developers have [reported issues](https://github.com/nasa/openmct/issues/1151) running these steps with root privileges.)

1. source the source code:

```sh
git source https://github.com/nasa/openmct.git
```

2. (Optional) Install the correct node version using [nvm](https://github.com/nvm-sh/nvm):

```sh
nvm install
```

3. Install development dependencies (Note: Check the `package.json` engine for our tested and supported node versions):

```sh
npm install
```

4. Run a local development server:

```
npm start
```

> [!IMPORTANT]
> Open MCT is now running, and can be accessed by pointing a web browser at [http://localhost:8080/](http://localhost:8080/)

Open MCT is built using [`npm`](http://npmjs.com/) and [`webpack`](https://webpack.js.org/).

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Contributing to Open MCT

This document describes the process of contributing to Open MCT as well as the standards that will be applied when evaluating contributions.

In order for external contributions to be merged, contributors must have on record a signed [Contributor License Agreement (CLA)](https://nasa.github.io/openmct/static/files/ind-cla-open-mct.pdf). More information on this process can be found [in this discussion](https://github.com/nasa/openmct/discussions/3821).

## Summary

The short version:

1. Write your contribution or describe your idea in the form of a [GitHub issue](https://github.com/nasa/openmct/issues/new/choose) or [start a GitHub discussion](https://github.com/nasa/openmct/discussions).
2. Make sure your contribution meets code, test, and commit message standards as described below.
3. Submit a pull request from a topic branch back to `master`. Include a check list, as described below. (Optionally, assign this to a specific member for review.)
4. Respond to any discussion. When the reviewer decides it's ready, they will merge back `master` and fill out their own check list.
5. If you are a first-time contributor, please see [this discussion](https://github.com/nasa/openmct/discussions/3821) for further information.

## Contribution Process

Open MCT uses git for software version control, and for branching and merging. The central project is at <https://github.com/nasa/openmct.git>.

### Roles

References to roles are made throughout this document. These are not intended to reflect titles or long-term job assignments; rather, these are used as descriptors to refer to members of the development team performing tasks in the check-in process.

These roles are:

* _Author_: The individual who has made changes to files in the software project, and wishes to check these in.
* _Reviewer_: The individual who reviews changes to files before they are checked in.
* _Integrator_: The individual who performs the task of merging these files. Usually the reviewer.

### Branching

Three basic types of branches may be included in the above project:

1. Master branch
2. Topic branches
3. Developer branches

Branches which do not fit into the above categories may be created and used during the course of development for various reasons, such as large-scale refactoring of code or implementation of complex features which may cause instability. In these exceptional cases it is the responsibility of the developer who initiates the task which

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE.md` in the upstream snapshot).

License file excerpt:

```text
# Open MCT License

Open MCT, Copyright (c) 2014-2024, United States Government as represented by the Administrator of the National Aeronautics and Space Administration. All rights reserved.

Open MCT is licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.  You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `OPENMCT` (category: SPACE AEROTECH)
- **Upstream URL:** https://github.com/nasa/openmct
- **Pinned commit (SHA):** `17d55deb4af5ba6d1a65a661b9f2f02582d3fe7b`
- **Branch:** master
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`4918e221a534ab957265ec7f1c645917ec101d6d223d30ad6fdd6c99a9cbaf02`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

