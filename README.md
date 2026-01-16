# Newsletter aplicado em N8N
Workflow automatizado que busca, seleciona e envia notícias de economia e tecnologia para o Discord, utilizando IA para curadoria de conteúdo.

## Descrição
Este workflow automatiza a entrega diária de notícias relevantes para sua comunidade no Discord. Todos os dias às 6h da manhã, o bot:
- Busca notícias de Economia na Forbes
- Busca notícias de Tecnologia no G1
- Utiliza IA para selecionar as notícias mais relevantes
- Envia automaticamente para um canal específico do Discord

## Pré-requisitos
- n8n instalado (versão 1.0 ou superior)
- **Credenciais necessárias**:
1. Webhook do Discord (URL do canal)
2. API Key da IA (OpenAI, Anthropic ou similar)
3. Acesso à internet para scraping de notícias

## Instalação
- Importe o workflow no n8n:
1. Abra seu n8n
2. Vá em "Workflows" > "Import from File"
3. Selecione o arquivo ```Newsletter copy.json```

- Configure as credenciais:
1. Discord Webhook: Vá até o canal do Discord > Configurações > Integrações > Webhooks > Copie a URL
2. API da IA: Configure sua chave de API do serviço de IA escolhido
3. Adicione as credenciais nos respectivos nós.


- Ajuste os parâmetros:

1. Verifique o horário de disparo (padrão: 6h AM)
2. Configure o fuso horário correto
3. Ajuste o número de notícias a serem selecionadas (se necessário)

## Configuração
- Webhook do Discord

1. Acesse seu servidor Discord
2. Vá ao canal onde deseja receber as notícias
3. Clique na engrenagem (⚙️) > Integrações > Webhooks
4. Crie um novo webhook e copie a URL
5. Cole a URL no nó Discord do workflow

- Horário de Execução
O workflow está configurado para executar:

1. Horário: 06:00 AM (ajuste conforme seu fuso horário)
2. Frequência: 2 verificações por minuto durante a execução
3. Periodicidade: Diariamente

- Nós Principais

1. Schedule Trigger: Dispara o workflow diariamente às 6h
2. HTTP Request (Forbes): Busca notícias de economia
3. HTTP Request (G1): Busca notícias de tecnologia
4. IA/LLM Node: Seleciona as notícias mais relevantes usando IA
5. Discord Webhook: Envia as notícias formatadas para o Discord

- Como Usar

1. Ative o workflow no n8n
2. guarde a execução automática às 6h da manhã
3. Verifique as notícias no canal do Discord configurado
4. (Opcional) Execute manualmente clicando em "Execute Workflow" para testar

## Contribuição
Contribuições são sempre bem-vindas! Para contribuir:
- Reportar bugs
- Sugerir melhorias
- Enviar pull requests

## Licença
Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Autor
Thomas Muniz Bratfich
- GitHub: [@Bratfich-gif](https://github.com/Bratfich-gif)
- LinkedIn: [Thomas Bratfich](https://linkedin.com/in/thomasbratfich)


## Links Úteis
- [Documentação do N8N](https://docs.n8n.io/)
- [Comunidade N8N](https://community.n8n.io/)
