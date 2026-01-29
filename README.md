# 🏆 Brasileirão Analytics 2026

Sistema completo de análise de desempenho para equipes e jogadores do Campeonato Brasileiro Série A e B 2026.

## 📋 Funcionalidades

### Análise de Equipes
- Estatísticas de desempenho (vitórias, empates, derrotas)
- Análise de gols (marcados, sofridos, saldo)
- Desempenho como mandante vs visitante
- Evolução ao longo do campeonato
- Análise de sequências (invencibilidade, vitórias consecutivas)
- Comparação entre equipes

### Análise de Jogadores
- Estatísticas individuais (gols, assistências, cartões)
- Desempenho por posição
- Ranking de artilheiros e garrafões
- Análise de eficiência
- Comparação entre jogadores

### Visualizações
- Gráficos de evolução de pontuação
- Tabelas de classificação interativas
- Heatmaps de desempenho
- Gráficos de radar para comparação
- Análise de correlações

## 🚀 Instalação

```bash
# Clone o repositório
git clone <seu-repositorio>
cd brasileirao_analytics

# Crie um ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate  # Windows

# Instale as dependências
pip install -r requirements.txt
```

## 📊 Uso

### 1. Coletar Dados
```python
from src.data_collector import BrasileiraoCollector

collector = BrasileiraoCollector()
collector.fetch_serie_a_data()
collector.fetch_serie_b_data()
```

### 2. Análise de Equipes
```python
from src.team_analyzer import TeamAnalyzer

analyzer = TeamAnalyzer('data/serie_a.csv')
stats = analyzer.get_team_stats('Flamengo')
analyzer.plot_team_evolution('Flamengo')
```

### 3. Análise de Jogadores
```python
from src.player_analyzer import PlayerAnalyzer

analyzer = PlayerAnalyzer('data/players.csv')
top_scorers = analyzer.get_top_scorers(limit=10)
analyzer.plot_player_comparison(['Jogador1', 'Jogador2'])
```

### 4. Gerar Relatórios
```python
from src.report_generator import ReportGenerator

report = ReportGenerator()
report.generate_full_report('Série A', output='reports/serie_a_report.html')
```

## 📁 Estrutura do Projeto

```
brasileirao_analytics/
├── data/                  # Dados brutos e processados
├── src/                   # Código fonte
│   ├── data_collector.py  # Coleta de dados
│   ├── team_analyzer.py   # Análise de equipes
│   ├── player_analyzer.py # Análise de jogadores
│   ├── visualizer.py      # Visualizações
│   └── report_generator.py # Geração de relatórios
├── notebooks/             # Jupyter notebooks
├── reports/               # Relatórios gerados
├── tests/                 # Testes unitários
└── requirements.txt       # Dependências
```

## 🛠️ Tecnologias

- **Python 3.8+**
- **Pandas**: Manipulação de dados
- **Matplotlib/Seaborn**: Visualizações
- **Plotly**: Gráficos interativos
- **BeautifulSoup**: Web scraping
- **Requests**: Requisições HTTP
- **Jupyter**: Análises exploratórias

## 📈 Exemplos de Análises

### Classificação Atual
```python
analyzer.get_standings()
```

### Melhor Ataque/Defesa
```python
analyzer.get_best_attack()
analyzer.get_best_defense()
```

### Aproveitamento
```python
analyzer.get_team_efficiency('Palmeiras')
```

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## 📝 Licença

MIT License

## 👥 Autor

Desenvolvido para análise do Campeonato Brasileiro 2026
