# AGENTS.md

## Project Overview

This repository is a Chinese translation of the [CUDA C Programming Guide](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html). It is based on [HeKun-NVIDIA/CUDA-Programming-Guide-in-Chinese](https://github.com/HeKun-NVIDIA/CUDA-Programming-Guide-in-Chinese) and has been further refined with corrections to grammar, key terminology, sentence structure, and content completeness.

## Repository Structure

Each chapter and appendix lives in its own directory, with the Markdown file inside following the same naming pattern as the directory:

```
第1章CUDA简介/
    第一章-CUDA简介.md
第2章CUDA编程模型概述/
    第二章CUDA编程模型概述.md
...
附录B对C++扩展的详细描述/
    附录B对C++语言扩展的详细描述.md
...
Readme.md       ← project index with completion status
AGENTS.md       ← this file
```

The `Readme.md` tracks which chapters/appendices have been fully proofread (`[x]`) and which are still pending (`[ ]`).

## Content Conventions

- **Language**: All translated content must be written in Simplified Chinese.
- **Terminology**: Use standard GPU/CUDA terminology in Chinese (e.g., 线程块 for thread block, 共享内存 for shared memory, 内核 for kernel, 流多处理器 for streaming multiprocessor). Prefer consistency with the existing translated chapters.
- **Formatting**: Follow the Markdown style already used in each file — headings, code blocks (` ``` `), inline code (`` ` ` ``), tables, and math expressions should match the conventions found in the completed chapters (第1章–第5章 and 附录A).
- **Code samples**: Preserve original CUDA C/C++ code snippets exactly; do not translate code. Add Chinese comments where useful.
- **Images/figures**: Reference images using relative paths. Do not alter or delete existing figure files.

## Completion Status

Chapters 1–5 and Appendix A are marked as proofread. Appendices B–N are translated but not yet fully proofread. When making edits, update `Readme.md` to mark a section as `[x]` only after a thorough review pass.

## Contribution Guidelines for Agents

1. **One section per commit**: Limit each commit to changes within a single chapter or appendix directory plus any corresponding `Readme.md` update.
2. **Proofread before marking complete**: Verify that terminology is accurate and consistent with other completed sections before setting `[x]` in `Readme.md`.
3. **Do not translate code**: CUDA code blocks must remain in their original English/C++ form.
4. **No new top-level files**: Do not create additional Markdown files at the repository root unless explicitly asked.
5. **Preserve directory names**: Directory and file names use Chinese characters as established; do not rename them.
6. **Branch**: Develop on the branch specified in the task instructions and open a pull request targeting `main`.

## Cursor Cloud specific instructions

This is a pure Markdown documentation repository with no build system, runtime services, or test frameworks. The development workflow is editing and linting `.md` files.

### Available tooling

- **Linting**: `markdownlint '**/*.md' --ignore '.git'` (installed globally via npm). The repo has many pre-existing style issues (6000+); most are line-length (MD013) and inline-HTML (MD033). When proofreading, focus on content correctness rather than satisfying all lint rules.
- **Preview**: `grip <file.md> 0.0.0.0:6419` renders GitHub-flavored Markdown locally (installed via pip). Useful for verifying formatting of tables, code blocks, and headings.

### Known issues

- Image references in Markdown files point to `.png` files that are **not present** in the repository. This is pre-existing; do not attempt to fix unless explicitly asked.
- The `Readme.md` links to `附录A支持GPU设备列表/附录A支持GPU设备列表.md` but the actual directory is `附录A支持CUDA的设备列表/`. This is a known path discrepancy.

### Workflow for proofreading tasks

1. Read the target appendix/chapter Markdown file.
2. Compare terminology and formatting against completed chapters (第1章–第5章).
3. Make corrections, commit, and update `Readme.md` checkbox if fully reviewed.
4. Run `markdownlint <file> --disable MD013 MD033` to check for structural issues (ignore line-length and inline-HTML for Chinese content).
