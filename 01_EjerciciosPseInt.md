# Ejercicios en PSeInt 

### 1. Ejercicio de calculo de salario de un ejempleado cuando trabaja más de 40 horas

```Psc
Algoritmo  SalarioEmpleado
	definir horasTrabajadas,horasAdicionales Como Entero
	definir precioHora, salario, precioHoraAdicional,salarioAdicional, totalSalario Como Real
	definir nombre Como Caracter
	
	Escribir "Por favor ingrese el nombre"
	leer nombre
	Escribir "Por favor ingresar las horas trabajadas: "
	leer horasTrabajadas
	Escribir "Por favor ingresar el precio de la hora: "
	leer precioHora
	
	
	Si horasTrabajadas<=40 Entonces
		salario=horasTrabajadas*precioHora
	SiNo
		horasAdicionales=horasTrabajadas-40
		precioHoraAdicional=1.5*precioHora
		salarioAdicional=horasAdicionales*precioHoraAdicional
		salario=(horasTrabajadas*precioHora)
		totalSalario=salario+salarioAdicional
	Fin Si
	
	Escribir "Nombre: ",nombre
	
	Si horasTrabajadas<=40 Entonces		
		Escribir "Salario: ",salario		
	SiNo		
		Escribir "Horas adicionales: ",horasAdicionales
		Escribir "Precio hora adicional: ",precioHoraAdicional
		Escribir "Salario adicional: ",salarioAdicional
		Escribir "Salario: ",salario
		Escribir "Total salario: ", totalSalario
		
	Fin Si
	
	
	
FinAlgoritmo

```

### 2. Ejercicio dado tres numeros a, b y c cual es el mayor. Tener encuenta si los número son iguales

```Psc
Algoritmo mayor 
	Escribir "Ingrese el valor de a: "
	Leer a
	Escribir "Ingrese el valor de b: "
	Leer b
	Escribir "Ingrese el valor de c: "
	Leer c
	Escribir "Valores de a: ",a," b: ",b," c: ", c
	
	ningunoMayor=0
	mayorAB=0
	mayorBC=0
	mayorAC=0

	Si a=b y b=c y a=c Entonces
		Escribir " a, b, c son iguales"
		ningunoMayor=1
	SiNo
	    Si a=b Entonces
			Escribir "a y b son iguales "
			mayorAB=1
		SiNo
			Si b=c Entonces
				Escribir "b y c son iguales "
				mayorBC=1
			SiNo
				Si a=c Entonces
					Escribir "a y c son iguales "
					mayorAC=1
				SiNo
					Escribir "Ningún número es igual a los otros "
				Fin Si
			Fin Si
		Fin Si
	Fin Si
	
	
	
	si ningunoMayor<>1 Entonces
		
	
	Si a>b Entonces
		Si a>c Entonces
			
			Si mayorBC=1 Entonces		
				Escribir "b o c son mayores 1 "
				
			SiNo
				Escribir "a es el mayor "
			Fin Si		
			
		SiNo			
			Si mayorAC=1 Entonces
				Escribir "a o c son mayores "
					
			SiNo				
				Escribir "b es el mayor "			
			Fin Si		
		Fin Si
	SiNo
		Si b>c Entonces
			
			Si mayorAB=1 Entonces				
				Escribir "a o b son mayores "
			SiNo
				Escribir "b es el mayor "
			Fin Si		
		SiNo
			
			Si mayorBC=1 Entonces				
				Escribir "b o c son mayores 2 "
			SiNo
				Escribir "c es el mayor "
			Fin Si
			
				
			
		Fin Si
		
	Fin Si
SiNo
	 Escribir "Ningun numero es mayor"
FinSi
	
FinAlgoritmo

```
### 3. Año bisiesto

```Psc
Algoritmo año_bisiesto
	Escribir "Ingrese el año"
	Leer año
	Si año mod 100 == 0 Entonces
		Si año mod 400==0 Entonces
			
			Escribir "El año ", año, " Es bisiesto"
		SiNo
			Escribir "El año ", año, " No es bisiesto"
		Fin Si
	SiNo
	
		Si año mod 4==0 Entonces
			Escribir "El año ", año, " Es bisiesto"
		SiNo
			Escribir "El año ", año, " No es bisiesto"
		Fin Si
	Fin Si
FinAlgoritmo

```
