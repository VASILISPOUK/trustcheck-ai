# TrustCheck AI

TrustCheck AI is a transparent, rule-based prototype for first-pass assessment of AI-generated answers. It helps users identify visible risk signals and decide when an answer should be verified by a person or a reliable source.

Built for the MANOLO Innovation Lab - Trustworthy AI & Innovation Lab, Thessaloniki, August 2026.

## The problem

AI answers can sound convincing even when they include unsupported claims, overconfident language, sensitive advice, or visible personal data. Users need a lightweight, understandable way to notice when an answer deserves extra scrutiny.

## What TrustCheck AI checks

- **Claim evidence** - flags factual claims or numbers without an obvious source.
- **Certainty and language** - flags absolute wording such as "always", "never", and "guaranteed".
- **Sensitive context** - flags health, legal, and financial topics where errors may have higher consequences.
- **Personal data** - flags visible email addresses and phone numbers.

The application produces a **Trust Score** and a **Trust Card**. The card gives a plain-language explanation for each signal and recommends either **Low risk** or **Human review**.

## Important limitation

TrustCheck AI is **not a truth detector**. It cannot prove that an AI answer is true or false. It makes visible, explainable risk signals so that users can decide when verification or human oversight is appropriate.

## Running the prototype

Open the deployed prototype:

https://trustcheck-ai.vasilispouk.chatgpt.site

To use it:

1. Enter the original question in **User question**.
2. Paste the generated output in **AI answer**.
3. Select **Check trustworthiness**.
4. Read the Trust Card and its explanations.

## Evaluation plan

For the Innovation Lab evaluation, test the prototype on 10-15 manually designed scenarios. Before each test, record the expected signal. Then compare the expected signal with the Trust Card produced by the tool.

Suggested scenarios include:

| Scenario | Expected signal |
| --- | --- |
| Medicine and alcohol | Human review - health context and absolute language |
| Investing all savings in one company | Human review - financial context and absolute language |
| Answer containing an email and a phone number | Human review - personal data |
| Study advice that acknowledges limitations | Low risk |

## Trustworthy AI alignment

The prototype is designed as a small monitoring and auditing tool. Its main alignment points are:

- **Transparency and explainability:** every signal is based on visible rules and includes an explanation.
- **Human agency and oversight:** it explicitly recommends human review in higher-risk situations.
- **Safety:** it treats health, legal, and financial content as sensitive contexts.
- **Privacy:** it highlights visible contact details.
- **Accountability:** the checks and limitations are documented and reproducible.

## Future work

- Expand the evaluation dataset and measure precision and recall for each risk signal.
- Add source-verification and citation-quality checks.
- Support more languages and configurable domain-specific rules.
- Integrate the checks into a model-response workflow or the MANOLO framework.

## License

This project is released under the Apache License 2.0. See [LICENSE](LICENSE).
