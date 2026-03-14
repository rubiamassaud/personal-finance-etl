# Netflix Shows Analytics
> Análise exploratória e visualização interativa do catálogo da Netflix (filmes e séries).

## 📋 Tema do Projeto
Analisar o conjunto de dados “Netflix Shows” (Kaggle) para entender a composição do catálogo, identificar tendências de lançamentos, gêneros mais populares, distribuição geográfica e outras métricas relevantes, apresentando tudo em um dashboard interativo.

## 👥 Integrantes
| Nome      | GitHub               | Responsabilidade |
|-----------|----------------------|------------------|
| Rubia     | @rubia-github        | Definição da base de dados |
| Nicolas   | @nicolas-github      | Estruturação do repositório e README |
| Felipe    | @felipe-github       | Transformações (limpeza, tipos) |
| Vanderson | @vanderson-github    | Protótipo do Dashboard |
| Isaac     | @isaac-github        | Implementação do ETL com Pandas |

## 🎯 Objetivo da Análise
- Explorar a diversidade de gêneros, países e durações presentes no catálogo.  
- Identificar tendências temporais de adição de títulos.  
- Disponibilizar um dashboard que permita ao usuário filtrar e comparar métricas de forma dinâmica.

## 📂 Estrutura do Repositório
netflix-shows-analytics/ │ ├─ data/ │ └─ raw/ # CSV original (não versionado) │ └─ processed/ # Dados limpos (Parquet/CSV) │ ├─ notebooks/ │ └─ 01‑exploracao.ipynb │ ├─ src/ │ ├─ init.py │ ├─ etl.py │ └─ utils.py │ ├─ dashboard/ │ └─ app.py │ ├─ docs/ │ └─ .gitkeep │ ├─ .gitignore ├─ requirements.txt └─ README.md


## 📅 Planejamento (Primeira Etapa)
| Data | Marco | Responsável |
|------|-------|-------------|
| 20/03 | Criação do repo + README | Nicolas |
| 20/03 | Download e versionamento do CSV | Rubia |
| 24/03 | Limpeza e padronização dos dados | Felipe |
| 26/03 | Wireframe do dashboard (escolha de gráficos) | Vanderson |
| 28/03 | Script ETL completo (Pandas) | Isaac |
| 02/04 | Integração e testes do dashboard | Isaac & Vanderson |
| 04/04 | Revisão final e documentação | Todos |

## 🔧 Transformações (esboço)
- Conversão de `date_added` → `datetime`.  
- Explosão das colunas `cast` e `listed_in` em tabelas auxiliares.  
- Tratamento de valores nulos (`Desconhecido` ou remoção de linhas).  
- Criação de colunas derivadas (`duration_value`, `duration_unit`).  
- Geração de datasets intermediários (`genres.parquet`, `countries.parquet`).

## 📊 Ideia Inicial do Dashboard
- **Sidebar** com filtros: Ano de lançamento, Gênero, País, Tipo (Movie/TV Show).  
- **Gráficos principais**:  
  1. Bar – Quantidade por tipo.  
  2. Bar – Top 10 gêneros.  
  3. Line – Lançamentos ao longo dos anos.  
  4. Pie – Distribuição de ratings.  
  5. Map (choropleth) – Conteúdo por país.  
  6. Box/Violin – Duração média por gênero.  

> O dashboard será desenvolvido em **Streamlit** (arquivo `dashboard/app.py`).  
> Dependências: `pandas`, `numpy`, `streamlit`, `plotly`, `pydeck`.
📚 Referências
Kaggle – Netflix Shows: https://www.kaggle.com/datasets/shivamb/netflix-shows
Pandas docs: https://pandas.pydata.org/docs/
Streamlit docs: https://docs.streamlit.io/

