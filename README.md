from Division import division
from Multiplicacion import multi
from Modulo import modulo
from Potencia import potencia
from Resta import resta
from Suma import suma

def game():
  score = 0
  while True:
    print('======== Menu ========'
         '\n1. Suma'
         '\n2. Resta'
         '\n3. Multiplicación'
         '\n4. División'
         '\n5. Potencia'
         '\n6. Módulo'
         '\n0. Exit')
    option = int(input('\nElige una opción: '))
     
    if option == 0:
      break
       
    num_1 = int(input('Ingresa el primer número: '))
    num_2 = int(input('Ingresa el segundo número: '))
    answer = int(input('Ingresa la respuesta: '))
     
    if option == 1:
      result = suma(num_1, num_2)
      if result == answer:
        score += 1
        print('Correcto!!')
      else:
       print('Incorrecto')
        
    if option == 2:
      result = resta(num_1, num_2)
      if result == answer:
        score += 1
        print('Correcto!!')
      else:
       print('Incorrecto')

    if option == 3:
      result = multi(num_1, num_2)
      if result == answer:
        score += 2
        print('Correcto!!')
      else:
       print('Incorrecto')

    if option == 4:
      result = division(num_1, num_2)
      if result == answer:
        score += 2
        print('Correcto!!')
      else:
       print('Incorrecto')

    if option == 5:
      result = potencia(num_1, num_2)
      if result == answer:
        score += 4
        print('Correcto!!')
      else:
       print('Incorrecto')

    if option == 6:
      result = modulo(num_1, num_2)
      if result == answer:
        score += 4
        print('Correcto!!')
      else:
       print('Incorrecto')
        
        
    print(f'======== Game Over ========'
         f'\nTu puntuación es {score}'
         '\nSigue así!')
    
game()
  
  
