# 🔐 Autenticação com OAuth 2.0 no Django

<p align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3064/3064197.png" width="120"/>
</p>

### 📘 Sobre o projeto
Este projeto foi desenvolvido como parte do curso da **[Alura](https://www.alura.com.br/)**, com o objetivo de **implementar autenticação de usuários via OAuth 2.0** utilizando o framework **Django**.  
O foco é demonstrar como integrar **provedores externos (como Google, GitHub, etc.)** ao sistema de login da aplicação.

> 💡 Projeto desenvolvido por **João Victor Rocha Cândido**, durante as atividades práticas de autenticação com OAuth2.0 da Alura.

---

### ⚙️ Tecnologias utilizadas
- **Python 3**
- **Django**
- **Django OAuth Toolkit**
- **SQLite3**
- **HTML / CSS**
- **Bootstrap**
- **OAuth 2.0**

---

### 🗂️ Estrutura do projeto
```
Django_autenticacao_com_OAuth2.0-ALURA/
│
├── manage.py                # Script principal do Django
├── requirements.txt         # Dependências do projeto
├── .gitignore
│
├── setup/                   # Configurações globais do projeto
│   ├── settings.py          # Configurações de apps, middleware, autenticação, etc.
│   ├── urls.py              # Rotas principais
│   ├── asgi.py / wsgi.py    # Configurações de servidor
│
├── tech/                    # Aplicação principal (módulo de autenticação)
│   ├── models.py            # Modelos de usuário e perfis
│   ├── views.py             # Views responsáveis pelas páginas e autenticação
│   ├── urls.py              # Rotas específicas do app
│   ├── admin.py             # Registro no painel administrativo
│
└── templates/               # Páginas HTML e arquivos estáticos
    ├── index.html           # Página inicial
    ├── members.html         # Página de membros autenticados
    └── static/
        ├── index.css        # Estilo da página inicial
        ├── members.css      # Estilo da página de membros
        └── assets/          # Logos e imagens
```

---

### 🚀 Como executar o projeto

#### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/JvrCandido/Django_autenticacao_com_OAuth2.0-ALURA.git
cd Django_autenticacao_com_OAuth2.0-ALURA
```

#### 2️⃣ Criar e ativar um ambiente virtual
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

#### 3️⃣ Instalar as dependências
```bash
pip install -r requirements.txt
```

#### 4️⃣ Executar as migrações
```bash
python manage.py migrate
```

#### 5️⃣ Iniciar o servidor de desenvolvimento
```bash
python manage.py runserver
```

Acesse no navegador:  
👉 **http://127.0.0.1:8000/**

---

### 🔐 Funcionalidades principais

| Recurso | Descrição |
|----------|------------|
| **Login OAuth 2.0** | Autenticação usando provedores externos (ex: Google, GitHub). |
| **Sistema de Usuários** | Cadastro e gerenciamento de perfis autenticados. |
| **Controle de Sessão** | Acesso restrito a páginas como `members.html`. |
| **Integração Frontend/Backend** | Uso de templates Django e estilos customizados em CSS. |

---

### 🧠 Explicação do código

- **`setup/settings.py`** → Configurações do projeto Django (apps, banco, OAuth, templates, etc).  
- **`tech/views.py`** → Define as views para login, logout e exibição de usuários autenticados.  
- **`tech/urls.py`** → Define rotas específicas da aplicação.  
- **`templates/`** → Contém as páginas HTML que exibem o conteúdo e o estado de autenticação.  
- **`requirements.txt`** → Lista todas as bibliotecas necessárias para rodar o projeto.

---

### 🧩 Exemplo de fluxo de autenticação

1. O usuário acessa a página inicial `index.html`.  
2. Clica em **"Login com Google"** (ou outro provedor OAuth).  
3. Após autenticação, é redirecionado para `members.html`.  
4. A sessão é armazenada localmente e pode ser encerrada via logout.

---

### 🧑‍💻 Créditos
Projeto desenvolvido por **João Victor Rocha Cândido**,  
como parte do módulo de autenticação OAuth2.0 da **Alura**.  
💻 *“Aprendendo segurança e autenticação na prática com Django.”*
