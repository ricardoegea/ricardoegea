### Olรก, bem vindos. Eu sou o Ricardo Ferndandes ๐


**ricardoegea/ricardoegea** is a โจ _special_ โจ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- ๐ญ Iโm currently working on ...
- ๐ฑ Iโm currently learning ...
- ๐ฏ Iโm looking to collaborate on ...
- ๐ค Iโm looking for help with ...
- ๐ฌ Ask me about ...
- ๐ซ How to reach me: ...
- ๐ Pronouns: ...
- โก Fun fact: ...

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=anuraghazra&show_icons=true&theme=radical)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=anuraghazra&layout=compact)](https://github.com/anuraghazra/github-readme-stats)


.github/workflows/cobrinha.yml
@@ -1,23 +1,15 @@
ame: Generate Datas
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
      github_user_name: ricardoegea
      svg_out_path: dist/github-contribution-grid-snake.svg
  - uses: crazy-max/ghaction-github-pages@v2.1.3
    with:
      target_branch: output
      build_dir: dist
    env:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
