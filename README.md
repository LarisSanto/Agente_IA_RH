<!-- Capa animada superior -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=2F2F2F&height=120&section=header" alt="Capa animada superior" width="1000" />
</p> 

# Agente de IA para Suporte ao RH.

Este projeto consiste em um Agente de IA inteligente integrado ao Telegram, desenvolvido com n8n, projetado para automatizar consultas e fornecer suporte imediato a colaboradores dentro de uma estrutura de Recursos Humanos.


### Visão Geral das Etapas.

O fluxo de trabalho foi dividido em etapas modulares para garantir escalabilidade e eficiência.


### Ingestão e Processamento de Dados.

Nesta etapa, preparamos a base de conhecimento que o Agente irá consultar:
- HTTP Request: Realiza a busca dos documentos ou políticas internas de RH hospedadas externamente (via URL).
- Default Data Loader: Processa os dados brutos recebidos.
- Embeddings Cohere: Converte o texto em vetores numéricos para permitir uma busca semântica eficiente.
- Simple Vector Store: Armazena esses vetores, permitindo que a IA recupere o contexto correto quando questionada.

<img width="1060" height="617" alt="image" src="https://github.com/user-attachments/assets/9e504493-42b8-430d-9f1d-569230525779" />

### Lógica do Agente e Integração.

Esta é a "inteligência" central do projeto:
- Telegram Trigger: O nó de entrada que aguarda mensagens de usuários.
- AI Agent: O cérebro do sistema, configurado com o modelo da Cohere. Ele orquestra as ferramentas disponíveis.
- Simple Memory: Garante que o agente mantenha o contexto da conversa, permitindo interações naturais e sequenciais.
- MySQL (Select Rows): Ferramenta utilizada pelo Agente para consultar diretamente tabelas de funcionários, permitindo que ele busque informações estruturadas (como dados cadastrais ou status de solicitações).
- Send a text message: O nó final que envia a resposta processada de volta ao usuário no Telegram. 

<img width="1191" height="598" alt="image" src="https://github.com/user-attachments/assets/ec7c00d4-7f02-45a6-9a5c-3cd24545b67c" />

### Exemplo de Execução.

Aqui demonstramos o agente em operação real:
- O fluxo é iniciado pelo comando /start.
- O Agente solicita a identificação do colaborador.
- Após a identificação, o Agente consulta o banco de dados (MySQL) para responder à dúvida específica do usuário.
- A interface de comunicação é amigável e direta, automatizando tarefas repetitivas que sobrecarregariam o setor de RH.  

<img width="1600" height="766" alt="image" src="https://github.com/user-attachments/assets/327f17e0-290a-491c-83d3-4b7cb725ffc4" />


### Tecnologias Utilizadas.

- n8n: Orquestração de fluxos e automação.
- Cohere: Processamento de Linguagem Natural (LLM).
- MySQL: Banco de dados relacional para dados de funcionários.
- Telegram API: Interface de atendimento ao usuário.
- Vector Search: Para recuperação de documentos e políticas internas.  



### Impacto de Negócio.

A análise permite:

- Identificar a loja com menor desempenho geral  
- Apoiar decisões estratégicas de investimento  
- Redirecionar recursos para unidades mais eficientes  
- Reduzir prejuízos operacionais  



### Reconhecimentos.

Este projeto foi desenvolvido como parte da Imersão Agente de IA da Alura. Agradeço à Alura e aos instrutores pela orientação e pelos conhecimentos compartilhados durante a jornada de aprendizado.



<br>
<br>
<!-- Capa animada inferior -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=2F2F2F&height=120&section=footer" alt="Capa animada inferior" width="1000" />
</p>

