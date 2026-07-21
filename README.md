# air-app-vers

- Ref. https://github.com/untillpro/airs-design/blob/main/uspecs/specs/devops/release/app-vers--td.md

## Send a pull request

Pull requests must be opened by a member of the `DevOps_releasep` team and can target the `main` branch of `untillpro/air-app-vers`.

To send a pull request from a fork:

```bash
# Fork and clone the repository
gh repo fork untillpro/air-app-vers --clone
cd air-app-vers

# Commit your changes to main and push them to your fork
git switch main
git add <changed-files>
git commit -m "<commit-message>"
git push origin main

# Open a PR from your fork's main branch to the upstream main branch
gh pr create --repo untillpro/air-app-vers --base main --head <github-username>:main
```

## Run tests

```bash
# Install dependencies
pip install coverage pyyaml lingua-language-detector

# Run tests
python scripts/validate.py

# Or, run tests with coverage and generate a report
coverage run --source=scripts -m unittest discover scripts -v
coverage run --source=scripts -a scripts/validate.py
coverage html
```

## Manual validate

```bash
./validate.sh
```
