# joao import os 


def listar_arquivos(diretorio):
    """
    lista os arquivos em um diretório e seus subdiretórios.
    args:
        diretorio (str): caminho do diretório a ser listado.

    """
    for raiz, diretorios, arquivos in os.walk(diretorio):
        print(f"Diretório: {raiz}")
        for arquivo in arquivos:
            print(f"  - {arquivo}")
    print("\nListagem concluída.")
if __name__ == "__main__":
    diretorio = input("Digite o caminho do diretório a ser listado: ")
    if os.path.isdir(diretorio):
        listar_arquivos(diretorio)
    else:
        print("O caminho fornecido não é um diretório válido.")
