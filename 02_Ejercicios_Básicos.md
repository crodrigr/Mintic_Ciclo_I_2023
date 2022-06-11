# Ejercicios Básicos 


## Programas simples

# 1. Saludo

![image](https://user-images.githubusercontent.com/31961588/163828082-08d94056-7373-4cc9-bf23-a374f3e8e01d.png)

**Solución 1**

# 2. Circulo

![image](https://user-images.githubusercontent.com/31961588/163828347-f0f3f021-0456-43f8-b481-1d818a87be08.png)

**Solución 2**

# 3. Promedio

![image](https://user-images.githubusercontent.com/31961588/163828427-6376a283-0445-4b3b-bd5c-f26c4c82ee72.png)

**Solución 3**

# 4. Conversión de unidades de longitud
![image](https://user-images.githubusercontent.com/31961588/163828482-cdd2dd38-e805-4418-9db9-f3a3fd2ce958.png)

**Solución 4**

# 5. Número invertido
![image](https://user-images.githubusercontent.com/31961588/163828564-7e54ea4c-73a9-4ef7-aca9-21f1dd124d93.png)

**Solución 5**

# 6. Pitágoras

![image](https://user-images.githubusercontent.com/31961588/163829448-e7ae3e2f-cf13-4058-88b8-6cdedbe19911.png)


**Solución 6**


# 7. Hora futura

![image](https://user-images.githubusercontent.com/31961588/163829518-a0a27ed0-1f63-45e6-9b76-d6e08d0cc001.png)


**Solución 7**

# 8. Parte decimal

![image](https://user-images.githubusercontent.com/31961588/163829563-509bc535-d528-47c7-a804-8725acb7a995.png)


**Solución 8**

# 9. Qué nota necesito

![image](https://user-images.githubusercontent.com/31961588/163829601-a7c25604-3947-4c9a-91a5-0ede2b01a018.png)


**Solución 9**
 
# 10. Año bisiesto

![image](https://user-images.githubusercontent.com/31961588/171307000-a088f237-f470-4fd5-adb6-d077a17695c5.png)

# 11 Califiación cualitativa

```Python

print("PROGRAMA DE CALIFCACIÓN CUALITATVIA")

nombre=input("Nombre: ")
calificacion=int(input("Calificación: "))


#0-59 D,60-79 C,80-89 B, 90-100 A
if(calificacion>=0 and calificacion<=100) :  
       if(calificacion<=59) :
        cualitativa="D"
       elif (calificacion>=60 and calificacion<=79) :
            cualitativa="C"
       elif (calificacion>=80 and calificacion<=89) :
            cualitativa="B"
       else :
            cualitativa="A"
else :
  cualitativa="No definida"



print("Nombre: ")
print("Califación cuantitativa: ",calificacion)
print("Califiación culitativa: ",cualitativa)

```

# 12. Servicio de agua - usuarios

```Python
print("PROGRAMA QUE CALCULA EL VALOR DEL SERVICIO DE AGUA PAR N USUARIOS")

usario=int(input("Numero de usarios: "))

TARIFACONSUMO=200

totalRecaudado=0

for i in range(usario) :

    codigo=input("Ingrese el código: ")
    nombre=input("Ingrese el nombre: ")
    estado=input("Ingrese el estado: V o S: ")
    estrato=int(input("Ingrese el estrato: "))
    cosumo=int(input("Comsumo del mes: "))
    tarifaBasica=0

    if(estado=="V") :
        if(estrato==1):
           tarifaBasica=10000
        elif(estrato==2):
           tarifaBasica=20000
        elif(estrato==3):
           tarifaBasica=30000
        elif(estrato==4) :
           tarifaBasica=45000
        elif(estrato==5) :
           tarifaBasica=60000
        else:
            tarifaBasica=70000
    valorConsumo=cosumo*TARIFACONSUMO
    total=tarifaBasica+valorConsumo

    totalRecaudado=totalRecaudado+total

    print("Nombre: ",nombre)
    print("Tarifa básica: ",'{:,.2f}'.format(tarifaBasica))
    print("Valor comsumo: ",'{:,.2f}'.format(valorConsumo))    
    print("Total: ",'{:,.2f}'.format(total))

print("Total recaudado: ",'{:,.2f}'.format(totalRecaudado))

```
# 13 Calculo de salario de docentes

```Python
print("PROGRAMA DE CALCULO DE SALARIO DE DOCENTES")

print("Número de docentes")
numeroDocentes=int(input())
totalSalarioDocentes=0
totalCtA=0
totalCtB=0
totalCtC=0


for i in range(numeroDocentes) :

      numeroIdentidad=input("Ingrese el número de documento: ")
      nombre=input("Ingrese el nombre: ")
      categoria=input("Ingrese al categoria(A,B,C): ")
      horas=int(input("Ingrese las horas trabajas: "))
      valorCategoria=0

      if(categoria=='A') :
           valorCategoria=25000
           totalCtA=totalCtA+1
      elif(categoria=='B'):
           valorCategoria=35000
           totalCtB=totalCtB+1
      else :
           valorCategoria=50000
           totalCtC=totalCtC+1


      valorTotalSalarioDocente=valorCategoria*horas
      totalSalarioDocentes=totalSalarioDocentes+valorTotalSalarioDocente

      print("Nombre: ",nombre)
      print("Valor a pagar: ",'{:,.2f}'.format(valorTotalSalarioDocente))

print("Valor total a pagar para todos los docentes: ",'{:,.2f}'.format(totalSalarioDocentes))
print("Total categoria A: ",totalCtA)
print("Total categoria B: ",totalCtB)
print("Total categoria C: ",totalCtC)
```
# 14 Tiempo de Viaje

![image](https://user-images.githubusercontent.com/31961588/172032683-1274fc42-8f00-4ae6-912d-ce4c33fa6d49.png)

```Python
print("PROGRAMA DE TIMPO DE VIAJE")

tramo=int(input("Ingrese el tramo: "))

totalMinTramos=0

while (tramo!=0) :
   totalMinTramos=totalMinTramos+tramo
   tramo=int(input("Ingrese el tramo: "))

print("El tiempo total del viaje en minutos ", totalMinTramos)
print("El tiempo total del viaje en horas ", totalMinTramos//60, ":",totalMinTramos%60)
```

# 15 Secuencia de Collatz

![image](https://user-images.githubusercontent.com/31961588/172032804-3de1ddff-4d2e-439d-95b1-9d5a8912e49b.png)

![image](https://user-images.githubusercontent.com/31961588/172032809-a65fb331-b378-459f-91e1-97c2551a7ff6.png)

```Python
print("PROGRAMA DE SERIE DE COLLATZ")


numero=int(input("Ingrese el número: \n"))
print(numero)
while(numero!=1) :
    if(numero%2==0) :
        numero=numero/2
    else :
        numero=numero*3+1
    print('{:,.0f}'.format(numero))
```

# 16 Tablas de multplicar - (ciclos anidados)

```Python

print("PROGRAMA TABLA GENER LAS TABLAS DE MULTIPLIACIÓN DEL UNO AL DIEZ")


#numero=int(input("Ingrese el número de la de multpliación: ")

   
for i in range(1,11) :
    print("TABLA DE MULTIPLICAR DEL ",i,"\n")
    for j in range(1,11) :
       print(i,"*",j,"=",i*j)
    print("\n") 
```

# 17 Tarifa basica de electricidad con validaciones

![image](https://user-images.githubusercontent.com/31961588/172966462-45a6971a-a826-4bc6-8d58-7571ce780f0a.png)

```Python
print("PROGRAMA QUE CALCULA LA TARIFA ELECTRICA CON VALIDACIÓN DE DATOS: ")

tarifaBasica=0

while True :
    try :
        estrato=int(input("Ingresar estrato (1,2,3,4,5): "))
        if(estrato<1 or estrato>5) :
            print("El estrato debe ser 1,2,3,4,5 ")
            continue
        #calculo la tarifa basica
        
        if(estrato==1) :
           tarifaBasica=10000  
        elif (estrato==2) :
           tarifaBasica=15000
        elif (estrato==3) :
           tarifaBasica=30000 
        elif (estrato==4) :
           tarifaBasica=50000 
        else :
           tarifaBasica=65000
        print("Tarifa basica es: ",'{:,.2f}'.format(tarifaBasica))
          
        break
    except ValueError:
        print("El dato ingresado debe ser númerico ")
print("Fin del proceso...")
```
# 18 Sevicio de teléfono con funciones. 

![image](https://user-images.githubusercontent.com/31961588/173166705-e4fe0f77-955d-4e82-816e-427096763865.png)

**Libreria funciones**
```Python
def getDatoNumericoValidado(leyenda) :
    while (True) :
      try:
        numero=int(input(leyenda))
        break         
      except ValueError :
        print("Ops' el dato que ingreso no es númerico. ")
    return numero

def getDatoNumericoEntreRango(leyenda,limiteInferior,limiteSuperior) :
    while True :
      try :
        estrato=int(input(leyenda))
        if(estrato<limiteInferior or estrato>limiteSuperior) :
            print("El valor debe estar entre, ",limiteInferior, "  y ",limiteSuperior)
            continue  
        break
      except ValueError:
        print("El dato ingresado debe ser númerico ")

```
**ServicioTelefono.py**

```Python
import funciones

VALOR_IMPULSO=100
#Funciones 
def getTarifa(estrato) :
    if(estrato==1):
        tarifaBasica=10000
    elif (estrato==2):
        tarifaBasica=15000
    elif (estrato==3):
        tarifaBasica=20000
    elif (estrato==4) :
        tarifaBasica=25000
    else :
        tarifaBasica=30000
    return tarifaBasica
#FinFunciones

n=funciones.getDatoNumericoValidado("Ingrese el número de abonados")
totalPagoAbonados=0

for i in range(n) :
    nombre=input("Ingrese el nombre: ")
    estrato=funciones.getDatoNumericoEntreRango("Ingrese por favor el estrato (1,2,3,4,5): ",1,5)
    impulsos=funciones.getDatoNumericoValidado("Ingrese los impulsos: ")
    tarifaBasica=getTarifa(estrato)
    valorPagarAbononado=(impulsos*VALOR_IMPULSO)+tarifaBasica
    totalPagoAbonados=totalPagoAbonados+valorPagarAbononado
    print("Nombre: ",nombre," valor a pagar: ",valorPagarAbononado)

print("Total a pagar de todos los abonados: ",totalPagoAbonados)

```
