# Calculadora Web (Python Flask HTML e JavaScript)

**Autor: Yan Barros Pereira**

Adaptado do projeto original de [VictorThomaz](https://github.com/VictorThomaz/projeto_calculadora_js_nav).

Este projeto é um exemplo didático de como usar **Python + Flask + HTML + JavaScript** para criar uma calculadora simples com páginas de **Soma**, **Subtração**, **Multiplicação** e **Divisão**.

---

## Requisitos

- Python 3 instalado
- VS Code (com extensão de Python)
- Ambiente virtual (venv)
- Flask instalado

---

## Estrutura do Projeto

```
projeto_calculadora_web/
│
├── app.py              # Rotas Flask
├── operacoes.py        # Funções matemáticas
├── requirements.txt    # Dependências
├── templates/          # Páginas HTML
│   ├── index.html
│   ├── soma.html
│   ├── subtracao.html
│   ├── multiplicacao.html
│   └── divisao.html
└── static/             # Arquivos estáticos
└── script.js
```

---

## Clonando o projeto para o computador local

Instale o Git, abra um terminal na pasta onde deseja salvar o projeto e clone o repositório:

```powershell
git clone https://github.com/usuario/nome-do-repositorio.git
```

Substitua o endereço de exemplo pela URL do repositório deste projeto. Em seguida, acesse a pasta criada pelo Git:

```powershell
cd nome-do-repositorio
```

## Criando e ativando o ambiente virtual no Windows

Abra o terminal na pasta do projeto e crie o ambiente virtual:

```powershell
py -m venv .venv
```

Para ativá-lo no PowerShell, execute:

```powershell
.\.venv\Scripts\Activate.ps1
```

Se estiver usando o Prompt de Comando (cmd), execute:

```cmd
.venv\Scripts\activate.bat
```

Com o ambiente ativado, o nome `.venv` aparecerá no início da linha do terminal.

## Instalando o Flask

Com o terminal ainda na pasta do projeto e o ambiente virtual ativado, instale as dependências listadas em `requirements.txt`:

```powershell
python -m pip install -r requirements.txt
```

## Executando a aplicação

Na pasta do projeto, com o ambiente virtual ativado, execute:

```powershell
python app.py
```

Quando o servidor iniciar, abra o navegador e acesse:

```text
http://127.0.0.1:5000
```

Para encerrar a aplicação, volte ao terminal e pressione `Ctrl+C`.

## Funcionalidades

- Navegação: Início, Soma, Subtração, Multiplicação e Divisão.
- Operações implementadas no arquivo `operacoes.py` (Python).
- Comunicação entre JavaScript e Flask via `fetch()` e endpoints JSON.
- Divisão por zero tratada com mensagem amigável, sem interromper a aplicação.

## Exemplos de API

`POST /api/multiplicacao` com JSON `{"valor1": 6, "valor2": 7}` retorna `{"resultado": 42.0}`.

`POST /api/divisao` com JSON `{"valor1": 10, "valor2": 2}` retorna `{"resultado": 5.0}`.

Para divisão por zero, a API responde HTTP 400 e a mensagem `Não é possível dividir por zero.`

## Versionamento e publicação

Esta cópia contém histórico Git local com commits separados para a base, multiplicação, divisão e documentação. O autor é **Yan Barros Pereira**, e a branch de desenvolvimento é `yan_barros_pereira`. Configure seu e-mail real do GitHub antes de novos commits ou da publicação.

No GitHub, crie um repositório **público vazio** (sem inicializar README) e execute na pasta do projeto:

```bash
git config user.name "Yan Barros Pereira"
git config user.email "SEU_EMAIL_DO_GITHUB"
git remote add origin https://github.com/SEU_USUARIO/calculadora-flask.git
git push -u origin main
git push -u origin yan_barros_pereira
```

**Importante:** a branch `main` representa a versão original; a branch com seu nome contém todas as melhorias e deve ser selecionada como padrão no GitHub (Settings → Default branch), ou incorporada à `main` por merge.

Fontes para estudo: [Documentação Flask](https://flask.palletsprojects.com/en/stable/quickstart/), [Flask e JavaScript](https://flask.palletsprojects.com/en/stable/patterns/javascript/) e [Documentação GitHub](https://docs.github.com/en/get-started/using-git/about-git).
