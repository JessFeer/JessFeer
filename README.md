### Olá, Eu sou a Jessica 👋

- 👩🏻‍🎓 Estudante do Curso de Análise e Desenvolvimento de Sistemas na Fatec Ipiranga - SP.
- 🌱 Atualmente, estou estudando Java e Phyton.
- 😄 Pronomes: Ela/Dela.





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
          github_user_name: JessFeer
          svg_out_path: dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
