# HeatIA-Recife

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red?style=for-the-badge&logo=pytorch)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0+-orange?style=for-the-badge&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)

Sistema de previsão e classificação de acidentes de trânsito em Recife utilizando Deep Learning e mapas interativos para identificação de áreas de alto risco.

[Funcionalidades](#funcionalidades) • [Tecnologias](#tecnologias) • [Instalação](#instalação) • [Uso](#uso) • [Resultados](#resultados) • [Contribuir](#contribuindo)

---

## Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Tecnologias](#tecnologias)
- [Arquitetura](#arquitetura)
- [Instalação](#instalação)
- [Uso](#uso)
- [Resultados](#resultados)
- [Próximos Passos](#próximos-passos)
- [Contribuindo](#contribuindo)
- [Licença](#licença)

---

## Sobre o Projeto

**HeatIA-Recife** é um projeto de análise preditiva e classificação de acidentes de trânsito na cidade de Recife, desenvolvido com redes neurais profundas (PyTorch) e técnicas avançadas de aprendizado de máquina. O sistema analisa padrões históricos de acidentes e prevê áreas críticas para 2025, auxiliando na tomada de decisões estratégicas em segurança viária.

### Principais Características

- **Previsão Inteligente** - Modelo de Deep Learning para estimar acidentes futuros
- **Classificação de Riscos** - Categorização em baixo, médio e alto risco
- **Mapas Interativos** - Visualização geoespacial com mapas de calor
- **Análise Geoespacial** - Identificação de hotspots e áreas críticas
- **Insights Acionáveis** - Suporte para políticas públicas de segurança viária
- **Código Aberto** - Disponível para comunidade e pesquisadores

---

## Funcionalidades

### Análise Preditiva

- **Previsão de Acidentes** - Estimativa de locais com maior probabilidade de acidentes em 2025
- **Modelos de Deep Learning** - Redes neurais treinadas com dados históricos
- **Validação Cruzada** - Métricas de performance e acurácia do modelo
- **Feature Engineering** - Extração de padrões espaciais e temporais

### Classificação de Riscos

- **Níveis de Severidade** - Classificação em baixo, médio e alto risco
- **Score de Risco** - Pontuação numérica para cada localização
- **Priorização** - Identificação de áreas que necessitam intervenção urgente
- **Análise Comparativa** - Evolução temporal dos riscos

### Visualização

- **Mapas de Calor** - Representação visual interativa dos pontos críticos
- **Camadas Customizáveis** - Filtros por severidade, período e região
- **Geocodificação** - Conversão de coordenadas em endereços legíveis
- **Exportação** - Geração de relatórios em HTML

---

## Tecnologias

### Machine Learning & Deep Learning

| Tecnologia   | Versão | Descrição                  |
| ------------ | ------ | -------------------------- |
| Python       | 3.8+   | Linguagem de programação   |
| PyTorch      | 2.0+   | Framework de Deep Learning |
| Scikit-Learn | 1.0+   | Biblioteca de ML           |
| NumPy        | 1.21+  | Computação numérica        |

### Análise de Dados

| Tecnologia | Versão | Descrição                  |
| ---------- | ------ | -------------------------- |
| Pandas     | 1.3+   | Manipulação de dados       |
| Matplotlib | 3.4+   | Visualizações estáticas    |
| Seaborn    | 0.11+  | Visualizações estatísticas |

### Geoespacial

| Tecnologia | Versão | Descrição           |
| ---------- | ------ | ------------------- |
| Folium     | 0.12+  | Mapas interativos   |
| Geopy      | 2.2+   | Geocodificação      |
| GeoPandas  | 0.10+  | Análise geoespacial |

---

## Arquitetura

### Estrutura do Projeto

```
HeatIA-Recife/
├── data/                    # Dados brutos e processados
│   └── acidentes2024.csv   # Dataset de acidentes
├── models/                  # Modelos treinados
│   └── model_checkpoint.pth
├── notebooks/              # Jupyter Notebooks
│   └── HeatIA_Recife.ipynb
├── outputs/                # Mapas e relatórios gerados
│   └── mapa_acidentes_2025.html
├── scripts/                # Scripts auxiliares
│   └── treinar_modelo.py
├── requirements.txt        # Dependências do projeto
└── README.md              # Documentação
```

### Pipeline de Dados

```
Dados Históricos
      ↓
Pré-processamento → Limpeza e Feature Engineering
      ↓
Treinamento → Modelo PyTorch (Rede Neural)
      ↓
Previsão → Estimativas para 2025
      ↓
Classificação → Categorização de Riscos
      ↓
Visualização → Mapas Interativos
```

---

## Instalação

### Pré-requisitos

- Python 3.8 ou superior
- pip (gerenciador de pacotes Python)
- Git

### Instalação Local

#### 1. Clone o repositório

```bash
git clone https://github.com/nevesmarcos42/HeatIA-Recife.git
cd HeatIA-Recife
```

#### 2. Crie um ambiente virtual (recomendado)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

#### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

#### 4. Verifique a instalação

```bash
python --version
pip list
```

---

## Uso

### Executar o Notebook

1. **Inicie o Jupyter Notebook:**

```bash
jupyter notebook HeatIA_Recife.ipynb
```

2. **Execute as células sequencialmente:**
   - Carregamento dos dados
   - Pré-processamento
   - Treinamento do modelo
   - Geração de previsões
   - Criação dos mapas

### Treinar o Modelo

```bash
python scripts/treinar_modelo.py
```

### Gerar Mapas de Calor

```bash
python scripts/gerar_mapas.py
```

### Visualizar Resultados

1. Após a execução, um arquivo `mapa_acidentes_2025.html` será gerado
2. Abra o arquivo no navegador para visualizar os mapas interativos
3. Interaja com as camadas para explorar diferentes níveis de risco

---

## Resultados

### Métricas do Modelo

- ✅ **Acurácia de Previsão** - Modelo ajustado com dados históricos de 2024
- ✅ **Identificação de Hotspots** - Mapeamento de áreas de alto risco
- ✅ **Classificação Precisa** - Categorização em 3 níveis de severidade
- ✅ **Visualização Interativa** - Mapas de calor com geolocalização

### Principais Insights

- **Zonas Críticas** - Identificação de regiões com maior concentração de acidentes
- **Padrões Temporais** - Horários e dias com maior incidência
- **Fatores de Risco** - Variáveis que contribuem para acidentes
- **Suporte à Decisão** - Dados para políticas públicas de segurança

---

## Próximos Passos

- [ ] **Novas Variáveis** - Incluir dados climáticos e de tráfego em tempo real
- [ ] **Expansão Geográfica** - Ampliar análise para outras cidades do Nordeste
- [ ] **API REST** - Desenvolver serviço web para consultas
- [ ] **Dashboard Interativo** - Interface web com Streamlit ou Dash
- [ ] **Modelos Avançados** - Testar arquiteturas Transformer e GNN
- [ ] **Integração** - Conectar com sistemas de trânsito municipais
- [ ] **App Mobile** - Aplicativo para consulta de áreas de risco

---

## Contribuindo

Contribuições são bem-vindas! Siga os passos:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

### Padrões de Código

- Seguir PEP 8 para código Python
- Documentar funções com docstrings
- Adicionar testes para novas funcionalidades
- Manter notebooks limpos e bem comentados

---

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

**Desenvolvido como projeto de pesquisa em Deep Learning e Segurança Viária**

**Versão:** 1.0.0  
**Última Atualização:** Novembro 2024

---

## Contato

**Marcos Neves** - [@nevesmarcos42](https://github.com/nevesmarcos42)

**Link do Projeto:** [https://github.com/nevesmarcos42/HeatIA-Recife](https://github.com/nevesmarcos42/HeatIA-Recife)

Para dúvidas ou sugestões, abra uma [Issue](https://github.com/nevesmarcos42/HeatIA-Recife/issues) ou entre em contato diretamente!
