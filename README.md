<div align="center">
  <a href="https://xmake.io">
    <img width="160" height="160" src="https://xmake.io/assets/img/logo.png">
  </a>

  <h1>xmake-skills</h1>

  <div>
    <a href="https://github.com/xmake-io/xmake-skills/blob/master/LICENSE.md">
      <img src="https://img.shields.io/github/license/xmake-io/xmake-skills.svg?colorB=f48041&style=flat-square" alt="license" />
    </a>
    <a href="https://discord.gg/xmake">
      <img src="https://img.shields.io/badge/chat-on%20discord-7289da.svg?style=flat-square" alt="Discord" />
    </a>
  </div>

  <b>Agent Skills for Xmake</b><br/>
  <i>A collection of Claude Agent Skills that teach AI assistants how to use Xmake effectively.</i><br/>
</div>

## Introduction ([中文](/README_zh.md))

**xmake-skills** is a collection of [Agent Skills](https://www.anthropic.com/news/agent-skills) for [Xmake](https://xmake.io), the cross-platform build utility based on Lua. These skills give AI coding assistants (such as Claude Code) the knowledge they need to create, configure, build, debug, and package Xmake projects correctly.

Each skill packages up focused Xmake know-how — from writing `xmake.lua` to integrating C/C++ packages — so AI agents can produce idiomatic, working Xmake configurations instead of guessing.

See [`skills/`](./skills/) for the full list and layout.

> **Context cost:** The 53 skill trigger descriptions (frontmatter `description` fields) consume about 4k tokens in total. These are always loaded so the agent knows which skills are available. The full skill body is only loaded on demand when the task matches the description — so you get comprehensive Xmake coverage without wasting context.

## Why

Large language models often know *about* Xmake but get the details wrong: outdated APIs, wrong option names, broken package syntax. Skills fix this by loading just the right documentation and examples into the agent's context when it is actually working on Xmake.

## Usage

### Claude Code (recommended)

**Install from GitHub:**

```bash
claude plugins install xmake-io/xmake-skills
```

**Or add as a marketplace first, then install:**

```bash
# In Claude Code interactive session:
/plugin marketplace add xmake-io/xmake-skills
/plugin install xmake-skills
```

### Manual installation

Clone this repository and point your agent at it directly. Refer to your agent platform's documentation for how to install and enable skills.

```bash
git clone https://github.com/xmake-io/xmake-skills.git
```

## Contributing

Contributions are very welcome. If you want to add a new skill or improve an existing one, please open an issue or pull request.

## Resources

- Xmake: https://github.com/xmake-io/xmake
- Documentation: https://xmake.io
- Community: https://discord.gg/xmake

## License

Licensed under the Apache License, Version 2.0. See [LICENSE.md](/LICENSE.md) for details.
