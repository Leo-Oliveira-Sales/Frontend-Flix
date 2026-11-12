## Front end Desenvolvido com Google IA Studio para o Projeto API-Django-Rest-Biblioteca-de-Filmes


---

## Todo o FrontEnd também pode ser feito com a ferramenta de **google stitch**, após criar todo o design de interfaces (UI/UX) leve o codigo para o Gemini e faça as adaptações para o BackEnd Django Templates, fornecendo os models.py, views.py, forms.py

---

## Para que serve o Stitch?

Google Stitch = Design de UI/UX e Front-end (visual, layouts, telas, fluxos e protótipos).
Ele gera a interface completa (telas, componentes, fluxos visuais) e o código front-end (HTML, CSS e estruturas de componentes). Ele é focado na experiência visual e no design (vibe design).

Google Stitch (Visual e Estética): Você monta a "casca" das suas telas, testa cores, ajusta tipografia, espaçamentos e efeitos visuais até ficar com cara de produto profissional. Depois, exporta o código HTML/Tailwind/JS limpo.

---

## Para que serve o Gemini?

Gemini (Engenharia e Integração): Você cola o HTML que saiu do Stitch junto com os arquivos do seu back-end (models.py, views.py, forms.py) e pede para eu fazer a "ponte" — substituindo os dados estáticos pelas variáveis e tags de template do Django ({% for %}, {{ campo }}, {% csrf_token %}).

---

# O fluxo operacional perfeito!

1. BackEnd Django

2. Design: Você usa o Stitch para gerar o visual e o código HTML/Tailwind limpo.

3. Gemini (Engenharia e Integração): Você cola o HTML que saiu do Stitch junto com os arquivos do seu back-end (models.py, views.py, forms.py) e pede para eu fazer a "ponte" — substituindo os dados estáticos pelas variáveis e tags de template do Django ({% for %}, {{ campo }}, {% csrf_token %}).

4. **Deploy**
VS Code / Django (Estrutura e Deploy): Você cria as pastas (templates/ e static/), cola os arquivos já mastigados, testa com python manage.py runserver e sobe tudo em um único deploy unificado.

Configure o Tailwind via CDN: Isso garante que qualquer código gerado pelo Stitch funcione imediatamente no seu navegador.

        └── templates/
                └── core/
                    └── base.html # Layout

      <!DOCTYPE html>
      <html lang="pt-br">
      <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>{% block title %}Meu Sistema{% endblock %}</title>
          <script src="https://cdn.tailwindcss.com"></script>
      </head>
      <body class="bg-gray-50 text-gray-900">
          {% block content %}{% endblock %}
      </body>
      </html>
   

---

## Run Local

**Prerequisitos:**  Node.js

Ative o ambiente virtual (venv):

Windows (PowerShell ou CMD):

Bash
venv\Scripts\activate


Aplique as migrações do banco de dados (caso seja a primeira vez ou tenha alterado o models.py):

Bash
python manage.py migrate

Inicie o servidor local:

Bash
python manage.py runserver

Acesse no navegador:

Abra o endereço [http://127.0.0.1:8000/](http://127.0.0.1:8000/) 
(ou segure Ctrl e clique no link que aparece no terminal).
