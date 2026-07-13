# TERMS OF USE, CUSTODY DISCLAIMER, AND LIABILITY MITIGATION

**Last Updated:** July 2026

## 1. Operating Mechanics and Data Custody
The "Software Architecture Interview Skill" (hereinafter "Skill") provided in this repository operates exclusively as a set of static logical routing rules (Markdown scripts) executed by the user's chosen Local or Cloud Large Language Model (LLM) client.

- **No Proprietary Storage:** The Skill does not possess, operate, or maintain any backend servers, cloud storage, or proprietary databases. 
- **Pass-Through Execution:** The Skill operates in a strict "Pass-Through" mode. When executing commands (such as `/interview docs` or `/interview resume`), the contents of your local directories are intercepted by your chosen LLM platform (e.g., OpenAI, Google, Anthropic, local runners) to generate the architectural context.

## 2. Privacy and Data Handling (LGPD/GDPR)
Because the Skill relies entirely on third-party LLMs to process text:
- The responsibility for data privacy, confidentiality, and GDPR/LGPD compliance lies **exclusively** with the Terms of Service of the specific LLM provider you have chosen to run this Skill.
- The author(s) and maintainer(s) of this repository do not collect, intercept, or have access to any data generated or read during the execution of this Skill.

## 3. Strict Prohibitions and User Responsibility
**WARNING:** It is strictly prohibited and highly unadvised to execute this Skill against directories or files that contain:
1. Real Personally Identifiable Information (PII) of clients or users (e.g., emails, social security numbers).
2. Hardcoded API Keys, production passwords, or database credentials.
3. Confidential Trade Secrets or proprietary intellectual property that has not been sanitized.

The AI agent will absorb the full text of the targeted files. **Injecting sensitive files into the LLM context window is a strict operational risk assumed solely by the operator.**

## 4. Limitation of Liability ("AS IS" Clause)
This project is an Open-Source tool distributed freely under the "AS IS" premise. 
- The author(s) provide no implied or explicit warranties regarding the tool's fitness for a particular purpose, nor do they guarantee an absence of operational bugs or compatibility issues with third-party APIs.
- The author(s) shall be held unconditionally and legally harmless from any and all civil liabilities, damages, or losses resulting from data leaks, intellectual property exposure, or financial costs (e.g., excessive token consumption) caused by the user's execution of this Skill.

By cloning, downloading, or executing this Skill within any environment, you explicitly acknowledge and agree to assume full responsibility for the data you provide to the LLM and the costs associated with its operation.
