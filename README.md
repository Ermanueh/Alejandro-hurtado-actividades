# Hurtado actividad
--contador de palabras
#Este ejercicio cuanta la cantidad de palabras en una oración 
#y te dice cuantas empiezan por una determinada letra

#Pide un string
oracion = input("Ingrese una oración: ")
#Separa el string en una lista de strings
palabras = oracion.split()
#Calcula cuantos elementos tiene la lista
cantidad_palabras = len(palabras)
#Pide una letra
letra = input("Ingrese una letra: ")
while len(letra) != 1:
    letra = input("Input no valido, ingrese una letra: ")
cantidad_letras = 0
letra = letra.upper()
#En el bucle busca que palabras empiezan por la letra
for i in palabras:
    if i[0].upper() == letra:
        cantidad_letras += 1
#Muestra por pantalla la solución
print(f"La oración tiene {cantidad_palabras} palabras, de las cuales {cantidad_letras} empiezan por {letra}")
--tabla de multiplicar
numero = int(input("Ingrese un número para mostrar su tabla de multiplicar: "))
for i in range(1, 11):
    resultado = numero * i
    print(f"{numero} x {i} = {resultado}")
    -- verificar si un numero es primo
    numero = int(input("Ingrese un número: "))
es_primo = True
if numero <= 1:
    es_primo = False
else:
    for i in range(2, int(numero**0.5) + 1):
        if numero % i == 0:
            es_primo = False
            break
if es_primo:
    print(f"{numero} es un número primo.")
else:
    print(f"{numero} no es un número primo.")
    --calculadora de interes compuesto
    #Calcula el interés en funcion de la cantidad inicial y el tiempo

#Pide la cantidad inicial y pasa el string a float
principal = float(input("Ingrese la cantidad principal: "))
#Pide la tasa de interes y pasa el string a float
tasa_interes = float(input("Ingrese la tasa de interés (porcentaje): "))
#Pide el tiempo y pasa el string a int
tiempo = int(input("Ingrese el tiempo en años: "))

tasa_interes /= 100  #Convertir la tasa de interés a decimal
monto_final = principal * (1 + tasa_interes) ** tiempo #Calcula el monto final
#Muestra por pantalla el monto final con dos decimales
print(f"El monto final es: {monto_final:.2f}")# calculadora
