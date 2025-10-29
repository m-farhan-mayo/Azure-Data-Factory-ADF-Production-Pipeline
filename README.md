# Azure-Data-Factory-ADF-Production-Pipeline


This repository contains a complete backup of a live production environment from Azure Data Factory. The project is structured as a series of exported ZIP archives, each representing a key component or version of the data pipeline.

The file names indicate a sophisticated ADF setup that includes:

Git Integration: Version control for the data factory (CI/CD).

Orchestration: A "manager" pipeline that controls other pipelines.

Multiple Environments: Separate "Production" (Pro) and "Variable" (Var) pipelines, suggesting a DEV/TEST/PROD workflow.

File Breakdown (Project Recall)
Here is what each archive likely contains, helping you recall the project's structure:

1_CopyData_support_live

Purpose: This is the foundational pipeline. It likely contains a simple Copy Data Activity used for the initial data ingestion (e.g., moving raw files from a source to a staging layer).

PipelineGit_support_live

Purpose: This is the core of the project. It's the ARM template (JSON definitions) exported from the live Git-enabled branch (e.g., adf_publish). This single archive contains the code for all linked services, datasets, and pipelines in your data factory.

pipelineManager_support_live

Purpose: This is the Orchestrator or "master" pipeline. Its job was to control the entire workflow by triggering other pipelines in the correct sequence, possibly using "Execute Pipeline" activities.

ProPipeline_support_live

Purpose: This is the main Production pipeline. It contains the stable, tested, and primary business logic for your data transformations.

VarPipeline_support_live

Purpose: This is the "Variable" or "Variant" pipeline. This was likely a development/feature branch, or a version of the pipeline that made heavy use of parameters and variables for dynamic execution.

SelectedFiles_support_live

Purpose: A miscellaneous backup. This was probably a manual export of specific components (like a single dataset or linked service) that you needed for debugging or testing.
