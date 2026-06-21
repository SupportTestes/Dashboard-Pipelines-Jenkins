# 📊 Pipeline Dashboard

Interface web para importação, análise e comparação de resultados de pipelines do Jenkins através de arquivos JSON.

O objetivo do projeto é fornecer uma visão clara da saúde das pipelines, permitindo acompanhar métricas de sucesso, falhas, histórico de execuções e tendências ao longo do tempo de forma simples e visual.

---

## 🚀 Funcionalidades

### 📥 Importação de Execuções
- Importação de arquivos `execution_results.json`
- Upload por seleção de arquivo ou drag-and-drop
- Armazenamento local utilizando LocalStorage
- Nomeação personalizada das execuções

### 📈 Dashboard Geral
- Total de execuções importadas
- Taxa média de sucesso
- Quantidade total de falhas
- Resumo da última execução
- Gráficos de acompanhamento

### 📋 Gestão de Execuções
- Listagem completa de todos os runs importados
- Visualização detalhada de cada execução
- Exclusão de execuções armazenadas
- Consulta rápida das principais métricas

### 📊 Histórico e Tendências
- Evolução da taxa de sucesso
- Volume de jobs executadas
- Quantidade de falhas por execução
- Comparação de duração entre runs

### ⚖️ Comparação entre Execuções
- Comparação lado a lado de dois runs
- Diferença de taxa de sucesso
- Diferença de falhas
- Identificação de jobs com alteração de status
- Comparação visual através de gráficos

### 🔍 Análise Consolidada de Jobs
- Visualização de todas as jobs importadas
- Busca por nome
- Filtro por status
- Ordenação por:
  - Nome
  - Taxa de falha
  - Quantidade de execuções
- Estatísticas consolidadas de cada job

### 📄 Detalhamento de Execução
- Lista completa das jobs executadas
- Status individual
- Número do build
- Tempo de execução
- Mensagens de erro
- Filtros rápidos

---

## 🛠️ Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- Chart.js
- LocalStorage

---

## 📁 Estrutura Esperada do JSON

O dashboard espera um JSON no seguinte formato:

```json
{
  "JOB_LOGIN": {
    "status": "SUCCESS",
    "buildNumber": 120,
    "duration": 15
  },
  "JOB_CADASTRO": {
    "status": "FAILURE",
    "buildNumber": 121,
    "duration": 20,
    "error": "Elemento não encontrado"
  }
}
