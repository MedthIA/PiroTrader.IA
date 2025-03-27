# Changelog - PiroTrader.IA

## Versão 0.1 Beta - 27/03/2025

### Adicionado
- Implementação inicial do sistema PiroTrader.IA
- Integração com a API da Binance
- Servidor API REST para comunicação com o sistema
- Servidor de Chat WebSocket para interface de usuário
- Estratégias básicas de trading (RSI, MACD, Bollinger Bands)
- Gerenciamento de portfólio e posições
- Interface web para visualização de dados
- Sistema de notificações por email

### Corrigido
- Resolvido erro de "Timeout na inicialização" do servidor API:
  - Aumentado o timeout de inicialização de 3 para 10 segundos
  - Alterada a sequência de inicialização do servidor Flask (startup_success definido antes da inicialização do servidor)
  - Adicionada opção `threaded=True` ao Flask para melhorar desempenho
- Resolvido conflito de portas entre servidor API e web:
  - Alterada a porta do servidor API de 8000 para 8080 no arquivo de configuração
- Melhorada lógica de encerramento do servidor API e servidor de chat
- Adicionada rota `/shutdown` para permitir encerramento limpo do servidor API

### Conhecido
- Erro ocasional no encerramento do servidor de chat: "A coroutine object is required"
  - Implementada correção na função _cancel_all_tasks para encerramento limpo de tarefas assíncronas