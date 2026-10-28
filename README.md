# ERP Guarametis

Sistema ERP desenvolvido para centralizar e organizar os processos administrativos e operacionais da Guarametis Soluções e Serviços, reunindo módulos de gestão, cadastros, controle de acesso, auditoria e acompanhamento das operações.

## Módulos do Sistema

### ERP Guara-Agenda

Sistema de gestão de agendas e agendamentos, com recursos para consulta, acompanhamento de atendimentos, controle de presença e acesso por aplicativo móvel.

### ERP Guara-Copa

Sistema de gestão de copa, com cadastro de itens e kits, envio de pedidos pelo aplicativo móvel e acompanhamento do preparo e da entrega.

### ERP Guara-Estoque

Sistema de gestão de estoques e insumos, com cadastro de itens, controle de saldos, movimentações, transferências e centros de custo.

---

## Visão Geral

O ERP Guarametis foi desenvolvido para centralizar processos administrativos e operacionais em uma única plataforma web.

O sistema possui interface responsiva, autenticação, controle de permissões por perfil e mecanismos de registro e monitoramento das operações realizadas pelos usuários.

## Principais Funcionalidades

### 1. Painel

- Indicadores operacionais.
- Visão geral do sistema.
- Acesso rápido aos módulos disponíveis.

### 2. GuaraHub

- Centralização dos aplicativos do sistema.
- Acesso aos módulos conforme as permissões do usuário.

### 3. Agenda

- Consulta de agendamentos por data, loja e sala.
- Visualização em agenda diária e lista de agendamentos.
- Registro de presença de clientes, colaboradores e arquitetos.
- Aplicativo móvel PWA para acesso à agenda.

### 4. Copa

- Cadastro e manutenção de copas, itens e kits.
- Envio de pedidos pelo aplicativo móvel.
- Acompanhamento dos pedidos nos estados: aguardando, em preparo, pronto e entregue.
- Prévia do consumo previsto dos kits por dia.

### 5. Estoque

- Cadastro de locais de estoque e itens.
- Definição de unidades de medida e limites mínimos e máximos.
- Controle de custo médio dos itens.
- Registro de movimentações de entrada, saída, ajuste e transferência.
- Controle dos estados das movimentações: rascunho, confirmado e cancelado.
- Cadastro e consulta de centros de custo.

### 6. Projetos, Lojas e Salas

- Cadastro e manutenção de projetos e tipos de projeto.
- Associação de projetos a clientes.
- Cadastro de lojas e salas vinculadas.
- Definição da capacidade das salas.
- Cadastro e manutenção de status no módulo Farol.

### 7. Controle de Usuários

- Cadastro e alteração de usuários.
- Atualização de dados cadastrais.
- Troca de senha.
- Controle de permissões.
- Ativação e desativação de contas.

### 8. Perfis de Acesso

Perfis previstos no sistema:

- Administrador.
- Gerência Operacional.
- Usuário.

As permissões de acesso são controladas conforme o perfil atribuído ao usuário.

### 9. Cadastros

Gestão dos seguintes cadastros:

- Arquitetos.
- Clientes.
- Colaboradores.
- Convidados.

### 10. Auditoria do Sistema

Registro das operações realizadas pelos usuários, incluindo:

- Inclusões.
- Alterações.
- Exclusões.
- Login.
- Encerramento de sessão.

As informações registradas permitem rastrear as operações realizadas no sistema.

### 11. Registros Técnicos

Monitoramento técnico das requisições, com informações como:

- Data e hora.
- Usuário.
- Endereço IP.
- Método HTTP.
- Endpoint acessado.
- Status da requisição.

## Segurança

O sistema utiliza mecanismos de segurança, incluindo:

- Armazenamento de senhas por meio de hash criptográfico.
- Controle de sessão.
- Proteção de rotas.
- Controle de permissões de acesso.
- Validação de dados de entrada.
- Registro de operações para fins de auditoria.

## Tecnologias Utilizadas

### Backend

- Python 3.
- FastAPI.
- Uvicorn.

### Front-end

- HTML5.
- Jinja2.
- CSS3.
- Tailwind CSS.
- JavaScript.

### Templates

- Jinja2 para renderização das páginas HTML.

### Banco de Dados

- Banco de dados relacional SQL.

### Hospedagem e Implantação

- Render.

### Controle de Versão

- Git.
- GitHub.

## Estrutura do Projeto

A aplicação está organizada em módulos, com separação entre rotas, serviços, segurança, acesso ao banco de dados, arquivos estáticos e templates.

```text
DellAnno/
├── api/
│   ├── core/
│   │   ├── __init__.py
│   │   ├── api_client.py
│   │   ├── atalhos_globais.py
│   │   ├── http_client.py
│   │   ├── logs.py
│   │   ├── relatorio_agenda.py
│   │   ├── sessao.py
│   │   ├── thread_worker.py
│   │   └── toast.py
│   ├── database/
│   │   ├── __init__.py
│   │   └── connection.py
│   ├── routers/
│   │   ├── __init__.py
│   │   ├── agenda_app_router.py
│   │   ├── agenda_conflicts_routers.py
│   │   ├── agenda_router.py
│   │   ├── arquiteto_router.py
│   │   ├── auditoria_router.py
│   │   ├── auth_router.py
│   │   ├── centro_custo_router.py
│   │   ├── cliente_app_router.py
│   │   ├── cliente_projeto_router.py
│   │   ├── cliente_router.py
│   │   ├── colaborador_router.py
│   │   ├── contato_router.py
│   │   ├── convidado_router.py
│   │   ├── copa_app_router.py
│   │   ├── copa_dashboard_router.py
│   │   ├── copa_item_router.py
│   │   ├── copa_kit_router.py
│   │   ├── copa_pedido_router.py
│   │   ├── copa_previa_page_router.py
│   │   ├── copa_previa_router.py
│   │   ├── copa_router.py
│   │   ├── dashboard_router.py
│   │   ├── estoque_item_router.py
│   │   ├── estoque_local_router.py
│   │   ├── estoque_movimento_router.py
│   │   ├── farol_router.py
│   │   ├── guarahub_router.py
│   │   ├── index_router.py
│   │   ├── logs_router.py
│   │   ├── loja_router.py
│   │   ├── perfil_acesso_router.py
│   │   ├── perfil_router.py
│   │   ├── permissao_router.py
│   │   ├── projeto_router.py
│   │   ├── sala_router.py
│   │   ├── unidade_medida_router.py
│   │   └── usuario_router.py
│   ├── schemas/
│   │   ├── __init__.py
│   │   ├── agenda_app_schema.py
│   │   ├── agenda_conflict_schema.py
│   │   ├── agenda_schema.py
│   │   ├── arquiteto_schema.py
│   │   ├── centro_custo_schema.py
│   │   ├── cliente_app_schema.py
│   │   ├── cliente_projeto_schema.py
│   │   ├── cliente_schema.py
│   │   ├── colaborador_schema.py
│   │   ├── convidado_schema.py
│   │   ├── copa_app_schema.py
│   │   ├── copa_dashboard_schema.py
│   │   ├── copa_item_schema.py
│   │   ├── copa_kit_schema.py
│   │   ├── copa_pedido_schema.py
│   │   ├── copa_previa_schema.py
│   │   ├── copa_schema.py
│   │   ├── dashboard_schema.py
│   │   ├── estoque_item_schema.py
│   │   ├── estoque_local_schema.py
│   │   ├── estoque_movimento_schema.py
│   │   ├── farol_schema.py
│   │   ├── logs_schema.py
│   │   ├── loja_schema.py
│   │   ├── perfil_acesso_schema.py
│   │   ├── perfil_schema.py
│   │   ├── permissao_schema.py
│   │   ├── projeto_schema.py
│   │   ├── sala_schema.py
│   │   ├── unidade_medida_schema.py
│   │   └── usuario_schema.py
│   ├── security/
│   │   ├── audit_middleware.py
│   │   ├── auth.py
│   │   ├── decorators.py
│   │   ├── permissions.py
│   │   └── session.py
│   ├── services/
│   │   ├── __init__.py
│   │   ├── agenda_app_service.py
│   │   ├── agenda_conflict_service.py
│   │   ├── agenda_service.py
│   │   ├── arquiteto_service.py
│   │   ├── audit_service.py
│   │   ├── centro_custo_service.py
│   │   ├── cliente_app_service.py
│   │   ├── cliente_projeto_service.py
│   │   ├── cliente_service.py
│   │   ├── colaborador_service.py
│   │   ├── convidado_service.py
│   │   ├── copa_app_service.py
│   │   ├── copa_dashboard_service.py
│   │   ├── copa_item_service.py
│   │   ├── copa_kit_service.py
│   │   ├── copa_pedido_service.py
│   │   ├── copa_previa_service.py
│   │   ├── copa_service.py
│   │   ├── dashboard_service.py
│   │   ├── email_service.py
│   │   ├── estoque_item_service.py
│   │   ├── estoque_local_service.py
│   │   ├── estoque_movimento_service.py
│   │   ├── farol_service.py
│   │   ├── logs_service.py
│   │   ├── loja_service.py
│   │   ├── perfil_acesso_service.py
│   │   ├── perfil_service.py
│   │   ├── permissao_service.py
│   │   ├── projeto_service.py
│   │   ├── sala_service.py
│   │   ├── unidade_medida_service.py
│   │   └── usuario_service.py
│   ├── static/
│   │   ├── css/
│   │   │   ├── components/
│   │   │   │   ├── buttons.css
│   │   │   │   ├── dropdown.css
│   │   │   │   ├── forms.css
│   │   │   │   ├── search.css
│   │   │   │   └── tables.css
│   │   │   ├── layout/
│   │   │   │   ├── base.css
│   │   │   │   ├── cards.css
│   │   │   │   ├── header.css
│   │   │   │   └── sidebar.css
│   │   │   ├── pages/
│   │   │   │   ├── estoque/
│   │   │   │   │   ├── centro_custo.css
│   │   │   │   │   ├── estoque_item.css
│   │   │   │   │   ├── estoque_local.css
│   │   │   │   │   └── estoque_movimento.css
│   │   │   │   ├── agenda.css
│   │   │   │   ├── agenda_app.css
│   │   │   │   ├── agenda_conflicts.css
│   │   │   │   ├── agenda_dia.css
│   │   │   │   ├── agenda_lista.css
│   │   │   │   ├── arquiteto.css
│   │   │   │   ├── cliente.css
│   │   │   │   ├── colaborador.css
│   │   │   │   ├── convidado.css
│   │   │   │   ├── copa.css
│   │   │   │   ├── copa_app.css
│   │   │   │   ├── copa_dashboard.css
│   │   │   │   ├── copa_item.css
│   │   │   │   ├── copa_kit.css
│   │   │   │   ├── copa_previa.css
│   │   │   │   ├── dashboard.css
│   │   │   │   ├── guarahub.css
│   │   │   │   └── usuario.css
│   │   │   └── style.css
│   │   ├── img/
│   │   │   ├── icon-192.png
│   │   │   ├── icon-512.png
│   │   │   ├── icon-agenda-192.png
│   │   │   ├── icon-agenda-512.png
│   │   │   ├── icon-copa-192.png
│   │   │   ├── icon-copa-512.png
│   │   │   ├── icon-maskable-512.png
│   │   │   ├── icon-maskable-512old (2).png
│   │   │   ├── icon-maskable-512old.png
│   │   │   ├── icon_maskable-513.png
│   │   │   ├── logodellanno.png
│   │   │   └── logoguarametis.png
│   │   ├── js/
│   │   │   ├── pages/
│   │   │   │   ├── estoque/
│   │   │   │   │   ├── centro_custo.js
│   │   │   │   │   ├── estoque_item.js
│   │   │   │   │   ├── estoque_local.js
│   │   │   │   │   └── estoque_movimento.js
│   │   │   │   ├── agenda_app.js
│   │   │   │   ├── agenda_conflicts.js
│   │   │   │   ├── agenda_dia.js
│   │   │   │   ├── agenda_lista.js
│   │   │   │   ├── copa.js
│   │   │   │   ├── copa_app.js
│   │   │   │   ├── copa_dashboard.js
│   │   │   │   ├── copa_item.js
│   │   │   │   ├── copa_kit.js
│   │   │   │   ├── copa_pedido.js
│   │   │   │   └── copa_previa.js
│   │   │   ├── base-crud.js
│   │   │   ├── dropdown.js
│   │   │   └── sidebar.js
│   │   ├── screenshots/
│   │   │   ├── copa_mobile.png
│   │   │   ├── desktop.png
│   │   │   └── mobile.png
│   │   ├── favicon.ico
│   │   ├── manifest_agenda.json
│   │   ├── manifest_copa.json
│   │   ├── manifest_guarahub.json
│   │   ├── sw-agenda.js
│   │   ├── sw-copa.js
│   │   ├── sw-guarahub.js
│   │   ├── sw-sistemas.js
│   │   └── sw.js
│   ├── templates/
│   │   ├── agenda/
│   │   │   ├── agenda.html
│   │   │   ├── agenda_app.html
│   │   │   ├── agenda_conflicts.html
│   │   │   ├── agenda_dia.html
│   │   │   └── lista.html
│   │   ├── copa/
│   │   │   ├── adm/
│   │   │   │   └── copa_previa.html
│   │   │   ├── atendimento/
│   │   │   │   └── copa_app.html
│   │   │   ├── cadastro/
│   │   │   │   ├── copa.html
│   │   │   │   ├── copa_item.html
│   │   │   │   └── copa_kit.html
│   │   │   └── operacao/
│   │   │       └── copa_dashboard.html
│   │   ├── estoque/
│   │   │   ├── centro_custo.html
│   │   │   ├── estoque_item.html
│   │   │   ├── estoque_local.html
│   │   │   └── estoque_movimento.html
│   │   ├── arquiteto.html
│   │   ├── base.html
│   │   ├── cliente.html
│   │   ├── cliente_app.html
│   │   ├── cliente_projeto.html
│   │   ├── colaborador.html
│   │   ├── convidado.html
│   │   ├── dashboard.html
│   │   ├── farol.html
│   │   ├── guarahub.html
│   │   ├── index.html
│   │   ├── login.html
│   │   ├── logs.html
│   │   ├── loja.html
│   │   ├── perfil.html
│   │   ├── perfil_acesso.html
│   │   ├── permissao.html
│   │   ├── projeto.html
│   │   ├── sem_permissao.html
│   │   └── usuario.html
│   ├── __init__.py
│   ├── main.py
│   ├── main_agenda.py
│   └── main_copa.py
├── .gitignore
├── Agendamento regras.txt
├── api.txt
├── Clientes - Regras.txt
├── converte_ui.bat
├── criar_admin.py
├── estruturadellanno.md
├── estruturadellanno.txt
├── GITHUB.txt
├── guaraagenda manual.docx
├── localdellanno
├── main.py
├── readme.md
├── Regra Lojas.txt
├── regra Projeto.txt
├── requirements.txt
├── SISTEMA DELL ANNO - Funcionamento.docx
├── sql dellanno.txt
├── SQL-Seguranca.zip
├── stylesold.qss
├── teste.py
├── teste_hash.py
└── 🔥 MAPEAMENTO (MODEL → API).txt
```

**Observação:** a árvore acima é ilustrativa e organizada por módulos. Confirme os caminhos e nomes dos arquivos existentes no repositório antes de utilizá-la como inventário completo.

## Fluxo de Desenvolvimento

### Ambiente Local

Para iniciar a aplicação com Uvicorn, utilize o comando correspondente ao ponto de entrada configurado no projeto:

```bash
uvicorn main:app --reload
```

O comando pressupõe que `main.py` esteja no diretório atual e exponha uma aplicação ASGI chamada `app`.

### Branches

- `main`: branch principal destinada à produção.
- `develop`: branch destinada ao desenvolvimento e aos testes.

### Fluxo Recomendado

1. Desenvolver as funcionalidades na branch `develop`.
2. Executar os testes no ambiente local.
3. Realizar o commit das alterações.
4. Validar as modificações.
5. Integrar as alterações à branch `main`.
6. Publicar a versão de produção.

## Implantação

A aplicação está hospedada na plataforma Render, com implantação integrada ao repositório GitHub.

Fluxo de implantação:

```text
Desenvolvimento
      ↓
     Git
      ↓
    GitHub
      ↓
     Render
      ↓
Implantação em produção
```

A implantação automática depende das configurações do serviço e da branch vinculada no Render.

## Objetivos do Projeto

- Centralizar informações administrativas e operacionais.
- Melhorar a rastreabilidade das operações.
- Reforçar a segurança e o controle de acesso.
- Reduzir processos manuais.
- Facilitar auditorias.
- Melhorar a produtividade operacional.
- Organizar os processos internos em uma plataforma integrada.

## Desenvolvido por

**Guarametis Soluções e Serviços**

Sistema desenvolvido com tecnologias web para apoiar a gestão interna, a segurança da informação e a organização dos processos operacionais.

Todos os direitos reservados.
