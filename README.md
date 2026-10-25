# sistema-cadastro-colaboradores-python
Sistema de cadastro de colaboradores desenvolvido em Python, com menu interativo no terminal. O projeto permite cadastrar colaboradores, consultar registros e praticar conceitos fundamentais de programação, como estruturas condicionais, funções, laços de repetição e manipulação de dados.

print("_________________________")
print("Cadastro de colaboradores")
print("_________________________")

colaboradores = []

while True:
    entrada = input(
        "\n1 - Cadastrar colaborador"
        "\n2 - Listar colaboradores"
        "\n3 - Sair"
        "\nSelecione uma opção: "
    )

    if entrada == "1":
        while True:
            nome = input("Digite o nome do colaborador: ")
            colaboradores.append(nome)

            print("\nColaborador cadastrado com sucesso!")

            resposta = input(
                "Deseja cadastrar outro colaborador? (s/n): "
            ).lower()

            if resposta != "s":
                break

    elif entrada == "2":
        if colaboradores:
            print("\nListando colaboradores...")

            for nome in colaboradores:
                print("Nome:", nome)
        else:
            print("Nenhum colaborador cadastrado!")

    elif entrada == "3":
        print("Saindo do programa...")
        break

    else:
        print("Opção inválida. Tente novamente!")
