# Ejercicios Básicos 


## Programas simples

# 0. Libreria de funciones

**funciones57.py**

```Python
def getDatoEnteroValidado(leyenda) :
    while (True) :
     try:
        numero=int(input(leyenda))
        break         
     except ValueError :
        print("Ops' el dato que ingreso no es númerico. ")
    return numero

def getDatoEnteroEntreRango(leyenda,limInf,limSup) :
    while True :
      try :
        estrato=int(input(leyenda))
        if(estrato<limInf or estrato>limSup) :
            print("El valor debe estar entre,",limInf," y ",limSup)
            continue  
        break
      except ValueError:
         print("El dato ingresado debe ser númerico ")
        
def getDatoDecimalValidado(leyenda) :
    while (True) :
     try:
        numero=float(input(leyenda))
        break         
     except ValueError :
        print("Ops' el dato que ingreso no es númerico y contener punto decimal. ")
    return numero


def imprimirMatriz(matriz):
    for i in range(len(matriz)) :
        for j in range(len(matriz[i])) :
          print(matriz[i][j])
        print("\n")

def ordenmiento(lista,tipo) :
    if(tipo=='desc') :
        for i in range(len(lista)) :
         for j in range(i+1,len(lista)) :         
                if (lista[i]<lista[j]) :
                    temp=lista[i]
                    lista[i]=lista[j]
                    lista[j]=temp
            
    elif(tipo=='asc') :
      for i in range(len(lista)) :
        for j in range(i+1,len(lista)) :
              if (lista[i]>lista[j]) :
                 temp=lista[i]
                 lista[i]=lista[j]
                 lista[j]=temp             
    return lista

def buscar(lista,valor) :    
    for i in range(len(lista)) :
       if(lista[i]==valor) :
          return i
    return -1
```

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
# 18 Servicio de teléfono con funciones. 

![image](https://user-images.githubusercontent.com/31961588/173166705-e4fe0f77-955d-4e82-816e-427096763865.png)

**funciones.py**
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

# 19 Lista de nombres con su tamaño

![image](https://user-images.githubusercontent.com/31961588/173210026-9f46b524-168f-4a8c-a0e4-4da1f3b64c1f.png)

```Python

print("PROGRMA DE LISTA DE NOMBRES Y SU TAMAÑO")

nombre=input("Ingresar nombre: ")

listaNombres=[]
listaNumeroCaracteres=[]
listaNombres.append(nombre)
listaNumeroCaracteres.append(len(nombre))

while (nombre!="FIN"):
     nombre=input("Ingresar nombre: ")
     listaNombres.append(nombre)
     listaNumeroCaracteres.append(len(nombre))


for i in range(len(listaNombres)) :
    print("Nombre: ",listaNombres[i], "tamaño: ",listaNumeroCaracteres[i])


```

# 20 Mayores que promedio usando listas

![image](https://user-images.githubusercontent.com/31961588/173965756-bd06178b-6f5e-4fad-be9d-48a6ff9d6887.png)

**Mayores**
```Python
from funciones57 import * 

#Variables Globales
datos=[]

#Funciones

def llenado(tamaño):
    for i in range(tamaño) :
        datos.append(getDatoDecimalValidado("Ingrese dato: "))

def imprimir():
    for i in range(len(datos)):
        print("Dato: ",datos[i])

def getPromedio():
    suma=0
    for i in range(len(datos)):
        suma=suma+datos[i]
    promedio=suma/len(datos)
    return promedio

def getMayorPro(prom):
    totalMayores=0
    for i in range(len(datos)):
        if(datos[i]>prom) :
            totalMayores=totalMayores+1        
    return totalMayores

#Incio Programa

n=getDatoEnteroValidado("Ingrese la cantidad de veces que se van a solicitar datos: ")
llenado(n)
pro=getPromedio()
total=getMayorPro(pro)
print("Promedio: ",pro)
print("Total de valors mayores del promedio es: ",total)
imprimir()

```
**funciones57.py**
```Python
def getDatoEnteroValidado(leyenda) :
    while (True) :
     try:
        numero=int(input(leyenda))
        break         
     except ValueError :
        print("Ops' el dato que ingreso no es númerico. ")
    return numero

def getDatoEnteroEntreRango(leyenda,limInf,limSup) :
    while True :
      try :
        estrato=int(input(leyenda))
        if(estrato<limInf or estrato>limSup) :
            print("El valor debe estar entre,",limInf," y ",limSup)
            continue  
        break
      except ValueError:
         print("El dato ingresado debe ser númerico ")
        
def getDatoDecimalValidado(leyenda) :
    while (True) :
     try:
        numero=float(input(leyenda))
        break         
     except ValueError :
        print("Ops' el dato que ingreso no es númerico y contener punto decimal. ")
    return numero


```

# 21 Promedio de calificaciones usando matrices.
```Python

#Funciones

def llenadoCalifiaciones():
    calificaciones=[]
    estu=int(input("Numbero estudiantes: "))
    calf=int(input("Numero de califiaciones: "))
    for i in range(estu) :        
        print("Califiaciones del estudiante: ",i)
        calificaciones.append([])
        for j in range(calf):
           calificaciones[i].append(int(input("ingrese la calificaciones:")))                 
    return calificaciones


def calcularNotaFinal(m):
    notasFinales=[]
    for i in range(len(m)) :
        sumaNotas=0
        for j in range(len(m[i])):
            sumaNotas=sumaNotas+m[i][j]
        notasFinales.append(sumaNotas/len(m[i]))
    return notasFinales

def aprobadosReprobados(n) :
    aprobados=0
    reprobados=0
    for i in range(len(n)) :
        print("Estudiantes: ",i,":",n[i])
        if(n[i]>=3):
            aprobados=aprobados+1
        else:
            reprobados=reprobados+1
    print("Aprobados: ",aprobados)
    print("Reprobados: ",reprobados)
        



#Inicio de programa
calificaciones=llenadoCalifiaciones()
#calificaciones=[[3,4,5,1,4],[1,3,5,1,2],[4,4,1,5,1],[3,4,1,5,1],[3,4,3,2,3],[2,3,4,2,3],[2,5,2,1,4]]
listaNotasFinales=calcularNotaFinal(calificaciones)
aprobadosReprobados(listaNotasFinales)




```

# 22 Supermercado con diccionarios.

![image](https://user-images.githubusercontent.com/31961588/174415294-dd483751-5042-4e8b-b2bf-4667330d9723.png)

```Python
from funciones57 import * 

#Funciones
articulos={1:"Lapiz",2:"Cuadernos",3:"Borrador",4:"Calculadore",5:"Escuadra"}
precios={1:2500,2:3800,3:1200,4:35000,5:3700}


#Incio de Programa

numerArticulos=getDatoEnteroValidado("Ingrese el número de articulos: ")

sumaTotal=0
for i in range(numerArticulos) :
    codigo=getDatoEnteroValidado("Ingrese código (1 a 5) del articulo: ")
    cantidad=getDatoEnteroValidado("Ingrese la cantidad: ")
    valorItem=precios[codigo]*cantidad
    sumaTotal=sumaTotal+valorItem
    print("Articulo: ",articulos[codigo]," valor unitario: ",precios[codigo]," cantidad: ",cantidad," valor Item:",valorItem)

print("Total: ",sumaTotal)
```
# 23 Notas de certamen

![image](https://user-images.githubusercontent.com/31961588/174418911-d7491680-aa66-4d40-9c0c-1656ab794000.png)

![image](https://user-images.githubusercontent.com/31961588/174418919-d725e180-341d-4979-9b14-f3ac7811a26b.png)

![image](https://user-images.githubusercontent.com/31961588/174418945-cfdabdfa-54fc-461b-86f9-1558c6f8e875.png)

```Python
from funciones57 import * 

#Variables Globales
listEstudiantes=[]

#Funciones

def loadData() :
    estu1={'id':'0001','nombre':"Camilo",'c1':45,'c2':98,'c3':89,'nf':0}
    estu2={'id':'0002','nombre':"Juan",'c1':23,'c2':38,'c3':56,'nf':0}
    estu3={'id':'0003','nombre':"Maria",'c1':56,'c2':25,'c3':43,'nf':0}
    estu4={'id':'0004','nombre':"Pedro",'c1':96,'c2':98,'c3':42,'nf':0}
    estu5={'id':'0005','nombre':"Jose",'c1':10,'c2':60,'c3':99,'nf':0}
    listEstudiantes.append(estu1)
    listEstudiantes.append(estu2)
    listEstudiantes.append(estu3)
    listEstudiantes.append(estu4)
    listEstudiantes.append(estu5)

def addEstudiante():
    estudiante={}
    estudiante['id']=input("Ingrese el id")
    estudiante['nombre']=input("Ingrese nombre: ")
    estudiante['c1']=getDatoEnteroValidado("Ingrese c1: ")
    estudiante['c2']=getDatoEnteroValidado("Ingrese c2: ")
    estudiante['c3']=getDatoEnteroValidado("Ingrese c3: ")
    estudiante['nf']=0
    listEstudiantes.append(estudiante)

def calcularNotafinaEstudiante():    
    for i in range(len(listEstudiantes)) :     
      suma=listEstudiantes[i].get('c1')+listEstudiantes[i].get('c2')+listEstudiantes[i].get('c3')
      listEstudiantes[i]['nf']=suma/3

def promdioCurso():
    suma=0
    for i in range(len(listEstudiantes)) :     
      suma+=listEstudiantes[i].get('nf')     
    promedio=suma/len(listEstudiantes)
    print("Promedio del curso: ",'{:,.1f}'.format(promedio))

def aprobadosReprobados():
    aprobados=0
    reprobados=0
    for i in range(len(listEstudiantes)) :   
        if(listEstudiantes[i].get('nf')>=55):
            aprobados+=1
        else:
            reprobados+=1
    print("Aprobados: ",aprobados) 
    print("Reprobados: ",reprobados)

def buscar(idBuscar) :
    for i in range(len(listEstudiantes)) :
      if(listEstudiantes[i].get('id')==idBuscar):
        return i
    return -1

def imprimirPorPos(pos) :   
        print("Id: ",listEstudiantes[pos].get('id'),
              "Nombre: ",listEstudiantes[pos].get('nombre'),
              "C1: ",listEstudiantes[pos].get('c1'),
              "C2: ",listEstudiantes[pos].get('c2'),
              "C3: ",listEstudiantes[pos].get('c3'),
              "Nf: ",'{:,.1f}'.format(listEstudiantes[pos].get('nf')))


def imprimir() :
    for i in range(len(listEstudiantes)) :
        print("Id: ",listEstudiantes[i].get('id'),
              "Nombre: ",listEstudiantes[i].get('nombre'),
              "C1: ",listEstudiantes[i].get('c1'),
              "C2: ",listEstudiantes[i].get('c2'),
              "C3: ",listEstudiantes[i].get('c3'),
              "Nf: ",'{:,.1f}'.format(listEstudiantes[i].get('nf')))

def menu() :
    print("_________________MENU____________________")
    print("1.Crear Estudiante ")
    print("2.Calcular la nota final de cada estudiante ")
    print("3.Calcular el promedio del curso")
    print("4.Cuantos aprobados y reprobados")
    print("5.Imprimir listado estudiantes")
    print("6.Buscar ")
    print("7.Salir")
    op=getDatoEnteroValidado("Ingresar opción: ")
    return op

#Inicia Programa
loadData()
op=1
while (op>=1 and op<=6) :
        op=menu()
        if(op==1):
          addEstudiante()
        if(op==2):
          calcularNotafinaEstudiante()
        if(op==3):
          promdioCurso()
        if(op==4):
          aprobadosReprobados()
        if(op==5):
          imprimir()
        if(op==6):
          id=input("Ingrese el id: ")
          pos=buscar(id)
          if(pos!=-1):
            print("Datos del estudiante: ")
            imprimirPorPos(pos)
          else :
            print("No existe ningún estudiante con ese Id !")




```

# 24 Torneo de tennis

![image](https://user-images.githubusercontent.com/31961588/175436135-b2d1f70e-5611-4978-a379-6348e1e2ffc2.png)

![image](https://user-images.githubusercontent.com/31961588/175436166-35dba909-5837-408f-bef7-9d73f90d64f8.png)

```Python
import random
#Declaraciones

tenistas=['Nadal','Melzer','Murray','Soderling','Djokovic','Berdych','Federer','Ferrer','Juan','Pedro','David','Eli','Willy','Jorge','Carlos','Daniel']

#Funciones
def mostrarTenista(n) :
    for i in range(len(n)) :
        print("Jugador: ",i+1,": ",n[i])


def rondas(n) :
    nuevaRonda=[]
    for i in range(0,len(n),2) :
        print("a. ",n[i],"- b.",n[i+1]," : ")
        g=random.randint(1,2)
        if(g==1) :
           print("a")
           nuevaRonda.append(n[i])
        else :
           print("b")
           nuevaRonda.append(n[i+1])
    return nuevaRonda


# Inicio del programa

mostrarTenista(tenistas)
while len(tenistas)>1 :
    tenistas= rondas(tenistas)
    print(" ")
    mostrarTenista(tenistas)
    print(" ")


```


# 25 Listas ordenadas

![image](https://user-images.githubusercontent.com/31961588/175436536-f6473122-2d23-44ba-81c6-2295c9ea4e74.png)

![image](https://user-images.githubusercontent.com/31961588/175436568-045a9b7a-df85-4818-9a42-1f60bbbbc7e2.png)

```Python
from funciones57 import *

a=[13,12,11,1,9,7,4,2,3,5,14]  
b=[2,1,6,7,9,16,10,14,3,4,13]
c=[]

print("Lista a")
print(a)
print("Lista b")
print(b)

a=ordenmiento(a,'asc')
b=ordenmiento(b,'asc')

#merge
for i in range(len(a)) :
    if(a[i]==b[i]) :
       c.append(a[i])   
    else :
        c.append(b[i])
        c.append(a[i])

#Ordenar lista
c=ordenmiento(c,'asc')

#Elminar repetidos
c1=[]
for i in range(len(c)) :
   sw=0
   for j in range(i+1,len(c)) :
       if(c[i]==c[j]) :
         sw=1
   if(sw==0) :
    c1.append(c[i])

#Resultado final  
print("Lista a")
print(a)
print("Lista b")
print(b)
print("Lista c")
print(c1)
```

# 26 Busqueda binaria recursiva

```Python
from funciones57 import*

listaNumeros=[4,5,8,9,10,40,30,50,49]

#Funciones
def busqueda_binaria(lista,elemento,izq,der):
    if izq>der:
        return -1
    med=(izq+der)//2
    if lista[med]==elemento :
        return med
    elif lista[med]>elemento:
        return busqueda_binaria(lista,elemento,izq,med-1)
    else :
        return busqueda_binaria(lista,elemento,med+1,der)


#Inicio de Programa
print(listaNumeros)
listaNumeros=ordenmiento(listaNumeros,'asc')
print(listaNumeros)
izq=0
der=len(listaNumeros)-1
numero=int(input("Ingrese número a buscar: "))
pos=busqueda_binaria(listaNumeros,numero,izq,der)
if(pos!=-1) :
 print("Elemento encontrador en :", pos)
else :
 print("Elemnto no encontrado")


```
# 27 Certanmenes con archivos

```Python
from operator import concat
from funciones57 import *
from io import open

#Variables Globales
listEstudiantes=[]


#Funciones

def guardarArchivo() :
    archivo=open("estudiantes.txt","w")
    datos=""
    for i in range(len(listEstudiantes)) :
        datos+=listEstudiantes[i].get('id')+","
        datos+=listEstudiantes[i].get('nombre')+","
        datos+=str(listEstudiantes[i].get('c1'))+","
        datos+=str(listEstudiantes[i].get('c2'))+","
        datos+=str(listEstudiantes[i].get('c3'))+","
        datos+=str(listEstudiantes[i].get('nf'))
        datos+="\n"

    archivo.write(datos) 
    print("Guardado...")

def loadData() :   
    archivo=open("estudiantes.txt","r")   
    linea=archivo.readline()
    while linea :
          estu={}
          datos=linea.split(',')         
          estu['id']=datos[0]
          estu['nombre']=datos[1]
          estu['c1']=int(datos[2])
          estu['c2']=int(datos[3])
          estu['c3']=int(datos[4])
          estu['nf']=float(datos[5])
          listEstudiantes.append(estu)
          linea = archivo.readline()

    archivo.close()

    

    



def addEstudiante():
    estudiante={}
    estudiante['id']=input("Ingrese el id")
    estudiante['nombre']=input("Ingrese nombre: ")
    estudiante['c1']=getDatoEnteroValidado("Ingrese c1: ")
    estudiante['c2']=getDatoEnteroValidado("Ingrese c2: ")
    estudiante['c3']=getDatoEnteroValidado("Ingrese c3: ")
    estudiante['nf']=0
    listEstudiantes.append(estudiante)

def calcularNotafinaEstudiante():    
    for i in range(len(listEstudiantes)) :     
      suma=listEstudiantes[i].get('c1')+listEstudiantes[i].get('c2')+listEstudiantes[i].get('c3')
      listEstudiantes[i]['nf']=suma/3

def promdioCurso():
    suma=0
    for i in range(len(listEstudiantes)) :     
      suma+=listEstudiantes[i].get('nf')     
    promedio=suma/len(listEstudiantes)
    print("Promedio del curso: ",'{:,.1f}'.format(promedio))

def aprobadosReprobados():
    aprobados=0
    reprobados=0
    for i in range(len(listEstudiantes)) :   
        if(listEstudiantes[i].get('nf')>=55):
            aprobados+=1
        else:
            reprobados+=1
    print("Aprobados: ",aprobados) 
    print("Reprobados: ",reprobados)

def buscar(idBuscar) :
    posiciones=[]
    for i in range(len(listEstudiantes)) :
      if(listEstudiantes[i].get('id')==idBuscar):
        posiciones.append(i)
    return posiciones


def imprimirPorPos(pos) :   
        print("Id: ",listEstudiantes[pos].get('id'),
              "Nombre: ",listEstudiantes[pos].get('nombre'),
              "C1: ",listEstudiantes[pos].get('c1'),
              "C2: ",listEstudiantes[pos].get('c2'),
              "C3: ",listEstudiantes[pos].get('c3'),
              "Nf: ",'{:,.1f}'.format(listEstudiantes[pos].get('nf')))


def imprimir() :
    for i in range(len(listEstudiantes)) :
        print("Id: ",listEstudiantes[i].get('id'),
              "Nombre: ",listEstudiantes[i].get('nombre'),
              "C1: ",listEstudiantes[i].get('c1'),
              "C2: ",listEstudiantes[i].get('c2'),
              "C3: ",listEstudiantes[i].get('c3'),
              "Nf: ",listEstudiantes[i].get('nf'))


def particion(lista) :
    pivote=lista[0].get('id')
    menores=[]
    mayores=[]
    for i in range(1,len(lista),1) :
       if lista[i].get('id')<pivote:
          menores.append(lista[i])
          print("menores")
          print(menores)
       else :
          mayores.append(lista[i])
    return menores,pivote,mayores

def quicksort(lista) :
   if len(lista)<2 :
      return lista
   else :
     menores,pivote,mayores=particion(lista)
     return quicksort(menores)+[pivote]+quicksort(mayores)



def menu() :
    print("_________________MENU____________________")
    print("1.Crear Estudiante ")
    print("2.Calcular la nota final de cada estudiante ")
    print("3.Calcular el promedio del curso")
    print("4.Cuantos aprobados y reprobados")
    print("5.Imprimir listado estudiantes")
    print("6.Buscar ")
    print("7.Ordenar asc")
    print("8.Guardar")
    print("9.Salir")
    op=getDatoEnteroValidado("Ingresar opción: ")
    return op

#Inicia Programa
loadData()
op=1
while (op>=1 and op<=8) :
        op=menu()
        if(op==1):
          addEstudiante()
        if(op==2):
          calcularNotafinaEstudiante()
        if(op==3):
          promdioCurso()
        if(op==4):
          aprobadosReprobados()
        if(op==5):
          imprimir()
        if(op==6):
          id=input("Ingrese el id: ")
          pos=buscar(id)
          if(pos!=-1):
            print("Datos del estudiante: ")
            imprimirPorPos(pos)
          else :
            print("No existe ningún estudiante con ese Id !")
        if(op==7) :
          print(listEstudiantes)
          listEstudiantes=quicksort(listEstudiantes)
          print(listEstudiantes)
        if(op==8) :
          guardarArchivo()








```
