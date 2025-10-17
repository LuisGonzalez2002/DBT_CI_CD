# LP-12-SDG-DBT
LP-12 — dbt CI/CD Sandbox

This repository is a hands-on sandbox to experiment with dbt end-to-end: modeling, testing, documentation, and the Semantic Layer (metrics, dimensions, entities). It also includes a practical CI pipeline with dbt Cloud wired to GitHub Pull Requests. On every PR, a dbt Cloud job installs deps and runs dbt build (models + tests + docs) in an isolated schema; the PR is blocked until the build passes, ensuring only green changes reach main.

Highlights

Models organized by layers (staging, dimensions, facts, semantic models).

Generic & custom tests, snapshots, seeds, and auto-generated docs.

Semantic Layer examples to define and query metrics consistently.

CI: PR-triggered dbt Cloud job + merge protection on main.

Security: credentials and local settings kept out of VCS (.env, profiles.yml).

Quick start

Install dbt and configure your warehouse in ~/.dbt/profiles.yml.

From the project root: dbt deps && dbt build

Open a Pull Request to see the CI checks in action.

This project was created for working in dbt cloud but it could be adapted for dbt core.

Dataset notice: The original dataset has been removed from this repository due to privacy and copyright restrictions. Please use your own data source or synthetic/sample data when running the project.
