Hello Github visitor! 😃 Welcome to my Profile! 👋

![Isaac's github stats](https://github-readme-stats.vercel.app/api?username=Istott)

<img src="https://github-readme-stats.vercel.app/api/top-langs?username=istott&show_icons=true&locale=en&layout=compact&theme=chartreuse-dark" alt="ovi" />

I'm rarely on here anymore. I mainly use this account to test new technologies, play around learning something new or teaching/mentoring others.

My current favorite stack that I code in everyday at work is:
- TypeScript
- React
- Redux ToolKit / Saga
- MUI

Feel free to contact me at:
isaac.cloyd@gmail.com  📧


<!--
**Istott/Istott** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

name: Contribution snake

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update snake grid
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: madushadhanushka
          svg_out_path: dist/github-contribution-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
