# 💡 Oi !! Eu sou o Maicon Bastos👋👋 :
Engenheiro de Biossistemas - USP<br>Ciências de Dados - UNIVESP


## 🌐 Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/https://www.linkedin.com/in/maiconbastos/) 

# 💻 Tech Stack:
![Python](https://img.shields.io/badge/python-3670A0?style=plastic&logo=python&logoColor=ffdd54) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=plastic&logo=google-cloud&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=plastic&logo=Keras&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=plastic&logo=Matplotlib&logoColor=black) ![mlflow](https://img.shields.io/badge/mlflow-%23d9ead3.svg?style=plastic&logo=numpy&logoColor=blue) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=plastic&logo=scikit-learn&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=plastic&logo=numpy&logoColor=white) ![Scipy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=plastic&logo=scipy&logoColor=%white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=plastic&logo=TensorFlow&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=plastic&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=plastic&logo=plotly&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=plastic&logo=PyTorch&logoColor=white)
# 📊 GitHub Stats:
</div>
<a href="https://github.com/MaiconBastos">
<img heigth="180cm" align="center" src="https://github-readme-stats.vercel.app/api?username=MaiconBastos&show_icons=true&theme=react&include_all_commits=true&count_private=true"/>
<img heigth="180cm" align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MaiconBastos&layout=compact&langs_count=7&theme=react"/>

# Nome da Actions:  
name: Snake Game

# Controlador do tempo que sera feito a atualização dos arquivos.
on:
  schedule:
      # Será atualizado a cada 5 horas.
    - cron: "0 */5 * * *"

# Permite executar na na lista de Actions (utilizado para testes de build).
  workflow_dispatch:

# Regras
jobs:
  build:
    runs-on: ubuntu-latest
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Repositorio que será utilizado para gerar os arquivos.
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: artur-debv
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - run: git status

      # Para as atualizações.
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


---
[![](https://visitcount.itsvg.in/api?id=MaiconBastos&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
