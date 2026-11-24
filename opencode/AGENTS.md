# Global Agent Instructions

## OpenCode Tool Usage

- Use `read`, `grep`, `glob`, and `shell` directly for file reads, content
  searches, file discovery, and terminal commands.
- Use `edit` or `write` directly when modifying files.
- Never call filesystem or shell tools from inside `execute`; Code Mode has no
  filesystem or shell access.
- Do not search the Code Mode catalog for built-in tools such as `read`,
  `grep`, `glob`, or `shell`; they are never listed there.
- Use `execute` only for orchestrating tools explicitly listed in the Code
  Mode catalog and for parallel operations. Verify a tool's presence in the
  catalog before calling it; never guess tool names.
