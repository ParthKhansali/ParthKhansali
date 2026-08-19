# GitHub Profile Setup

## 1. Create the special profile repository

GitHub only renders a profile README automatically when the repository is:

- **Public**
- named exactly the same as your GitHub username
- contains a non-empty `README.md` in its root

Example:

```text
YOUR_GITHUB_USERNAME/
├── README.md
├── metrics-languages.svg        # generated automatically
├── metrics-habits.svg          # generated automatically
├── metrics-calendar.svg        # generated automatically
└── .github/
    └── workflows/
        └── metrics.yml
```

## 2. Replace the placeholders

Before pushing, replace:

- `ParthKhansali`
- `parth-khansali`
- `parthkhansali@gmail.com`

The most important one is `ParthKhansali`.

## 3. Add the README

Copy `README.md` from this package into the root of the profile repository.

The HUD image at the top is the same public asset used by the reference profile you provided. The rest of the layout is original and uses a darker terminal/HUD structure around it.

## 4. Enable Metrics

The repository includes:

```text
.github/workflows/metrics.yml
```

This uses **lowlighter/metrics** to generate three SVG assets:

```text
metrics-languages.svg
metrics-habits.svg
metrics-calendar.svg
```

The workflow is scheduled to refresh daily and can also be triggered manually from the GitHub Actions tab.

## 5. Create the Metrics token

Create a GitHub personal access token with the minimum permissions you need.

Then go to:

```text
Profile repository
→ Settings
→ Secrets and variables
→ Actions
→ New repository secret
```

Create:

```text
Name: METRICS_TOKEN
Value: <your GitHub token>
```

The Metrics project's documented setup uses a repository secret with this name and a workflow step using `lowlighter/metrics@latest`.

## 6. Fix the workflow username

Open:

```text
.github/workflows/metrics.yml
```

and replace both/each occurrence of:

```yaml
user: ParthKhansali
```

with your real GitHub username.

## 7. Run it

Push the repository, then open:

```text
Actions → GitHub Profile Metrics → Run workflow
```

After it succeeds, the workflow commits the generated SVG files to your profile repository.

Your `README.md` already references those local files, so they will appear automatically.

## 8. Pin the right repositories

On your GitHub profile itself, pin the projects you want recruiters to see first.

For your current portfolio, a strong order would be:

1. OmniMentor
2. GEHU Connect
3. Your strongest systems / OS project
4. TaskFlow
5. One polished AI/data project
6. One strong open-source contribution

## 9. Keep the profile clean

The design intentionally avoids stacking every possible GitHub widget.

The hierarchy is:

```text
HUD banner
   ↓
terminal identity
   ↓
short about
   ↓
stack
   ↓
featured builds
   ↓
dynamic metrics
   ↓
engineering focus
   ↓
contact
```

That makes the page visually interesting without turning it into a dashboard.

## Notes

The profile uses external image services for:

- the reference HUD asset
- Skill Icons
- GitHub Readme Stats
- profile view counter

The contribution/language/habit graphics come from your own repository after the Metrics workflow renders them.

For the cleanest result, use GitHub's dark theme while viewing the profile.
