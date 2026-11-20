<!-- hyperresearch-opencode-adapter:start -->
## Deep research routing (hyperresearch)

When the user asks for deep research, a literature review, a multi-source
analysis, or a cited research report, load the `hyperresearch` skill
(`skill` tool, id `hyperresearch`) and run its pipeline. Do not answer such a
request inline from your own knowledge. The deliverable is
`research/notes/final_report_<vault_tag>.md` in the current project, and a run
is complete only when `F:/hyperresearch-skill/.venv/Scripts/hyperresearch.exe run finish <vault_tag> --json` reports
`passed: true`. `/hyperresearch <question>` is the explicit entry point.
<!-- hyperresearch-opencode-adapter:end -->
