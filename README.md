# Projeto FarmTech: Previsão de Safra com IA e Análise de Custos na Nuvem

Este projeto, desenvolvido para a Fase 5 do curso de IA da FIAP, apresenta uma solução de Machine Learning de ponta a ponta para a empresa fictícia FarmTech Solutions. O objetivo é prever o rendimento de safras agrícolas com alta precisão, encontrar tendências nos dados de produção e realizar uma análise de custos detalhada para a implantação da solução na nuvem AWS.

-----

## 🎥 Vídeos Demonstrativos

  * **Vídeo 1: Demonstração da Solução de Machine Learning (Entrega 1)**

      * *https://youtu.be/a419OtD7_zU*

  * **Vídeo 2: Demonstração da Análise de Custos na AWS (Entrega 2)**

      * *https://youtu.be/olDpwUIFqRA*

-----

## 📊 Metodologia e Resultados de Machine Learning

O desenvolvimento seguiu um fluxo de trabalho profissional, da análise exploratória à preparação de um modelo para produção.

### 1\. Análise Exploratória e Clusterização

A análise inicial dos dados revelou um insight crucial: as relações entre as variáveis (como temperatura e umidade) e o rendimento da safra (`Yield`) não eram lineares, apresentando correlações muito fracas. Isso demonstrou a necessidade de modelos de Machine Learning mais avançados para capturar os padrões complexos dos dados. Adicionalmente, foi utilizada a técnica de clusterização com o algoritmo K-Means para identificar grupos e tendências ocultas nos diferentes cenários de plantio.

### 2\. Modelagem Preditiva para Rendimento (Regressão)

O principal objetivo do projeto foi treinar um modelo capaz de prever o rendimento da safra. Após comparar modelos de base com modelos avançados, o **Random Forest Regressor** se destacou, alcançando um resultado espetacular:

  * **Coeficiente de Determinação (R²): 0.99**

Um R² de 0.99 significa que nosso modelo final consegue **explicar 99% da variação no rendimento da safra**, um nível de precisão altíssimo e de grande valor para o negócio.

### 🏆 Desafio "Ir Além": Classificação de Saúde da Safra

Para ir além da previsão numérica, o desafio de classificação foi integrado ao projeto. Foi criada uma nova variável (`Saude_Planta`) que rotula uma safra como "Saudável" ou "Não Saudável" com base em seu rendimento. Um modelo de **Regressão Logística** foi treinado para esta tarefa, alcançando uma **acurácia de 68.75%** e provando ser uma ferramenta viável para a detecção de safras com potencial de baixo rendimento.

-----

## 🚀 Destaques "Além do Além": Técnicas de Nível Profissional

Para garantir a excelência e robustez da solução, foram aplicadas técnicas que vão além do escopo básico do projeto:

1.  **Otimização de Hiperparâmetros:** Foi utilizada a biblioteca `GridSearchCV` para realizar uma busca exaustiva e sistemática pelos melhores parâmetros para o modelo Random Forest. Este processo validou que o modelo já operava em sua performance máxima, garantindo que nenhum potencial de precisão foi desperdiçado.

2.  **Pipeline Profissional:** O fluxo de trabalho completo, desde o pré-processamento dos dados (como a conversão de variáveis categóricas) até o treinamento do modelo final, foi encapsulado em um `Pipeline` do Scikit-learn. Esta é uma prática padrão da indústria que torna o código mais limpo, robusto e menos propenso a erros.

3.  **Serialização do Modelo (Pronto para Produção):** O pipeline final e treinado foi salvo no arquivo `modelo_previsao_safra.joblib`. Isso significa que a inteligência do modelo está "empacotada" e pronta para ser carregada em qualquer outra aplicação ou servidor para fazer previsões em tempo real, demonstrando o ciclo de vida completo de um projeto de IA.

-----

## ☁️ Análise de Custos na Nuvem AWS (Entrega 2)

Foi realizada uma estimativa de custos para hospedar a API da solução em uma instância EC2 (`t3.small`: 2 vCPUs, 2 GiB RAM, 50 GB SSD) em duas regiões estratégicas.

### Comparativo de Custos (On-Demand)

| Região | Custo Mensal Estimado |
| :--- | :--- |
| **São Paulo (BR)** | **$32.13 USD** |
| **N. Virgínia (EUA)**| **$19.18 USD** |

### Justificativa da Escolha Estratégica

À primeira vista, a análise de custos mostra uma vantagem clara para a região da Virgínia do Norte (EUA), que é aproximadamente 40% mais barata que a de São Paulo.

No entanto, para um projeto do mundo real como o da FarmTech Solutions, o custo não é o único fator. Dois requisitos críticos do negócio mudam completamente a decisão:

1.  **Performance e Baixa Latência:** O projeto exige "acesso rápido aos dados dos sensores". Como os sensores da fazenda estão no Brasil, hospedar a solução em **São Paulo** garante uma latência (tempo de resposta) muito menor. Em uma operação agrícola que depende de decisões rápidas, essa agilidade é uma necessidade operacional.

2.  **Segurança e Conformidade Legal (LGPD):** O projeto alerta para "restrições legais para armazenamento no exterior". Manter os dados gerados pela fazenda, que são um ativo estratégico, em servidores localizados no Brasil (**São Paulo**) elimina riscos e complexidades jurídicas relacionadas à **Lei Geral de Proteção de Dados (LGPD)**, garantindo que o projeto já nasça em total conformidade com a legislação brasileira.

**Conclusão da Escolha:**

Portanto, a decisão profissional e estratégica é escolher a região de **São Paulo**. Embora o custo mensal seja maior, o investimento se justifica pela garantia de maior performance (baixa latência) e total conformidade legal (soberania de dados), pilares essenciais para o sucesso e a segurança da operação.

-----

## 🛠️ Como Executar o Projeto

1.  Clone este repositório.
2.  Certifique-se de ter as bibliotecas Python necessárias instaladas:
    ```
    pandas
    numpy
    matplotlib
    seaborn
    scikit-learn
    jupyter
    joblib
    ```
3.  Abra e execute o Jupyter Notebook localizado em `notebooks/DiogoLeiteZequiniPinto_RM565535_pbl_fase5.ipynb`.