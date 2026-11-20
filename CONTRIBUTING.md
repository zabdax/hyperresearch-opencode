# Contributing

1. Fork the repository and create a branch.
2. Make a focused change. The adapter is intentionally standard-library-only;
   avoid new runtime dependencies.
3. Verify against a real hyperresearch install:

   ```powershell
   python build_opencode.py --scope global --repo <path-to-hyperresearch>
   python test_opencode.py --repo <path-to-hyperresearch> --scope global
   python build_opencode.py --scope project --repo <path-to-hyperresearch> --project <some-project>
   python test_opencode.py --repo <path-to-hyperresearch> --scope project --project <some-project>
   ```

4. If you changed the browser-fetcher translation, check the OpenCode browser
   tool names against the current OpenCode tools documentation.
5. Open a pull request with what changed and the commands you ran.

The rendered skills, agents, commands and config files are not checked into
this repository — they are produced from the upstream CLI output at install
time. `OPENCODE_INSTRUCTIONS.md` is committed for reference and regenerated on
every install. Do not hand-edit generated output; change the translation in
`build_opencode.py` instead.
