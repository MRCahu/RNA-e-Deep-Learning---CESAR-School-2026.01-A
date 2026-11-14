# Atividade 2 — California Housing em PyTorch

**Mauro Roberto Barbosa Cahu** · mrbc@cesar.school  
RNA e Deep Learning — CESAR School 2026.01-A · Professor Vitor Casadei

[Notebook executado](atividade_2.ipynb) · [Abrir no Colab](https://colab.research.google.com/github/MRCahu/RNA-e-Deep-Learning---CESAR-School-2026.01-A/blob/main/Atividade%202/atividade_2.ipynb)

A entrega adapta o pipeline do notebook 2.6 de salários do professor para oito entradas do California Housing. Inclui dicionário, `describe()`, dispersões de duas variáveis, divisão 70/15/15 com semente 42, padronização de X e y ajustada só no treino, `nn.Linear(8, 1)`, `nn.MSELoss`, `optim.SGD`, curvas de treino e validação, RMSE no teste em dólares, baseline da média do treino, oito pesos interpretados e conclusão.

## Resultado da execução

| Métrica no teste | Modelo linear | Média do treino |
|---|---:|---:|
| RMSE (US$) | 72.129,13 | 114.992,22 |
| MAE (US$) | 52.104,28 | 91.177,38 |
| R² | 0,6066 | aproximadamente zero |

Redução do RMSE: **37,27%**. A época **2.236** foi selecionada pela validação dentre 4.000 épocas, com taxa 0,05. Foram executadas todas as 20 células de código em ordem, sem erros. As saídas são da execução desta atividade no Colab; não foram herdadas do exemplo de salários.

## Reprodução

No Colab, use Ambiente de execução → Executar tudo. Em ambiente próprio, use Python 3.13 e `pip install -r requirements.txt`, depois abra o notebook em Jupyter e execute em sessão limpa. O primeiro `fetch_california_housing` exige internet e não requer login. Versões efetivamente verificadas estão na primeira saída e no arquivo de dependências; a instalação do Colab usa PyTorch CPU com sufixo `+cpu`. `ipython` fornece a exibição de tabelas e Markdown.

## Interpretação e limites

O maior peso positivo é MedInc; os maiores negativos são Latitude e Longitude. São associações condicionais, não efeitos causais. Os dados representam grupos de quarteirões do Censo de 1990 e valores medianos históricos, com teto próximo de US$ 500.001. O modelo gera erros extremos e sete previsões negativas no teste; não foram aplicados cortes após avaliar o teste. É uma referência didática, sem validação para precificar uma casa individual hoje.

O original do professor foi preservado. A adaptação mantém as 46 posições e os tipos de células e os identificadores do modelo-base, mas modifica textos e códigos para cumprir a nova tarefa e registra novas saídas. SHA-256 da referência: `4caa7b088f92883184f267a1c2c1c1dbe384d07005d27bcdfaa739e31abb3e99`.
