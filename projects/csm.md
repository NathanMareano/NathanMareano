# CSM

**Offline invoice-reference review · HHCIS project contribution · Working prototype**

[Back to profile](../README.md) · [Full walkthrough](https://nathanielmareano.com/projects/csm/)

![CSM desktop results showing separate invoice, Article, and diagnosis-pair evidence views](../assets/csm-results.png)

*Native v0.4.0 screen using generated synthetic invoices and demonstration Article references. No patient records are shown; visible timings describe one local test.*

## Why I built it

An invoice-level result is difficult to review when its underlying reference is hidden. Through project contributions to H&H Continuous Improvement & Services LLC, I built an offline prototype that keeps invoice inputs, reference comparisons, and review history in one workspace.

## My contribution

I built the Python prototype and helped shape it into a native application with managed datasets, searchable results, review history, and packaged delivery. I tested the packaged application with synthetic inputs.

**Stack:** Python, Tk, SQLite, PyInstaller.

## How it works

1. Import invoice CSVs and supplied CMS Billing & Coding Article reference tables into local storage.
2. Check the selected inputs before running a review.
3. Compare procedure and diagnosis pairs against applicable Article versions while retaining separate evidence for each reference.
4. Search invoice, Article, and diagnosis-pair results; save review history and export the output.

## Decisions that matter

- **Preserve each reference.** One supporting Article does not erase a different result from another Article.
- **Keep ambiguous cases reviewable.** Unclear mappings can remain flagged for manual review instead of being forced into a yes/no result.
- **Contain the workflow.** Local datasets, native controls, and saved history keep the evidence available after a run finishes.

## Current status

The functional prototype has been tested with synthetic inputs. Its output is reference-screening evidence, not a coverage determination or finding of improper billing. Demonstration Articles are test references rather than an official CMS extract. Operational use would require validation against the recipient's actual file mappings and workflow.

The source code is private. This page shares the application workflow using synthetic examples.
