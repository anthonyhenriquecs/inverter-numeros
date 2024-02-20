# inverter-numeros

import pandas as pd

def inverter_e_pegar_9_primeiros(numero):
    numero_invertido = str(numero)[::-1]  # Inverte o número
    numero_invertido = numero_invertido[:9]  # Retorna os 9 primeiros dígitos do número invertido
    numero_invertido = numero_invertido[::-1]
    
    return numero_invertido
def formatar(valor):
    return "5561{}".format(valor)


tabela = pd.read_excel("Enviar.xlsx")
tabela["Número"] = tabela["Número"].apply(inverter_e_pegar_9_primeiros)
tabela["Número"] = tabela["Número"].apply(formatar)
display(tabela)
