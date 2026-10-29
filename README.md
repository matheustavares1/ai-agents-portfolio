# Matheus Tavares — Portfólio de IA

Desenvolvedor e fundador da **[Bridg AI](https://www.bridgai.com.br)**. Construo agentes de IA, automações e integrações que resolvem problemas reais de negócio, da conversa com o cliente até a solução em produção.

> 💬 **Teste um agente meu agora:** o atendimento da Bridg AI no WhatsApp é feito por um agente que eu construí. [Conversar com o agente](https://wa.me/5561991174763?text=Oi%21%20Vim%20pelo%20GitHub%20e%20quero%20testar%20o%20agente%20da%20Bridg%20AI)

---

## Projetos

### 🤖 [VOGA Concierge: agente com IA + painel de operação](./01-agente-concierge)
Agente no WhatsApp para os clientes premium da VOGA Wealth, assessoria de investimentos. Ele só conversa com quem é cliente, responde pela base de conhecimento (RAG), conhece o histórico de cada cliente e passa os pedidos para a equipe pelo WhatsApp em poucos minutos. Inclui campanhas pela API oficial da Meta, com freio por falhas e por gasto, e um painel web em que a equipe acompanha conversas e pedidos, cria campanhas e edita o prompt do agente. São 9 workflows, todos publicados aqui.

`n8n` `OpenAI` `RAG` `Supabase Vector Store` `Redis` `API oficial do WhatsApp` `Next.js`

🎬 [Vídeo do painel em uso (79 s)](./01-agente-concierge/README.md#demo)

### 💬 [Agente de atendimento da Bridg AI](./02-agente-bridg-ai)
O agente que atende quem chega à Bridg AI pelo WhatsApp, a qualquer hora. Entende o negócio da pessoa, mostra o que um agente faria por ela, marca a reunião de diagnóstico na agenda com Google Meet e manda o resumo do lead para mim. **Está no ar e pode ser testado pelo link acima.**

`n8n` `GPT-4.1 mini` `Evolution API` `Redis` `Google Agenda`

### 📊 [Conciliação bancária automatizada com IA](./03-conciliacao-bancaria)
Automação para o setor financeiro de uma corretora. A IA confere extratos com os lançamentos e trata as divergências que antes exigiam conferência manual.

<!-- TODO: ferramentas usadas e resultado (ex.: de X horas por semana para Y minutos) -->

### 🏠 [Vistera: staging virtual com IA para imóveis](./04-vistera)
Produto próprio. O corretor envia a foto do cômodo vazio e recebe o ambiente mobiliado em segundos, em dez estilos, preservando paredes, janelas e o ângulo da câmera. Inclui análise de mercado pelo endereço e proposta com PDF.

🔗 [Conhecer a plataforma](https://vistera-gamma.vercel.app)

### 🛠️ [Infraestrutura self-hosted](./05-infra)
Servidor próprio com n8n, Evolution API v2, Traefik e Redis em VPS, que é a base dos agentes acima.

---

## Como eu construo

- **Agentes que agem, não só respondem:** consultam sistemas, registram pedidos, marcam reuniões e acionam a equipe.
- **Pensando em produção:** buffer e deduplicação de mensagens, verificação do cliente antes da IA, filas no banco em vez de loops, freios automáticos, memória de longo prazo e alertas de erro em linguagem simples.
- **Segurança de IA:** regras fixas fora do prompt editável, dados do cliente tratados como informação e nunca como instrução, filtro de vazamento na resposta e regras determinísticas para o que não pode depender do modelo.
- **O cliente no controle:** painel para a equipe operar o agente, editar o prompt com histórico de versões e alimentar a base de conhecimento sem depender de mim.
- **Base de desenvolvedor:** também atuo com integrações no setor financeiro (APIs REST/SOAP, mensageria com AWS SQS, Java) e entendo o que roda por trás do agente.

## Stack

**IA nos agentes:** OpenAI (GPT-4.1 mini e `gpt-6-luna`, embeddings, transcrição de áudio), RAG, bancos vetoriais, tool calling, saída estruturada, prompt engineering
**Desenvolvimento com IA:** Claude Code e o MCP do n8n
**Automação:** n8n, Evolution API, API oficial do WhatsApp (Meta), webhooks
**Desenvolvimento:** TypeScript, React, Next.js, Python, Java, PostgreSQL, Supabase, Redis
**Infra:** Docker, VPS, Traefik, Vercel, AWS

## Sobre os workflows publicados

Os JSONs saíram do n8n de produção e foram sanitizados antes de entrar aqui: sem credenciais, URLs e domínios do servidor e dos clientes, telefones, e-mails, IDs ou dados de clientes. A única URL que ficou é a da API pública da Meta (`graph.facebook.com`), igual para qualquer conta. Quem importar troca os placeholders `{{NOME}}` (ou `<NOME>`, dentro de expressões do n8n) pelos próprios valores. Cada projeto explica como importar.

## Contato

🌐 [bridgai.com.br](https://www.bridgai.com.br) · 💼 [LinkedIn](https://linkedin.com/in/matheus-tavares-ramos) · ✉️ mt8822774@gmail.com
