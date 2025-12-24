# TravelPlan Project 🌍✈️

Bem-vindo à organização oficial do **TravelPlan**, um ecossistema multiplataforma projetado para simplificar a gestão de veículos, custos e roteiros de viagem. Este projeto nasceu da necessidade de centralizar dados de viagens que antes ficavam isolados em aplicativos móveis.

## 🏛️ Visão da Arquitetura

O TravelPlan utiliza uma arquitetura baseada em micro-serviços e clientes independentes, garantindo que o usuário tenha a mesma experiência seja no computador ou no celular.

### Fluxo de Dados:
1.  **Backend (API Central):** O "cérebro" do sistema, desenvolvido em **Java + Spring Boot**, que gerencia as regras de negócio e a persistência no banco de dados.
2.  **Frontend Web (React):** Interface administrativa e de consulta rápida para desktop.
3.  **Mobile (Android):** (Em migração) Aplicativo nativo para uso durante o percurso da viagem.


---

## 📂 Repositórios da Organização

Atualmente, o ecossistema é composto por:

### 1. [travelplan-web](https://github.com/travelplan-project/travelplan-web)
* **Papel:** Cliente Web Principal.
* **Tech Stack:** React 18, Vite, Tailwind CSS v4, Axios.
* **Status:** ✅ Funcional (Listagem de Veículos e Integração com API).

### 2. [travelplan-api](https://github.com/travelplan-project/travelplan-api)
* **Papel:** Servidor de API REST.
* **Tech Stack:** Java, Spring Boot, Spring Data JPA, MySQL/H2.
* **Status:** ✅ Online (Endpoints de Veículos e Viagens).

---

## 🔄 Protocolo de Integração

A integração entre os projetos é estritamente via **JSON**.

* **Autenticação:** (Planejado) JWT para segurança das rotas.
* **CORS:** O Backend permite requisições originadas do domínio do Frontend Web para garantir a comunicação segura entre diferentes portas locais.
* **Contratos de Dados:**
    * `GET /api/veiculos`: Retorna a frota cadastrada.
    * `POST /api/veiculos`: Cadastra novo veículo.

---

## 🛠️ Procedimento de Configuração Global

Para rodar o ecossistema completo localmente:

1.  **Inicie o Backend:**
    - Vá para o repositório `travelplan-api`.
    - Execute o comando `./mvnw spring-boot:run`.
    - Verifique se a API está respondendo em `http://localhost:8080`.

2.  **Inicie o Frontend:**
    - Vá para o repositório `travelplan-web`.
    - Execute `npm install` seguido de `npm run dev`.
    - Acesse `http://localhost:5173`.

---

## 📅 Roadmap de Evolução

- [x] Integração Base (Web + API).
- [ ] Implementação de Módulo de Custos (Combustível/Pedágios).
- [ ] Sincronização offline para o App Android.
- [ ] Dashboard de estatísticas de viagem no Frontend Web.

---

**Mantenedor:** Jackson Santos
**Organização:** [travelplan-project](https://github.com/travelplan-project)
