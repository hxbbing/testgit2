# RTL2REASON

Code for **Source-Grounded Reasoning Alignment for Sequential RTL Design**.

## Overview

RTL2REASON improves LLM-based sequential RTL generation by constructing source-grounded reasoning traces from reference RTL and incorporating them into supervised fine-tuning. The framework emphasizes temporal dependencies among register updates, state transitions, and control conditions.

## Method

- **Bottom-up temporal information extraction:** Extract clock and reset behavior, state transitions, and register-update conditions from reference RTL through program analysis.
- **Template-based reasoning reconstruction:** Organize the extracted information into structured reasoning traces grounded in the source implementation.
- **Temporal-aware supervised fine-tuning:** Assign greater training weight to temporal-related tokens to emphasize sequential behavior.

## Evaluation

We evaluate RTL2REASON on **SeqRTLBench**, our benchmark of **306 sequential RTL tasks**, and the general benchmark of **VerilogEval**, using **pass@1**, **pass@5**, and **pass@10**.
