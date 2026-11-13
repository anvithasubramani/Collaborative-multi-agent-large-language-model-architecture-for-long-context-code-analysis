# Collaborative Multi-Agent Large Language Model Architectures for Long-Context Code Analysis

A research project comparing single-agent and collaborative multi-agent
large language model (LLM) architectures for analysing long-context
code.

## Project overview

This project investigates whether coordinating multiple specialised LLM
agents can support long-context code analysis more effectively than a
single-agent approach.

The experiments compare five architectures:

1.  **Single-Agent Baseline** -- one language model processes the
    code-analysis task.
2.  **Sequential Multi-Agent** -- multiple agents contribute in a
    defined sequence.
3.  **Planner--Reviewer** -- a planning stage is followed by a review
    stage.
4.  **Planner--Reviewer--Validator** -- planning, review, and validation
    are separated into distinct stages.
5.  **Hybrid Chunked Multi-Agent** -- long input is handled in chunks
    within a multi-agent workflow.

The project was developed as part of an MSc Data Science dissertation at
Queen Mary University of London.

## Research objectives

-   Implement and compare different single-agent and multi-agent LLM
    architectures.
-   Investigate approaches for handling long-context code-analysis
    tasks.
-   Evaluate the architectures under a consistent experimental setup.
-   Examine the strengths, limitations, and trade-offs of collaborative
    agent workflows.

## Technologies

-   **Python**
-   **Hugging Face Transformers**
-   **TinyLlama-1.1B-Chat**
-   **Google Colab**
-   **CodeSearchNet** dataset samples

## Repository structure

Adapt this structure to match the files in your actual project before
uploading:

``` text
multi-agent-code-analysis/
├── README.md
├── requirements.txt
├── notebooks/
│   └── experiments.ipynb
├── src/
│   ├── single_agent.py
│   ├── sequential_multi_agent.py
│   ├── planner_reviewer.py
│   ├── planner_reviewer_validator.py
│   └── hybrid_chunked_multi_agent.py
├── data/
│   └── README.md
└── results/
    └── README.md
```

Only include files and folders that exist in your project. If your
implementation is contained in one or more Google Colab notebooks, place
the exported `.ipynb` files in `notebooks/` and update the structure
above accordingly.

## Experimental architectures

  -----------------------------------------------------------------------
  Architecture                        General workflow
  ----------------------------------- -----------------------------------
  Single-Agent Baseline               A single LLM handles the task

  Sequential Multi-Agent              Agents process or contribute to the
                                      task in sequence

  Planner--Reviewer                   A planner produces an initial
                                      approach and a reviewer examines it

  Planner--Reviewer--Validator        A validator adds a further checking
                                      stage after planning and review

  Hybrid Chunked Multi-Agent          Long input is divided into chunks
                                      and processed through a multi-agent
                                      workflow
  -----------------------------------------------------------------------

The table describes the architecture categories. Consult the
implementation and dissertation for the exact prompts, agent
responsibilities, orchestration logic, and evaluation procedure used in
each experiment.

## Dataset

The experiments used samples from **CodeSearchNet**, a dataset for
code-related research.

The dataset files are not included in this repository by default. Follow
the dataset's official access and usage instructions, and document the
exact subset, preprocessing steps, and sampling procedure used in the
experiments.

Do not upload restricted, licensed, or large raw dataset files unless
you have confirmed that redistribution is permitted. Where possible,
provide a script or instructions for obtaining the data instead.

## Setup

### 1. Clone the repository

``` bash
git clone https://github.com/<your-github-username>/<your-repository-name>.git
cd <your-repository-name>
```

### 2. Create and activate a virtual environment

``` bash
python -m venv .venv
```

macOS / Linux:

``` bash
source .venv/bin/activate
```

Windows PowerShell:

``` powershell
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

If a `requirements.txt` file is provided:

``` bash
pip install -r requirements.txt
```

If you have not yet created a dependency file, export or record the
packages used in your working environment, review the list, and save the
verified dependencies to `requirements.txt`. Do not assume that every
package in a Colab environment is required.

## Running the experiments

The original experiments were developed using Google Colab. If notebooks
are included:

1.  Open the relevant notebook in Google Colab.
2.  Follow the notebook's setup and data-access cells.
3.  Confirm that the model and dataset paths are configured correctly.
4.  Run the cells in order.
5.  Save the resulting outputs and record the configuration used.

If you convert the notebooks into Python scripts, add the exact commands
here. For example, the following is illustrative only and must be
changed to match the actual filenames and arguments in this repository:

``` bash
python src/single_agent.py
```

Repeat with the relevant script or notebook for each architecture.

## Evaluation and results

The project compares five architectural approaches. Add a concise
summary of the actual evaluation methodology and findings from your
dissertation here.

For reproducibility, document:

-   The exact evaluation metrics and how each is calculated.
-   The dataset subset and preprocessing procedure.
-   Model and generation settings, including versions and parameters.
-   The number of runs or samples evaluated.
-   Any random seeds used.
-   Hardware and runtime constraints.
-   The results for each architecture, including limitations.

**Results summary:** Replace this paragraph with your verified findings
and, where useful, a results table copied from your dissertation. Do not
add performance figures unless they match the experiments you actually
ran.

## Reproducibility notes

LLM outputs can vary with generation settings and runtime environment.
For meaningful comparisons, keep the dataset samples, prompts, model
version, generation parameters, and evaluation procedure consistent
across architectures wherever the experimental design allows.

Record any deviations, failed runs, or manual interventions that may
affect the comparison.

## Limitations

Document the limitations identified in the dissertation. Potential areas
to discuss, if applicable to your actual experiments, include the size
and representativeness of the dataset sample, the use of a relatively
small language model, computational constraints, output variability, and
the extent to which the evaluation generalises to other code-analysis
tasks.

## Author

**Anvitha Priyaa Vellal Subramani**\
MSc Data Science, Queen Mary University of London

## Academic context

This repository accompanies an MSc Data Science dissertation titled:

*Collaborative Multi-Agent Large Language Model Architectures for
Long-Context Code Analysis.*

The repository is intended to document the research implementation and
support review and reproducibility. Please refer to the dissertation for
the full research background, methodology, analysis, and conclusions.

## Citation

If you use or refer to this work, cite the dissertation using the final
bibliographic details approved by the university:

> Vellal Subramani, A. P. (2026). *Collaborative Multi-Agent Large
> Language Model Architectures for Long-Context Code Analysis*. MSc Data
> Science dissertation, Queen Mary University of London.

Check the author-name format and year against the final dissertation
record before using this citation.

## Licence

No licence has been specified in this repository. Add a licence only
after deciding what permissions you want to grant for reuse. If this is
primarily an academic portfolio repository, you can leave the licence
unspecified while you confirm any university, dataset, and third-party
model terms.
