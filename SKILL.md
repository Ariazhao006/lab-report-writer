---
name: lab-report-writer
description: Write, continue, organize, or format course lab reports, or generate experiment guides from experiment manuals. Use when the user asks for an experiment guide, operation guide, pre-lab report, lab report, continuation of a specific experiment section, continuation in the style of an existing report, or report content based on experiment manuals and result screenshots.
---

# Lab Report Writer

## Core Principles

Read the materials before writing. Do not draft report content until you understand the experiment manual, the report template, the existing report structure, and the available results.

Respect the project template strictly. If the project folder contains a Word, PDF, LaTeX, or other report template, inspect it first and reproduce it in LaTeX as fully as practical.

Write from the experiment instructions and the actual results. Existing reports and example reports may guide structure and style, but never copy them. Reorganize and rewrite in original wording; avoid mechanical paraphrasing.

Do not invent results. If screenshots, data tables, or user notes do not support a result or conclusion, leave a placeholder, mark it as pending, and ask the user.

## Start-Up Checks

Before starting, confirm both the target experiment and the task type.

If the user states the experiment number, experiment name, instruction file, result images, or result files, use that information directly.

If the user does not identify which experiment to work on, ask for the experiment number or experiment name.

If the user maps files explicitly, such as saying a specific file is the manual, template, or result file, prioritize those files. Do not rely only on filename guesses.

## Task Type Selection

Choose one of the following three task types based on the user's request. If the user clearly asks for one type, complete only that type.

1. **Experiment guide**: If the user asks for an experiment guide, operation guide, "how to do the experiment," "walk me through it step by step," or "start from zero," generate a beginner-friendly `实验指南.md`.
2. **Pre-lab report**: If the user says the experiment has not been performed yet, or asks for a pre-lab report, preparation section, pre-experiment content, or "everything before results," fill only the report sections before experiment results.
3. **Complete lab report**: If the user asks for a complete report, formal report, report completion, report based on results, result analysis, conclusion, or thinking-question answers, follow the complete report workflow.

If the user's wording does not clearly indicate which task type they need, ask whether they want an experiment guide, a pre-lab report, or a complete lab report. Do not guess and begin writing.

## Reading Order

1. Inspect the project folder structure and identify experiment manuals, instruction PPT/PDF files, report templates, existing reports, result images, code files, example reports, and the LaTeX project location.
2. For an experiment guide, read experiment-manual-style documents first and understand the full process from software startup, project creation, code writing, running, verification, to result saving.
3. For a pre-lab report or complete lab report, read the report template or existing report and extract the formatting and writing structure.
4. Read the current experiment manual or instruction PPT. Understand the objectives, principles, devices, procedure, record tables, thinking questions, and submission requirements.
5. For a complete lab report, read the result materials. Results are often screenshots, photos, record tables, simulation outputs, logs, or user notes.
6. If earlier experiments already exist in the same report, imitate that report's structure, heading hierarchy, tone, and figure-text organization for later experiments.
7. If the user provides someone else's report as an example, imitate only the structure and level of detail. Do not copy its sentences, paragraphs, or personal information.

## Template and LaTeX Requirements

When the deliverable is in LaTeX, usually for pre-lab reports and lab reports:

- Create or maintain a clear LaTeX project structure, such as `main.tex`, `preamble.tex`, `metadata.tex`, `chapters/`, and `figures/`.
- Except for local details such as minor headings, lists, figures, and tables, the overall report layout must follow the experiment template in the project folder. Reproduce the cover page, table of contents, experiment titles, experiment information blocks, body heading levels, captions, table style, page margins, fonts, headers, and footers as closely as practical.
- If the template comes from a Word report, inspect the DOCX content and structure first. When needed, check paragraph styles, table content, image order, page margins, and title formatting.
- Do not omit school emblems, wordmarks, college names, course fields, underlined fields, scoring fields, or other template elements.
- A skill may include common logos, emblems, and template assets in `assets/`. If this skill's `assets/` folder provides SCUT emblems or wordmarks, use them when the template needs those images but the project folder does not provide them, which covers many South China University of Technology lab-report scenarios. If the template uses special icons, college marks, course-specific graphics, or school-specific assets that are absent from both the project folder and the skill assets, ask the user to provide the images. Do not fabricate icons or substitute mismatched graphics.
- By default, use normal LaTeX `section`, `subsection`, and `subsubsection` formatting for headings and list-like divisions. Only switch to manual Chinese-style divisions such as `一、`, `1.`, and `（1）` when the user specifically asks to match the template's divisions, keep the template numbering, use that style, or when the template clearly requires manual numbering.
- For Chinese reports, prefer XeLaTeX with `ctex`.
- It is acceptable to copy images to stable LaTeX figure folders and rename copies with clear ASCII filenames, but do not delete the user's original images.
- After edits, check image references, package requirements, and paths.

## Report Content

A complete lab report commonly includes:

- Experiment objectives
- Experiment principles
- Experiment environment or equipment
- Experiment content or procedure
- Experiment results
- Result analysis
- Experiment conclusion
- Answers to thinking questions
- Reflection or learning summary

Use the template and the experiment manual as the authority for the actual section list. If the manual includes special record tables, operation steps, FAQ items, notes, or thinking questions, reflect them in the report instead of omitting them.

## Experiment Guide

When the task type is experiment guide, generate `实验指南.md` in the project folder. The guide must assume the user has no experience. Make it detailed, plain, and actionable. Explain necessary concepts, but avoid obscure wording and meaningless analogies.

The experiment guide should cover the complete workflow from zero. Based on the experiment type and manual, include:

- Experiment content: what the experiment must complete, verify, and submit.
- Before each sub-experiment, write a short explanation for the user: what this sub-experiment does, what the prompt requires, why the operation is needed, and what they should expect to observe. Keep the language plain while preserving the tone of an academic report; do not add empty analogies.
- File organization: if the experiment is performed on the user's computer and involves multiple files, suggest a file tree. For example, create `lab1/` in the project folder, then create `.m`, `.v`, `.tex`, and image-output folders inside it.
- Software operation: start from opening the experiment software, such as Matlab, Quartus, Multisim, Vivado, Proteus, Keil, oscilloscope/signal-generator companion software, or similar tools. Cover project creation, file import, parameter configuration, running, simulation, compilation, downloading, and result saving.
- Code and commands: if the experiment requires code, provide code that can be used directly or adapted according to the manual. For Matlab-style experiments that generate figures, include automatic figure-saving code and set clear titles, axis labels, legends, and output filenames.
- Hands-on procedure: for physical experiments, circuit experiments, hardware wiring, and instrument adjustment, strictly follow the experiment manual and state the wiring, parameter settings, measurement order, recording method, and notes.

Guide steps must be grounded in experiment-manual-style files in the project folder. If a necessary operation is not described in the manual but must be added so the user can complete the experiment, explicitly mark it as "supplemented according to common software/instrument workflows; not explicitly stated in the experiment manual." Do not present inferred steps as manual requirements.

## Pre-Lab Report

When the task type is pre-lab report, read the report template and fill all sections before experiment results, such as objectives, principles, environment, design, expected procedure, pre-lab key questions, and pre-lab thinking questions. Do not write results, result analysis, conclusions, or reflection content that depends on actual results.

If the template requires result, analysis, or conclusion sections but the user only asks for a pre-lab report, leave those sections blank in the template style.

## Complete Lab Report

When the task type is complete lab report, follow the full workflow in this skill. Use the result materials to write experiment results, result analysis, conclusions, thinking-question answers, and reflections as required by the report template.

If the user later provides results after a pre-lab report has already been written, append or revise the result-related sections while preserving the existing style.

## Writing Standards

Use formal, natural student lab-report language. Be clear and specific. Avoid both overly casual phrasing and machine-like template filler.

Understand the experiment from the manual rather than merely summarizing it. Explain the relationship between objectives, core principles, procedure, and results.

In the principles section, focus on the devices, signals, formulas, and data paths actually used in the experiment. Avoid unrelated encyclopedia-style background.

In the procedure section, describe the operation flow using the manual and actual screenshots.

In result analysis, tie each claim to a screenshot or record table. Explain the phenomenon, output value, flag value, whether it matches expectations, and why.

Answer thinking questions one by one. Provide reasoning, not only conclusions.

## Using Example Reports

If the user provides an example report:

- Use it to learn section order, level of detail, table layout, and answer style.
- Do not copy its sentences, paragraphs, captions, reflection text, or personal information.
- If the example contains errors, omissions, or weak reasoning, correct them based on the instruction materials instead of inheriting them.
- Make the final report fit the user's own experiment materials and results.

## Using Result Images

Users often place experiment screenshots in the project folder and specify filenames or order.

- Confirm that each image exists.
- Preserve the user-specified order when images must be inserted in order.
- For stable LaTeX references, copy images to `figures/<experiment>/` and rename copies with clear English filenames.
- Give every important image a meaningful caption.
- Captions should describe the experiment state or result, not just say `Image 1`.
- If an image is unclear, write only what is supported by visible information; ask the user when interpretation would be guesswork.

## Quality Check

Before finishing, check that:

- The current experiment manual or instruction PPT has been read and its key requirements are reflected.
- If the task is an experiment guide, `实验指南.md` has been generated and covers the complete process from software/instrument startup to result saving.
- User-specified result images or data have been used correctly.
- The report template's formatting characteristics have been preserved and reproduced.
- Example reports have not been copied.
- There are no fabricated data, missing thinking questions, missing images, incorrect image order, or broken LaTeX paths.

## Delivery

Prefer directly editing the project report or LaTeX files instead of only giving advice.

In the final response, briefly state:

- Which files were modified.
- Which images were added or referenced.
- Whether compilation or static checks were completed.
- Any remaining items the user needs to confirm or provide.
