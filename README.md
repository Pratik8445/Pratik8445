
const pratik = {
  Hi I'm Pratik

  identity: {
    name: "Pratik Raj",
    role: "Full Stack Web Developer"
  },

  boot_sequence: [
    " Loading problem solving modules...",
    " Initializing system design...",
    " Applying clean code principles...",
    " System ready"
  ],

  tech_stack: {
    languages: ["Java", "JavaScript", "SQL"],
    frontend: ["HTML", "CSS", "React"],
    backend: ["Node.js", "Express"],
    database: ["SQLite", "MongoDB"]
  },

  current_focus: [
    "Data Structures & Algorithms",
    " Backend Engineering",
    " Scalable Architecture"
  ],

  system_values: ["Simplicity", "Performance", "Scalability"],

  status: "Building. Learning. Improving ",

  easter_egg: () => "☕ Coffee → Code → Repeat"
};

─────────────────────────────────────────────
                WELCOME
─────────────────────────────────────────────
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
