# ==============================================================================
# DESAFIO 1: Validação de Pedidos de Servidores
# ==============================================================================
entrada_servidores = input().split()

projeto = entrada_servidores[0]
solicitados = int(entrada_servidores[1])
limite = int(entrada_servidores[2])

if solicitados < 0 or limite < 0:
    print("INVALID")
else:
    if solicitados <= limite:
        print("APPROVED")
    else:
        print("REJECTED")

# ==============================================================================
# DESAFIO 2: Monitoramento de Saúde de Instâncias
# ==============================================================================
status_instancia = input()

if status_instancia == "up":
    print("running")
elif status_instancia == "down":
    print("alert")
elif status_instancia == "idle":
    print("standby")
else:
    print("invalid")

# ==============================================================================
# DESAFIO 3: Verificador de Sinais de Status (CPU, Memória e Rede)
# ==============================================================================
entrada_sinais = input().split()
valores_validos = {"ok", "fail"}

if len(entrada_sinais) != 3 or any(status not in valores_validos for status in entrada_sinais):
    print("invalido")
else:
    quantidade_falhas = entrada_sinais.count("fail")

    if quantidade_falhas == 0:
        print("normal")
    elif quantidade_falhas == 1:
        print("alerta")
    else:
        print("incidente")
