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
  <img src="https://raw.githubusercontent.com/Pratik8445/Pratik8445/output/github-contribution-grid-snake-dark.svg" />
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
