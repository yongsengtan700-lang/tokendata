# TokenData Gateway

**An OpenAI-compatible gateway that hard-stops runaway API spend at a budget you set.**

Unlike observability tools that send you an email *after* you burn $80, TokenData Gateway acts as a FinOps execution layer. It intercepts requests, attributes costs to virtual keys, and blocks calls the moment a budget is exceeded.

## How it works
1. Generate a Virtual Key (`td_xxx`).
2. Point your OpenAI SDK `base_url` to this gateway.
3. Set a hard USD budget.
4. The gateway returns `402 Payment Required` when the limit is hit.
