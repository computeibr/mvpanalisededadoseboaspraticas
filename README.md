# MVP Análise de Dados e Boas Práticas

Passo a passo foi acessar minha conta kagle e baixar os arquivos de chuvas com minhas credenciais de api. Percebi que para divulgar seria necessário publicar os arquivos para posteriormente deixá-lo no githut e assim disponibilizar para análise mais prática e com permissões públicas.

1. Acessar o kaggle
2. baixar os dados do INMET https://www.kaggle.com/datasets/gregoryoliveira/brazil-weather-information-by-inmet
3. Descompactá-lo
4. Dicionário de Dados https://www.kaggle.com/datasets/gregoryoliveira/brazil-weather-information-by-inmet
5. Após baixar aproximadamente 8GB de dados, selecionei um conjunto de 250MB para uso nessa análise

Esta base é dividida em quatro sessões:

1. Dados brutos por ano (weather_YYYY)
2. Resumir dados por ano (weather_sum_YYYY)
3. Todos os dados resumidos disponíveis (weather_sum_all)
4. Informações das estações com último registro.


<span data-v-3b6f9c90="" class="text-atom__text">Matrícula: 4052025000144</span>


O conjunto de dados brutos predefiniu as colunas:

* ESTAÇÃO / STATION
* DATA (AAAA-MM-DD) / DATA (AAAA-MM-DD)
* HORA (UTC) / HORA (UTC)
* PRECIPITAÇÃO TOTAL HORARIA (mm) / TOTAL DE CHUVA HORARIA (mm)
* PRESSAO ATMOSFERICA AO NIVEL DA ESTACAO, HORARIA (mB) / PRESSÃO ATMOSFÉRICA NO NÍVEL DA ESTAÇÃO, TEMPO (mB)
* PRESSÃO ATMOSFÉRICA MÁX.NA HORA ANT. (AUT) (mB) / PRESSÃO ATMOSFÉRICA MÁX. NO TEMPO ANTERIOR. (AUT) (mB)
* PRESSÃO ATMOSFÉRICA MÍN. NA HORA ANT. (AUT) (mB) / ATMOSFERIC PRESSURE MIN. IN THE EARLY TIME. (AUT) (mB)
* RADIAÇÃO GLOBAL (W/m2) / RADIAÇÃO GLOBAL (W/m2)
* TEMPERATURA DO AR - BULBO SECO, HORARIA (C) / TEMPERATURA DO AR - BULBO SECO, TEMPO (C)
* TEMPERATURA DO PONTO DE ORVALHO (C) / TEMPERATURA DO PONTO DE ORVALHO (C)
* TEMPERATURA MÁXIMA NA HORA ANT. (AUT) (C) / TEMPERATURA MÁXIMA DO HORÁRIO ANTERIOR. (AU) (C)
* TEMPERATURA MÍNIMA NA HORA ANT. (AUT) (C) / TEMPERATURA MÍNIMA DO HORÁRIO ANTERIOR. (AU) (C)
* TEMPERATURA ORVALHO MAX. NA HORA ANT. (AUT) (C) / TEMPERATURA MÁXIMA DE ORVALHO. NO TEMPO PRIMEIRO. (AU) (C)
* TEMPERATURA ORVALHO MIN. NA HORA ANT. (AUT) (C) / TEMPERATURA DE ORVALHO MIN. NO TEMPO PRIMEIRO. (AU) (C)
* UMIDADE REL. MÁX. NA HORA ANT. (AUT) (%) / UMIDADE REL MÁX. NO TEMPO PRIMEIRO. (AU) (%)
* UMIDADE REL. MIN. NA HORA ANT. (AUT) (%) / REL. UMIDADE MIN NA HORA INI7 CIAL (AUT) (%)
* UMIDADE RELATIVA DO AR, HORARIA (%) / UMIDADE RELATIVA DO AR, HORAS (%)
* VENTO, DIREÇÃO HORARIA (gr) / VENTO, DIREÇÃO DO TEMPO (gr)
* VENTO, RAJADA MÁXIMA (m/s) / VENTO, ARMAS MÁXIMAS (m/s)
* VENTO, VELOCIDADE HORARIA (m/s) / VENTO, VELOCIDADE HORARIA (m/s)

6. Os Dados que vamos trabalhar são Consolidados dados e apresenta as colunas:

| Coluna                                        | Função   | Nova Coluna         |
| --------------------------------------------- | ---------- | ------------------- |
| PRECIPITAÇÃO TOTAL, HORÁRIO (mm)           | máx.      | chuva_máxima       |
| RADIAÇÃO GLOBAL (KJ/m²)                    | máx.      | rad_máx            |
| TEMPERATURA DO AR - BULBO SECO, HORARIA (°C) | significar | temperatura média  |
| TEMPERATURA MÁXIMA NA HORA ANT. (AUT) (°C)  | máx.      | temperatura_máx.   |
| TEMPERATURA MÍNIMA NA HORA ANT. (AUT) (°C)  | significar | temperatura mínima |
| UMIDADE RELATIVA DO AR, HORARIA (%)           | significar | hum_avg             |
| UMIDADE REL. MÁX. NA HORA ANT. (AU) (%)      | máx.      | hum_max             |
| UMIDADE REL. MÍN. NA HORA ANT. (AU) (%)      | min        | hum_min             |
| VENTO, RAJADA MÁXIMA (m/s)                   | máx.      | vento_máx.         |
| VENTO, VELOCIDADE HORARIA (m/s)               | significar | média do vento     |

7. Que vou disponibiliá-lo no Gogole Drive de forma pública dados_publicos_mvp/weather_sum_all.csv

Interessante no aprendizado

- Pude perceber que o conteúdo das aulas sendo bem aplicados nos documentos que decidi fazer a análise, o site do Kaggle visualizei o dicionário de dados, as pastas organizadas, códigos, origem dos dados claramente referenciada, atualizações frequentes, conjunto de metadados robusto. Exemplos: Inclui detalhes de cada estação automática: localização, parâmetros medidos, frequência temporal etc. Essenciais para quem pretende fazer análises espaciais ou temporais.
