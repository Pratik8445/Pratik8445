name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

permissions:
  contents: write

jobs:
  build:
    runs-on: ubuntu-latest

## 💻 Terminal Profile

```javascript
const pratik = {
  terminal: "active 💻",

  identity: {
    name: "Pratik Raj",
    role: "Software Engineer 👨‍💻"
  },

  boot_sequence: [
    "Loading problem solving modules... 🧠",
    "Initializing system design thinking... ⚙️",
    "Applying clean code principles... ✨",
    "System ready 🚀"
  ],

  tech_stack: {
    languages: ["Java", "JavaScript", "SQL"],
    frontend: ["HTML", "CSS", "React"],
    backend: ["Node.js", "Express"],
    database: ["SQLite", "MongoDB"]
  },

  current_focus: [
    "Data Structures & Algorithms 🚀",
    "Backend Engineering 🔧",
    "Scalable Architecture 📈"
  ],

  system_values: "Simplicity • Performance • Scalability",

  easter_egg: () => "Debugging powered by coffee ☕"
};
```
<p align="center">
  <img src="https://raw.githubusercontent.com/Pratik8445/Pratik8445/output/github-contribution-grid-snake.svg" />
</p>

    steps:
      - name: Generate snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: Pratik8445
          outputs: dist/github-contribution-grid-snake.svg

      - name: Push snake to branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
