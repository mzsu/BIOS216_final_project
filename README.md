# README

## Authors

Morgan Su


## File structure

Combining resources across OSF and GitHub should yield the following structure.

```
├── .gitignore          <- Lists files to be ignored in syncing between local and remote.
├── README.md           <- Describes the project and orchestration (how to run)
│
├── code
│   ├── data_processing <- Code to process data from raw all the way to tidy.
│   │   └── <experiment>
│   ├── data_analysis   <- Code that operates on tidy data for draft data analytics and visualizations.
│
├── output
│   ├── <experiment>    <- Tables and figures from the data analysis
│
├── publication                      
│   └── journal                      <- Journal that this was submitted to
│       └── submission-1_YYYY-MM-DD  <- All materials of submission 1
│           ├── docs                 <- All documents for submission
│           ├── figures              <- All figures for submission
│           └── tables               <- All tables for submission
│
├── deps.R              <- Import packages not used elsewhere to help renv
├── renv.lock           <- Lockfile with all dependencies managed by renv
└── renv                <- Package dependency management directory with renv
```


## Code structure

All code follows the following structure.

```
├── Title
│   ├── Inputs          <- Define the input sources.
│   └── Outputs         <- Define the outputs.
│
├── Setup
│   ├── Import          <- Import modules.
│   ├── Parameters      <- Input parameters (e.g., data definitions)
│   ├── Configs         <- Input any configurations (e.g., source data, % sampled).
│   └── Functions       <- Define all functions.
│
├── Read
│   ├── Import          <- Import data.
│   └── Conform         <- Conform data to a format appropriate for analysis.
│
├── Compute
│   └── Compute - <Analysis type>   <- Compute descriptive statistics, visualize, analyze.
│       └── <Analysis subtype>      <- Analysis subtype (if applicable; e.g., histograms).
│
├── Write
│   ├── Conform         <- Conform data to a format appropriate for storage.
│   └── Export          <- Write/push/sink data to a storage service.
│
├── Reproducibility
│   ├── Linting and styling
│   ├── Dependency management
│   └── Containerization
│
├── Documentation
    ├── Session info
    └── References
```


## How to get the data

As of the time of writing, these are on a Share Drive on Google Drive [here](https://drive.google.com/drive/u/1/folders/0AHwZeCcC1chbUk9PVA).


## How to run

### From source

To run this code, use the following diagramatic acyclic graph (DAG). Note that this applies for each experiment. Note that you need to combine all resources first into one repository to run.

![How to run diagram](https://github.com/serghiou/repo-template/blob/main/how-to-run.jpg?raw=true)


## How to get help

If you encounter a bug, please file an issue with a minimal reproducible example [here](https://github.com/serghiou/repo-template/issues) and please Label it as a "bug" (option on the right of your window). For help on how to use the package, please file an issue with a clearly actionable question [here](https://github.com/serghiou/repo-template/issues) and label it as "help wanted." For all other questions and discussion, please email the first author.
