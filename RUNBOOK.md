# Automation Runbook

This repository demonstrates the full GitHub automation loop: repo setup, a manually
triggered Actions pipeline, a short branch with a pull request, and a review.

## How to trigger the pipeline by hand

The pipeline in this repo (`.github/workflows/baseline.yml`) is named
**Baseline Demo Pipeline** and is configured with a `workflow_dispatch` trigger, so it
does **not** run on every push — it only runs when triggered manually.

To trigger it by hand:

1. Open the repository on GitHub: `mcpmark-eval-liuhezi/gh-automation-baseline`.
2. Click the **Actions** tab in the top navigation bar.
3. In the left sidebar, select **Baseline Demo Pipeline**.
4. On the right side, open the **Run workflow** dropdown.
5. Choose the branch you want to run against — `main` or `demo/runbook`.
6. Click the green **Run workflow** button.

The run starts immediately and consists of a single job, `baseline`, whose only step
prints the line:

```
baseline pipeline executed
```

Once the run finishes, click into it to inspect the job logs — you should see the exact
line above under the "Print baseline line" step.
