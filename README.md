# 🎓 Portal Acadêmico - Módulo de Notas e Faltas

## 1. Visão Geral e Objetivos do Projeto
O Portal Acadêmico é uma solução de software desenvolvida para centralizar, simplificar e tornar intuitiva a jornada do estudante. O objetivo principal do sistema é permitir que o aluno gerencie o seu desempenho (notas), acompanhe as suas frequências em tempo real e verifique se corre riscos de retenção de forma rápida e prática.

## 2. Tipos de Usuários e Permissões
* **Aluno (Usuário Comum):** Permissão apenas de leitura (`Read`). Visualiza as suas próprias notas, médias, histórico de faltas e disciplinas matriculadas.
* **Professor / Secretaria (Admin):** Permissão de escrita e modificação (`CRUD`). Responsável por lançar/atualizar as notas e computar as faltas no diário de classe.

## 3. Fluxo de Utilização e Telas
1. **Tela de Login:** Autenticação segura com Matrícula e Senha.
2. **Dashboard:** Tela inicial com avisos da coordenação e atalhos rápidos.
3. **Página de Notas e Faltas:** Painel em formato de tabela onde o aluno consulta o progresso das suas avaliações ($AV1, AV2, Final$) e o acumulado de faltas com alertas visuais.

## 4. Planejamento de Expansão (Funcionalidades Futuras)
* **Simulador de Médias:** Ferramenta interativa para simular notas futuras e prever a pontuação necessária para aprovação.
* **Notificações via WebSockets:** Alertas *Push* em tempo real no momento exato em que o professor lançar uma nova nota.

## 5. Arquitetura de Dados e Backend (Proposta)
O sistema foi concebido utilizando uma API RESTful conectada a um banco de dados relacional SQL.

### Rotas de API (Endpoints):
* `POST /api/auth/login` -> Valida o utilizador e inicia a sessão.
* `GET /api/academic/boletim` -> Procura e renderiza o boletim do aluno logado.
* `POST /api/admin/notas/lancar` -> Permite ao professor registar notas no banco de dados.
