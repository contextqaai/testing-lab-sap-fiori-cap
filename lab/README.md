# ContextQA lab — SAP web · Fiori / UI5 / CAP

Educational source fork of [SAP-samples/ui5-cap-event-app](https://github.com/SAP-samples/ui5-cap-event-app). Original history, notices and license are retained. This is not an endorsed integration or a customer production app.

**Status: source and exercises available. Public deployment, platform import and ContextQA run results are not verified.**

Starting source commit: `e8d098f8cebe7e984b20b71dddccfd6260d981b0`.

## Setup and scope

Use upstream npm install/build guidance. Development mode uses in-memory data and sample credentials; production auth/database configuration is not supplied by the sample. This is a UI5/CAP event app, not ECC, S/4HANA or native SAP GUI. Public multi-user hosting needs its own identity and isolated data.

Follow the [original setup instructions](../README.md#upstream-project-documentation). See [stack/platform guidance](https://github.com/contextqaai/testing-lab/blob/main/PLATFORMS.md) for deployment boundaries.

## Exercises

| Scenario | Explicit assertion |
|---|---|
| Event form | The seeded event can be opened in the registration UI. |
| Registration | A synthetic attendee submission produces the defined result. |
| Administrator view | An authorized test administrator can find the selected registration. |
| Draft behavior | The chosen draft flow behaves as documented for that form. |
| Role boundary | Desired deployment requirement: a regular user cannot access administrator data. Verify real auth setup first; local sample credentials do not prove this. |

These are acceptance exercises, not claims that upstream currently satisfies each desired requirement. Inspect the implemented workflow and fixtures before generating executable steps. Missing validation/auth may deliberately demonstrate a failure and must be disclosed.

## End-to-end lesson

Start an owned/authorized copy with synthetic fixtures. State the assertion, create/review a test in your authenticated ContextQA workspace, execute, and inspect the actual verdict. Introduce one disclosed regression in a separate variant, rerun the same assertion, fix the app and rerun. Confirm mutations against disposable data. Keep credentials and private reports out of this repository.

Record app commit/build, fixture/scenario version, browser/runner version, environment and timestamp with every real report. A cached report is recorded evidence, not a new run. No ContextQA report has been generated for this fork yet.

[ContextQA setup](https://contextqa.com/tutorials/getting-started-with-contextqa-test-automation/) · [Central catalog](https://github.com/contextqaai/testing-lab)
