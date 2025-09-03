# 🌍 Tutorial: Acessando Dados do ERA5 via API (Copernicus CDS)

O ERA5 é o conjunto de reanálises do ECMWF disponível no Copernicus Climate Data Store (CDS). Ele fornece dados globais de temperatura, precipitação, vento, radiação, pressão e muito mais, em alta resolução, no formato NetCDF.  

🔹 **Passo 1 — Criar conta no CDS**  
Acesse o [Copernicus Climate Data Store](https://cds.climate.copernicus.eu/) e crie uma conta gratuita. Depois de logado, vá em "Your profile" → "API key". 
Nessa aba vamos copiar duas coisas:
url: sua-url
key: sua-key
---
🔹 Passo 2 — Instalar dependência no Python
pip install cdsapi
---
🔹 Passo 3 — Criar arquivo cdsapi
No diretório home do seu usuário (ex.: C:\Users\seu_usuario\ no Windows ou /home/usuario/ no Linux), crie o arquivo chamado .cdsapirc no bloco de notas mesmo, com o seguinte conteúdo:
url: sua-url
key: sua-key
---
######### DESCRIÇÃO DO SCRIPT #########

# 🌍 Download e Processamento de Dados ERA5 via Copernicus API  

Este repositório contém um script em **Python** para realizar o **download, tratamento e visualização de dados climáticos do ERA5** por meio da API do **Copernicus Climate Data Store (CDS)**.  

O código foi desenvolvido para análises meteorológicas e ambientais, com foco em variáveis atmosféricas como **temperatura a 2 metros**, podendo ser adaptado para outras variáveis da reanálise ERA5.  

---

## ⚙️ Etapas principais do script  

**Conexão com a API do Copernicus**  
- Autenticação via arquivo `.cdsapirc`  
- Inicialização do cliente `cdsapi`  

**Download dos dados**  
- Produto: `reanalysis-era5-single-levels`  
- Variável: `2m_temperature`  
- Seleção de datas e horários  
- Saída em formato **NetCDF**  

**Processamento e manipulação**  
- Leitura de arquivos NetCDF com `xarray`  
- Organização temporal e espacial dos dados  
- Conversão de unidades e ajustes numéricos  

**Visualização dos dados**  
- Mapas temáticos com `matplotlib` e `cartopy`  
- Inserção de camadas geográficas (`coastlines`, `borders`, `states`)  
- Colormaps customizados  

---

## 📊 Variáveis de saída  
| Variável | Descrição |  
|----------|------------|  
| t2m | Temperatura do ar a 2 metros (K ou °C após conversão) |  
| latitude / longitude | Localização espacial dos dados |  
| time | Série temporal das variáveis baixadas |  

---

## 🎯 Aplicações  
- Estudos de variabilidade climática e tendências de longo prazo  
- Monitoramento meteorológico em diferentes escalas temporais  
- Modelagem hidrológica e agrícola com dados de reanálise  
- Integração com outros dados ambientais (precipitação, vento, radiação etc.)  

---

## 🛠️ Tecnologias utilizadas  
- **Python 3.x**  
- [cdsapi](https://pypi.org/project/cdsapi/)  
- [xarray](https://docs.xarray.dev/)  
- [numpy](https://numpy.org/)  
- [pandas](https://pandas.pydata.org/)  
- [geopandas](https://geopandas.org/)  
- [matplotlib](https://matplotlib.org/)  
- [cartopy](https://scitools.org.uk/cartopy/docs/latest/)  
