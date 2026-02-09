# Dashboard-de-volumetria-de-atendimento
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("dados_atendimento.csv")

resumo = df.groupby("canal")["quantidade"].sum()

print("Resumo por canal:")
print(resumo)

resumo.plot(kind="bar", title="Volume por canal")
plt.ylabel("Quantidade")
plt.show()
