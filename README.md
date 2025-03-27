# PiroTrader.IA

Um sistema integrado de trading de criptomoedas autônomo operado por inteligência artificial.

## Visão Geral

O PiroTrader.IA foi projetado para operar 24/7, realizando operações de trading em múltiplos pares na Binance. O sistema inclui um operador de trading com IA que analisa o mercado e executa ordens automaticamente com dados reais.

## Características Principais

- **Trading Autônomo**: Opera 24/7 sem necessidade de intervenção humana
- **Múltiplos Pares**: Suporta diversos pares de criptomoedas na Binance
- **Análise Inteligente**: Utiliza IA para análise de mercado e tomada de decisões
- **Interface Web**: Monitoramento em tempo real através de dashboard web
- **Chat Integrado**: Comunicação com o sistema através de interface de chat
- **Portfólio Dinâmico**: Gerenciamento automático de portfólio
- **Notificações**: Alertas por email sobre operações e estado do sistema

## Estrutura do Projeto

```
PiroTrader.IA/
├── start_integrated.py                # Ponto de entrada do sistema
├── config/
│   └── config.yaml                    # Configurações do sistema
├── src/
│   ├── api/
│   │   ├── api_server.py              # Servidor API
│   │   ├── chat_server.py             # Servidor de chat
│   │   ├── binance_client.py          # Cliente para interação com a API da Binance
│   │   └── llm_client.py              # Cliente para interação com o LLM
│   ├── core/
│   │   ├── intelligent_trader.py      # Componente central que gerencia o trading
│   │   └── portfolio.py               # Gestão de portfólio e posições
│   ├── strategies/
│   │   └── strategy_manager.py        # Gerenciamento de estratégias de trading
│   ├── utils/
│   │   ├── config_manager.py          # Gerenciamento de configurações
│   │   └── logger.py                  # Configuração de logging
│   └── web/
│       └── app.py                     # Aplicação web (frontend)
```

## Configuração e Instalação

### Pré-requisitos

- Python 3.9+
- Conta na Binance com API Key
- Chave de API DeepSeek

### Instalação

1. Clone o repositório:
   ```
   git clone https://github.com/MedthIA/PiroTrader.IA.git
   cd PiroTrader.IA
   ```

2. Instale as dependências:
   ```
   pip install -r requirements.txt
   ```

3. Configure as variáveis de ambiente no arquivo `.env`:
   ```
   BINANCE_API_KEY="sua_chave_api"
   BINANCE_SECRET_KEY="sua_chave_secreta"
   DEEPSEEK_API_KEY="sua_chave_deepseek"
   EMAIL_SENDER="seu_email@gmail.com"
   EMAIL_PASSWORD="sua_senha_email"
   ```

4. Inicie o sistema:
   ```
   python start_integrated.py
   ```

## Uso

Após iniciar o sistema, acesse:

- **Interface Web**: http://localhost:8000
- **API**: http://localhost:8080/api
- **Chat**: http://localhost:8001

## Aviso de Risco

Este sistema opera com dinheiro real em operações de criptomoedas. O trading envolve risco significativo de perda financeira. Use por sua conta e risco.

## Licença

Este projeto é privado e não está disponível sob licença de código aberto.