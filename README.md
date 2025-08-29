# Checkpoint 01 – Análise de Dados de Consumidores de Energia

Este repositório contém a solução completa para a atividade de análise de dados do dataset **Individual Household Electric Power Consumption** disponível no [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption). O objetivo é explorar e compreender padrões de consumo elétrico domiciliar entre 2006 e 2010.

## Estrutura do projeto

```
checkpoint01_repo/
└── notebooks/
    └── Checkpoint01_Energia.ipynb  # Notebook interativo com as resoluções
├── src/
│   └── energy_analysis.py          # Script Python para reproduzir as análises
├── outputs/                        # Diretório onde são salvos gráficos e CSVs gerados
├── README.md                       # Instruções e descrição do dataset
├── requirements.txt                # Bibliotecas necessárias para execução
└── .gitignore                      # Arquivos e diretórios a serem ignorados pelo Git
```

## Como executar

1. Faça o download do arquivo `household_power_consumption.txt` a partir do repositório da UCI: https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption.
2. Coloque o arquivo de dados na raiz deste repositório (no mesmo nível que este `README.md`). **Não faça commit deste arquivo**, pois ele é muito grande.
3. Crie um ambiente virtual (opcional) e instale as dependências:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # no Windows use .venv\Scripts\activate
   pip install -r requirements.txt
   ```

4. Execute o script de análise, indicando a localização do arquivo de dados e o diretório de saída para gráficos e tabelas:

   ```bash
   python src/energy_analysis.py --data household_power_consumption.txt --out outputs
   ```

   Isso criará diversos arquivos CSV com métricas, tabelas, e gráficos em `outputs/`.

5. Para explorar os passos de forma interativa, abra o notebook `notebooks/Checkpoint01_Energia.ipynb` no Jupyter e execute célula por célula. O notebook contém explicações e códigos correspondentes aos exercícios.

## Sobre o dataset

O dataset contém mais de 2 milhões de registros de consumo elétrico, medidos minuto a minuto, em uma residência localizada no sul da França. Cada linha possui variáveis como:

* **Global_active_power**: potência elétrica ativa média (kW) consumida.
* **Global_reactive_power**: potência elétrica reativa média (kVAR) – energia que não realiza trabalho útil, associada a campos magnéticos/indutivos.
* **Voltage**: tensão média (V).
* **Global_intensity**: corrente global média (A).
* **Sub_metering_1/2/3**: energia consumida por subcircuitos específicos (Wh).

Essas variáveis permitem explorar correlações, padrões diários e sazonais de consumo, além de aplicar técnicas de clusterização e modelagem preditiva.

## Licença

Este trabalho é acadêmico e segue as diretrizes da disciplina. O dataset original é disponibilizado sob a política do UCI Machine Learning Repository.
