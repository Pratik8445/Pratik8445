## 👋 About Me

<table>
<tr>
<td width="55%">

```yaml id="w0h5dp"
Name       : Pratik Raj
Role       : Full Stack Web Developer

Focus      : Backend Development • Problem Solving • System Design

Tech Stack :
  - Java • JavaScript • SQL
  - React • Node.js • Express
  - MongoDB • SQLite

Learning   : Deepening backend development with a focus on scalable systems
             while integrating GenAI into real-world applications.

```

</td>

<td width="45%" align="center">

<img src="https://cdn-icons-png.flaticon.com/512/1055/1055687.png" width="220"/>

</td>
</tr>
</table>


<p align="center">
 <img src="https://raw.githubusercontent.com/Pratik8445/Pratik8445/output/github-contribution-grid-snake.svg" />
</p>

    steps:
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

    steps:
      - name: Generate snake
        uses: Platane/snk@v3
        with:
          github_user_name: Pratik8445
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push snake
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
