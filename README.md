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
## 🛠️ Tech Stack

### 🧠 Languages
<p>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white"/>
</p>

---

### 💻 Frontend
<p>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black"/>
</p>

---

### ⚙️ Backend
<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white"/>
</p>

---

### 🗄️ Database
<p>
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white"/>
</p>

---

### 🛠️ Tools
<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</p>


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
