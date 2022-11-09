### Olá, bem vindos. Eu sou o Ricardo Ferndandes 👋


**ricardoegea/ricardoegea** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=anuraghazra&show_icons=true&theme=radical)

name: Generate Datas
on:
schedule: # execute every 12 hours
- cron: "* */12 * * *"
workflow_dispatch:
jobs:
build:
name: Jobs to update datas
runs-on: ubuntu-latest
steps:
# Summary Cards
- uses: actions/checkout@v2
- uses: vn7n24fzkq/github-profile-summary-cards@release
env:
GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
with:
USERNAME: ${{ github.repository_owner }}

      # Snake Animation
       - uses: Platane/snk@master
    id: snake-gif
    with:
      github_user_name: camilamaraschin
      svg_out_path: dist/github-contribution-grid-snake.svg
  - uses: crazy-max/ghaction-github-pages@v2.1.3
    with:
      target_branch: output
      build_dir: dist
    env:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
