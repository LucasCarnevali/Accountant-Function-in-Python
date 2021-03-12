# Accountant-Function-in-Python

from time import sleep

def contador(inicio, fim, passo):
    if passo < 0:
        passo *= -1
    if passo == 0:
        passo = 1
    print('-' * 20)
    print(f'Contagem de {inicio} até {fim} de {passo} em {passo}')
    sleep(1)

    if inicio < fim:
        contador = inicio
        while contador <= fim:
            print(f'{contador} ', end='', flush=True)
            sleep(0.5)
            contador += passo
        print('FIM')
    else:
        contador = inicio
        while contador >= fim:
            print(f'{contador} ', end='', flush=True)
            sleep(0.5)
            contador -= passo
        print('FIM!')

contador(1, 10, 1)
contador(10, 0, 2)
print('-' * 20)
print('Agora é a sua vez de personalizar a contagem!')
inicio = int(input('Inicio: '))
fim = int(input('Fim:    '))
passo = int(input('Passo:  '))
contador(inicio, fim, passo)
