# DELLANNO ERP

Sistema ERP desenvolvido para gestão interna da Dell Anno, com foco em controle de usuários, cadastros, auditoria, segurança e acompanhamento operacional.

---

## Visão Geral

O DellAnno ERP foi desenvolvido para centralizar processos administrativos e operacionais em uma única plataforma web.

O sistema possui interface responsiva, autenticação segura, controle de permissões por perfil e registro completo das ações realizadas pelos usuários.

---

## Principais Funcionalidades

### Dashboard

* Indicadores operacionais
* Visão geral do sistema
* Acesso rápido aos módulos

### Controle de Usuários

* Cadastro de usuários
* Alteração de dados
* Troca de senha
* Controle de permissões
* Ativação e desativação de contas

### Perfis de Acesso

* Administrador
* Gerência
* Operacional
* Usuário

Permissões controladas por perfil.

### Cadastros

Gestão de:

* Arquitetos
* Clientes
* Colaboradores
* Convidados

### Sistema de Auditoria

Registro completo das operações realizadas:

* Inclusão
* Alteração
* Exclusão
* Login
* Logout

Informações registradas:

* Usuário
* Data e hora
* Módulo
* Operação executada

### Logs do Sistema

Monitoramento técnico contendo:

* Data/Hora
* Usuário
* Endereço IP
* Método HTTP
* Endpoint acessado
* Status da requisição

### Segurança

* Senhas criptografadas
* Controle de sessão
* Proteção de rotas
* Validação de permissões
* Tratamento de exceções

---

## Tecnologias Utilizadas

### Backend

* Python 3
* FastAPI
* Uvicorn

### Frontend

* HTML5
* CSS3
* Tailwind CSS
* JavaScript

### Templates

* Jinja2

### Banco de Dados

* SQL Relacional

### Hospedagem

* Render

### Controle de Versão

* Git
* GitHub

---

## Estrutura do Projeto

```text
DELLANNO/
│
├── api/
│   ├── controllers/
│   ├── services/
│   ├── database/
│   ├── security/
│   ├── models/
│   └── routes/
│
├── templates/
│
├── static/
│   ├── css/
│   ├── js/
│   ├── imagens/
│   └── icons/
│
├── uploads/
│
├── main.py
│
├── requirements.txt
│
└── README.md
```

---

## Fluxo de Desenvolvimento

### Ambiente Local

```bash
uvicorn main:app --reload
```

### Branches

```text
main
└── Produção

develop
└── Desenvolvimento/Testes
```

Fluxo recomendado:

1. Desenvolver na branch develop
2. Testar localmente
3. Realizar commit
4. Fazer merge para main
5. Publicar em produção

---

## Deploy

Hospedado na plataforma Render.

Fluxo:

```text
GitHub
    ↓
Render
    ↓
Deploy Automático
```

---

## Objetivos do Projeto

* Centralizar informações
* Melhorar rastreabilidade
* Aumentar segurança
* Reduzir processos manuais
* Facilitar auditorias
* Melhorar produtividade operacional

---

## Desenvolvido por

Guarametis Soluções e Serviços

Sistema desenvolvido utilizando tecnologias modernas para garantir segurança, desempenho e escalabilidade.

Todos os direitos reservados.
