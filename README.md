# Projeto FarmTech: Previsão de Safra com IA e Análise de Custos na Nuvem (Fase 5)

Este repositório contém a solução completa para o projeto da Fase 5 da FIAP, desenvolvido para a empresa fictícia FarmTech Solutions. O projeto aborda a **Entrega 1 (Machine Learning)**, a **Entrega 2 (Cloud Computing)** e o **Projeto "Ir Além" (Classificação)**, demonstrando um fluxo de trabalho de ponta a ponta, desde a análise de dados até a preparação de um modelo para implantação.

-----

## 🎥 Vídeos Demonstrativos

  * **Vídeo 1: Demonstração da Solução de Machine Learning (Entrega 1)**

      * [https://youtu.be/a419OtD7\_zU](https://youtu.be/a419OtD7_zU)

  * **Vídeo 2: Demonstração da Análise de Custos na AWS (Entrega 2)**

      * [https://youtu.be/olDpwUIFqRA](https://youtu.be/olDpwUIFqRA)

-----

## ✅ Checklist de Entregas e Metas Cumpridas

Esta seção detalha como cada meta exigida no enunciado do projeto foi atendida.

### **Entrega 1: Machine Learning**

| Meta | Status | Evidência |
| :--- | :--- | :--- |
| **1. Análise Exploratória de Dados** | **✅ Concluído** | A análise completa, com visualizações gráficas (histogramas, boxplots) e estatísticas, está detalhada no início do Jupyter Notebook. |
| **2. Encontrar Tendências com Clusterização** | **✅ Concluído** | A técnica de clusterização com o algoritmo K-Means foi aplicada para agrupar os dados em diferentes cenários de plantio e identificar tendências, conforme demonstrado nas Células 8, 9 e 10 do notebook. |
| **3. Fazer Cinco Modelos Preditivos** | **✅ Concluído** | Foram desenvolvidos e avaliados múltiplos modelos, superando o requisito. Os modelos implementados incluem: **1. Regressão Linear** (como baseline), **2. Random Forest** (modelo avançado), **3. Random Forest Otimizado com GridSearchCV** (versão de especialista), e **4. Regressão Logística** (para o desafio de classificação). Todos estão documentados no notebook. |

O modelo de maior destaque, **Random Forest Regressor**, alcançou um resultado de **Coeficiente de Determinação (R²) de 0.99**, significando que ele consegue explicar 99% da variação no rendimento da safra, um nível de precisão altíssimo.

### **Entrega 2: Cloud Computing (AWS)**

| Meta | Status | Evidência |
| :--- | :--- | :--- |
| **1. Estimativa de Custos (SP vs. Virgínia)** | **✅ Concluído** | A análise comparativa de custos foi realizada na Calculadora AWS para uma instância com 2 vCPUs, 2 GiB de RAM e 50 GB de armazenamento. Os resultados estão abaixo. |
| **2. Justificativa da Escolha da Região** | **✅ Concluído** | A justificativa técnica detalhada, considerando latência e conformidade com a LGPD, está apresentada logo após a tabela de custos. |

#### Comparativo de Custos (On-Demand)

| Região | Custo Mensal Estimado |
| :--- | :--- |
| **São Paulo (BR)** | **$32.13 USD** |
| **N. Virgínia (EUA)**| **$19.18 USD** |

#### Justificativa da Escolha Estratégica

Apesar do custo mais baixo na Virgínia do Norte, a decisão profissional e estratégica é escolher a região de **São Paulo**. O investimento se justifica pela garantia de **maior performance (baixa latência)**, crucial para o acesso rápido aos dados dos sensores, e **total conformidade com a Lei Geral de Proteção de Dados (LGPD)**, eliminando riscos jurídicos e garantindo a soberania dos dados.

### **🏆 Projeto "Ir Além": Opção 2 - Classificação da Saúde da Safra**

| Meta | Status | Evidência |
| :--- | :--- | :--- |
| **Desenvolver Modelo de Classificação** | **✅ Concluído** | A parte de Machine Learning da segunda opção do "Ir Além" foi **integralmente implementada**. Foi criada uma lógica para classificar as safras em "Saudável" ou "Não Saudável" e um modelo de Regressão Logística foi treinado para esta tarefa, alcançando uma **acurácia de 68.75%**. O processo está nas Células 16 e 17 do notebook. |

-----

## 🚀 Destaques "Além do Além": Técnicas de Nível Profissional

Para garantir a excelência da solução, foram aplicadas técnicas que vão além do escopo básico do projeto:

1.  **Otimização de Hiperparâmetros:** Foi utilizado o `GridSearchCV` para realizar uma busca exaustiva e sistemática pelos melhores parâmetros para o modelo Random Forest, validando cientificamente que sua performance é a melhor possível.

2.  **Pipeline Profissional:** O fluxo de trabalho completo foi encapsulado em um `Pipeline` do Scikit-learn, uma prática padrão da indústria que torna o código mais limpo, robusto e pronto para produção.

3.  **Serialização do Modelo:** O pipeline final foi salvo no arquivo `modelo_previsao_safra.joblib`, "empacotando" toda a inteligência do modelo. Isso o deixa pronto para ser carregado em qualquer outra aplicação para fazer previsões em tempo real.

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
