Relatório de Análise Preditiva: Evasão de Clientes
Objetivo

O objetivo deste estudo foi desenvolver modelos preditivos capazes de identificar clientes com maior probabilidade de evasão (churn), utilizando dados históricos da empresa. A partir dos resultados, buscamos compreender os fatores que mais influenciam a evasão e propor estratégias de retenção.

2 - Preparação dos Dados
Fonte: Arquivo df_normalizado.csv
Tratamentos aplicados:

Remoção de colunas irrelevantes (customerID, PaperlessBilling, etc.)

Codificação de variáveis categóricas com OneHotEncoder

Balanceamento da variável alvo Churn com SMOTE

Normalização dos dados para modelos sensíveis à escala (Regressão Logística)

3 - Modelos Utilizados
Regressão Logística

Motivo da escolha: Modelo linear, interpretável, sensível à escala.
Pré-processamento: Normalização com StandardScaler
Desempenho:
Acurácia: 0.763
Precisão: 0.742
Recall: 0.808
F1-score: 0.773
Random Forest

Motivo da escolha: Modelo robusto, não sensível à escala, bom para dados tabulares.
Pré-processamento: Sem normalização
Desempenho:
Acurácia: 0.852
Precisão: 0.839
Recall: 0.872
F1-score: 0.855
4 - Avaliação Comparativa
Regressão Logística

Acurácia: 0.763
Precisão: 0.742
Recall: 0.808
F1-Score: 0.773
Random Forest

Acurácia: 0.852
Precisão: 0.839
Recall: 0.872
F1-Score: 0.855
Conclusão: O modelo Random Forest apresentou desempenho superior em todas as métricas, com maior capacidade de generalização e menor risco de overfitting.

5 - Análise das Variáveis Mais Relevantes
Regressão Logística – Top 5 variáveis por coeficiente

Contract_Two year → Reduz evasão
InternetService_Fiber optic → Aumenta evasão
PaymentMethod_Electronic check → Aumenta evasão
OnlineSecurity_No → Aumenta evasão
tenure → Reduz evasão
Random Forest – Top 5 variáveis por importância

tenure
MonthlyCharges
TotalCharges
Contract_Two year
OnlineSecurity_No
Conclusão:

Clientes com contratos mais curtos, sem segurança online, e pagamento eletrônico têm maior risco de evasão.
Clientes com maior tempo de contrato e valores mais altos pagos mensalmente tendem a permanecer.
6 - Estratégias de Retenção
Com base nas variáveis mais influentes, propomos:

Incentivar contratos de longo prazo

Oferecer descontos ou benefícios para migração para planos anuais ou bienais.
Melhorar a percepção de segurança

Promover o serviço de segurança online como diferencial.
Oferecer testes gratuitos ou pacotes com segurança incluída.
Revisar métodos de pagamento

Clientes que usam pagamento eletrônico têm maior evasão.
Incentivar débito automático ou cartão com benefícios exclusivos.
Fidelizar clientes com menor tempo de contrato

Criar campanhas de engajamento nos primeiros meses.
Oferecer bônus de fidelidade progressiva.
7 - Considerações Finais
O modelo Random Forest se mostrou mais eficaz para prever evasão.

A análise das variáveis permitiu identificar padrões comportamentais e contratuais que influenciam a decisão do cliente.

As estratégias propostas podem ser aplicadas em campanhas de retenção, segmentação de risco e personalização de ofertas.
