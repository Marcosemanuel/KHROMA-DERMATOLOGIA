<div align="center">
  <!-- Sugestão: Adicione aqui uma imagem ou GIF de capa do Khroma (ex: mockup do celular/desktop) -->
  <h1>Khroma Copiloto Clínico</h1>
  <p><strong>Inteligência Artificial de Alto Padrão para Análise e Prescrição Médica</strong></p>
</div>

---

## 📖 Visão Geral (Overview)

O **Khroma** é uma plataforma SaaS (Software as a Service) desenvolvida para auxiliar médicos e profissionais de saúde na estruturação e análise de relatórios clínicos. O foco absoluto do produto é garantir **precisão técnica**, **agilidade** e uma **experiência de usuário (UX) premium**, nivelada aos mais altos padrões de design de mercado (clean aesthetic, glassmorphism, foco em conversão).

> 🔒 **Nota de Propriedade Intelectual:** O código-fonte original deste projeto é mantido em um repositório privado devido a algoritmos proprietários de IA e integrações de segurança médica. Este repositório serve como uma vitrine (Showcase) da arquitetura, stack tecnológico e soluções de engenharia implementadas.

---

## 🚀 Impacto e Funcionalidades Core

* **Análise Clínica com IA:** Workflow otimizado em que o médico envia dados de um caso e recebe uma resposta formatada e estruturada em Markdown de forma assíncrona.
* **UX/UI de Alta Conversão:** Interface focada em evitar atrito cognitivo. Utiliza animações fluidas (Framer Motion), feedback instantâneo e design focado no usuário de saúde, auditado para os mais altos padrões de acessibilidade (ARIA).
* **Paywall e Monetização Inteligente:** Fluxo de assinatura com múltiplas camadas (Planos Clínico e Especialista) e modelo de Tripwire (Free Trial otimizado para R$1,99) que ajuda na filtragem de leads e mitigação de perdas. Tudo gerenciado com Webhooks Seguros.
* **Telemetry & Tracking Profissional:** "Gold Standard" de eventos usando a Conversions API (CAPI) do Meta, com deduplicação perfeita entre os eventos do navegador (Pixel via React) e backend (Edge Functions via Webhook do Stripe).

---

## 🛠️ Stack Tecnológico (Tech Stack)

### Frontend (User Interface)

* **Framework:** React / Vite (SPA Otimizado)
* **Styling & UI:** Tailwind CSS v3/v4, shadcn/ui (Componentes desacomplados e acessíveis).
* **Animações:** Framer Motion (Curvas de `easing` customizadas para fluidez premium).
* **Roteamento:** React Router DOM.
* **Gerenciamento de Estado & Mutação:** Hooks Customizados (ex: `useDirectCheckout`), Context API.
* **SEO e Metadados:** React Helmet Async (Gerenciamento dinâmico do `<head>` para máxima taxa de clique - CTR).

### Backend & BaaS (Backend as a Service)

* **Plataforma Core:** Supabase (BaaS autogerenciado).
* **Banco de Dados:** PostgreSQL hospedado (com RLS rígido para segurança dos perfis e dados do usuário).
* **Edge Functions:** Funções serverless escritas em Deno/TypeScript (`analyze-derma`, `stripe-webhook`, `meta-conversions-api`) para segurança máxima de chaves de serviço e integrações (OpenAI e Stripe).
* **Autenticação:** Supabase Auth (Magic Links, OAuth, senhas fortes).

### Integrações de Terceiros

* **Inteligência Artificial:** OpenAI API (GPTs) para processamento da árvore de decisões clínicas.
* **Pagamentos:** Stripe (Checkout Sessions, Webhooks, Billing Portal, Produtos).
* **Marketing & Atribuição:** Meta Pixel + Facebook Conversions API (CAPI) para eventos Offline/Server-side (`InitiateCheckout`, `Purchase`, `Subscribe`).

---

## 🏗️ Arquitetura e Soluções de Engenharia Destaque

Neste projeto, apliquei metodologias complexas para resolver problemas reais de SaaS:

1. **Supabase Edge Functions para Webhooks Resilientes do Stripe:**
   O processamento do pagamento (renovações de planos, compras de créditos, trial `tripwire`) ocorre de ponta a ponta no backend Deno usando chaves de serviço de acesso restrito (Service Role Access). O script lida graciosamente com falhas, deduplicação de eventos, alocação de créditos ao usuário e "downgrade" seguro (Graceful Degradation).

2. **Deduplicação de Eventos do Facebook (CAPI & Pixel):**
   A arquitetura garante precisão total dos dados ao disparar um `fbpixel.trackPurchase` e/ou `trackInitiateCheckout` na camada frontend, e _simultaneamente_ registrar a efetivação no backend, unindo os eventos em um único Funnel (Hash CAPI) no gerenciador de anúncios do Facebook sem duplicar lucros/cadastros.

3. **Design System & Acessibilidade Progressiva:**
   Não utilizei geradores automáticos genéricos. A interface possui componentes robustos reconstruídos com HTML semântico, atributos `<aria-label>`, paleta baseada em tons de "Earthy Red & Stone" padronizada no `index.css` global, otimizando LCP (Largest Contentful Paint) através do Minifier da build.

4. **Automação de Pipelines & Auditorias Constantes:**
   Foi implementado um ecossistema de scripts independentes (em Python) para rodar Lints em massa, varredura de Segurança Crítica (Security Scans baseados na OWASP 2025) e Verificações de UX e SEO antes de todo deploy, que consolidam os relatórios para atestar a qualidade Enterprise do software compilado.

---

## 📸 Demonstração Visual da Experiência (UI)

_No seu repositório oficial, adicione abaixo:_

* `[Screenshot 1 - Hero Section e Proposta de Valor]`
* `[GIF do fluxo de Upload de Análise ocorrendo em real-time]`
* `[Screenshot 2 - Paywall de Alta Conversão]`

---

## 🙋‍♂️ Sobre o Autor / Contato

_Desenvolvido pela minha consultoria (ou por mim), integrando design thinking, engenharia distribuída full-stack e machine learning (LLMs) corporativo._

* **LinkedIn:** [Insira seu link aqui]
* **Portfólio Pessoal:** [Insira seu link aqui]
* **E-mail:** [Insira seu contato aqui]
