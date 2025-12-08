# ATML PA5

Summary based on the accompanying report (`ATML_PA5.pdf`) and the three task notebooks in this repository.

## Project layout
- `Task 1/Task1.ipynb` — LLM decoding strategy analysis; explores different decoding methods and compares metrics.
- `Task 2/Task2.ipynb` — Alignment experiments with DPO, PPO, and GRPO, including reward-model training; saved checkpoints live in the corresponding `*_aligned_model/` and `reward_model/` folders.
- `Task 2/Task2_results_plots.ipynb` — Stand-alone notebook that visualizes evaluation CSVs (`aligned_eval_summary.csv`, `reward_eval_samples.csv`, `verbosity_bias_eval.csv`, `verbosity_length_eval.csv`) and training curves (reward/KL and losses from PPO/GRPO/DPO and the reward model).
- `Task 3/Task3.ipynb` — Universal Sparse AutoEncoders (USAE) implementation with model hooks and class utilities.
- `ATML_PA5.pdf` — Report write-up for the assignment.

## How to run
1. Use Python 3. Install needed Python packages (pandas, seaborn, matplotlib, torch/transformers/trl for the alignment notebooks) in your environment.
2. Open each notebook in Jupyter or VS Code. Run top-to-bottom; the notebooks are self-contained and expect the saved CSVs and model folders to remain in place.
3. For a quick view of results without rerunning training, execute `Task 2/Task2_results_plots.ipynb`.

## Artifacts and results
- Alignment metrics: `Task 2/aligned_eval_summary.csv`
- Reward model inspection: `Task 2/reward_eval_samples.csv`
- Verbosity evaluations: `Task 2/verbosity_bias_eval.csv`, `Task 2/verbosity_length_eval.csv`
- Training logs: `Task 2/*_aligned_model/*_training_logs.csv`, `Task 2/reward_model/rm_training_logs.csv`
- Saved models: `Task 2/dpo_aligned_model/`, `ppo_aligned_model/`, `grpo_aligned_model/`, `reward_model/`

Refer to the PDF report for detailed methodology and discussion of results; use the notebooks for code, reproduction, and visualizations.
