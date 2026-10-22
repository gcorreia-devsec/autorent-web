# AutoRent - Sistema de Gestão de Frota e Locação de Veículos

**Disciplina:** Desenvolvimento Web  
**Professor:** Esp. Welliton Cunha  
**Desenvolvedor:** Guilherme Correia  
**Turma:** Sistemas de Informação (2026.2)

---

## 1. Problemática e Contexto Atual
O projeto AutoRent surgiu a partir de uma dificuldade comum em locadoras de pequeno e médio porte: a falta de um controlo centralizado sobre a situação da frota e os prazos de locação. 

Atualmente, o controlo é feito de forma manual (planilhas de Excel ou papel). Isso gera lentidão no balcão, risco de alugar um carro que precisa de manutenção e falta de um histórico confiável de devoluções.

## 2. Público-Alvo e Principais Usuários
- **Atendentes de balcão:** Registarão as saídas e devoluções dos carros no dia a dia.
- **Gerentes/Proprietários:** Acompanharão a taxa de ocupação da frota e o histórico de contratos.
- **Equipa de manutenção:** Consultarão quais veículos estão com status inativo para revisão.

## 3. Objetivo da Solução e Escopo Inicial
O objetivo é desenvolver uma aplicação web simples e direta que centralize o registo da frota, dos clientes e das locações, evitando reservas duplicadas e mantendo o status dos carros atualizado em tempo real.

**O que fará parte do projeto (Dentro do Escopo):**
- CRUD de veículos (modelo, placa, categoria, valor, status).
- CRUD de clientes (nome, CPF, CNH).
- Registo de locação vinculando cliente, veículo, data de saída e devolução.
- Alteração automática de status do carro (Disponível, Alugado, Manutenção).

**O que NÃO fará parte do projeto (Fora do Escopo):**
- Integração com pagamentos online (PIX/Cartão).
- Emissão de fatura/nota fiscal.
- Rastreamento por GPS.

## 4. Requisitos Iniciais

### Requisitos Funcionais (RF)
- **RF01:** Permitir gerenciar (cadastrar, listar, editar, excluir) os veículos da frota.
- **RF02:** Permitir gerenciar os clientes da locadora.
- **RF03:** Registar uma nova locação vinculando cliente e carro disponível.
- **RF04:** Alterar automaticamente o status do veículo para "Alugado" na retirada.
- **RF05:** Registar a devolução e voltar o status do carro para "Disponível".
- **RF06:** Filtrar frota por status (Disponíveis, Alugados, Manutenção).

### Requisitos Não Funcionais (RNF)
- **RNF01:** O backend deve ser uma API REST (JSON) dividida em Routes, Controllers e Models.
- **RNF02:** Persistência de dados em banco relacional PostgreSQL.
- **RNF03:** Credenciais do banco salvas de forma segura em arquivo `.env`.

## 5. Tecnologias Escolhidas e Justificativa
- **Frontend (HTML/CSS/JS):** Para construir uma interface rápida e limpa para o balcão.
- **Backend (Node.js com Express.js):** Facilita a criação das rotas HTTP (GET, POST, PUT, DELETE) e a comunicação assíncrona, ideal para o desenvolvimento full-stack individual.
- **Banco de Dados (PostgreSQL + biblioteca 'pg'):** Garante a integridade relacional entre clientes, carros e contratos.
- **Controlo de Versão (Git e GitHub):** Para manter o histórico do código seguro e versionado.

## 6. Riscos, Dúvidas e Premissas
- **Riscos:** Atraso na integração final entre o frontend e a API devido ao volume de trabalho ser concentrado num único programador.
- **Dúvidas:** O sistema final precisará de alojamento em cloud (deploy) ou poderá ser demonstrado localmente (localhost)?
- **Premissas:** O ambiente de desenvolvimento (Node.js, VS Code e pgAdmin) já se encontra configurado no computador principal.
