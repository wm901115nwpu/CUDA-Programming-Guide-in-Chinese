# AGENTS.md

## Project Overview

This repository is a Chinese translation of the [CUDA C Programming Guide](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html). It is based on [HeKun-NVIDIA/CUDA-Programming-Guide-in-Chinese](https://github.com/HeKun-NVIDIA/CUDA-Programming-Guide-in-Chinese) and has been further refined with corrections to grammar, key terminology, sentence structure, and content completeness.

## Repository Structure

Each chapter and appendix lives in its own directory, with the Markdown file inside following the established naming convention:

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
- **Terminology**: Use standard GPU/CUDA terminology in Chinese (e.g., 线程块 for thread block, 共享内存 for shared memory, 内核 for kernel, 流式多处理器 for streaming multiprocessor). Prefer consistency with the existing translated chapters.
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
