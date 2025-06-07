
Algoritmo ProyectoCalculadora

	Definir Opcion, Realizar_Otra_Transaccion Como Entero
	Definir PrimerNumero, SegundoNumero Como Real
	Definir TamaMatriz, A, B Como Entero
	Definir Matriz1, Matriz2, resultado_De_Matriz, Total_Suma_De_Ambas_Matrices, Total_Resta_De_Ambas_Matrices Como Entero
	Dimension Matriz1[100,100], Matriz2[100,100], resultado_De_Matriz[100,100]
	Definir Total_Suma_Matriz, Total_Resta_Matriz Como Entero
	Definir Numero_Triangulo_Filas, Fila_Triangulo, Columna_Triangulo, Numero_Triangulo_Actual Como Entero
	Definir Numero_Rectangulo, Fila_Rectangulo, Columna_Rectangulo Como Entero
	Definir D Como Entero
	Definir Seleccion_numeros Como Real
	Dimension Seleccion_numeros[100]
	Definir Cantidad_De_Numeros_Ingresados Como Entero
	Definir Numero_Ingresado, Suma_Estadistica, Numero_Mayor, Numero_Menor, Promedio Como Real
	Definir Resultado_Sobre_Promedio, Resultado_Debajo_Promedio Como Entero
	
	
	Repetir 
		
		Escribir "MENÚ PRINCIPAL"
		Escribir " "
		Escribir "Elija una operación por favor: "
		Escribir " "
		Escribir "1. Suma"
		Escribir "2. Resta"
		Escribir "3. Multiplicación"
		Escribir "4. División"
		Escribir "5. Sumar todos los valores de Matriz"
		Escribir "6. Restar todos los valores de Matriz"
		Escribir "7. Suma de Matrices"
		Escribir "8. Resta de Matrices"
		Escribir "9. Triángulo con Numeros"
		Escribir "10. Rectángulo con Asteriscos"
		Escribir "11. Estadísticas en una lista de Numeros"
		Escribir "0. Deseo salir de la Aplicación"
		Escribir Sin Saltar "Elija una opción para continuar: "
		Leer Opcion
		
		
		Segun Opcion Hacer
			
			1:
				Repetir
					Escribir " SUMA"
					Escribir " Ingrese el Primer Numero:"
					Leer PrimerNumero
					Escribir " Ingrese el Segundo Numero:"
					Leer SegundoNumero
					Escribir "El total de la suma es: ", PrimerNumero + SegundoNumero
					Escribir ""
					Escribir "¿Desea realizar otra Suma? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			2:
				Repetir
					Escribir "RESTA"
					Escribir "Ingrese el Primer Numero: "
					Leer PrimerNumero
					Escribir "Ingrese el Segundo Numero: "
					Leer SegundoNumero
					Escribir "El residuo de la resta es: ", PrimerNumero - SegundoNumero
					Escribir ""
					Escribir "¿Desea realizar otra Resta? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			3:
				Repetir
					Escribir " MULTIPLICACIÓN"
					Escribir "Ingrese el Primer Numero: "
					Leer PrimerNumero
					Escribir "ingrese el Segundo Numero"
					Leer SegundoNumero
					Escribir " El resultado de la Multiplicación es:", PrimerNumero * SegundoNumero
					Escribir ""
					Escribir "¿Desea realizar otra Multiplicación? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			4:
				Repetir
					Escribir " DIVISIÓN "
					Escribir "Ingrese el Primer Numero: "
					Leer PrimerNumero
					Escribir "Ingrese el Segundo Numero: "
					Leer SegundoNumero
					Escribir " El resultado de la División es: ", PrimerNumero / SegundoNumero
					Escribir ""
					Escribir "¿Desea realizar otra División? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			5:
				Repetir
					Escribir " Sumar Todos Los Valores De La Matriz"
					Escribir " Ingrese el Tamaño de la Matriz"
					Leer TamaMatriz
					
					Si TamaMatriz > 0 Y TamaMatriz <= 100 Entonces
						Total_Suma_Matriz = 0
						Escribir "Ingrese los valores para llenar la Matriz: "
						Para A = 1 Hasta TamaMatriz Hacer 
							Para B = 1 Hasta TamaMatriz Hacer 
								Escribir Sin Saltar "Matriz[", A, ",", B, "]: "
								Leer Matriz1[A, B]
								Total_Suma_Matriz = Total_Suma_Matriz + Matriz1[A,B]
							FinPara
						FinPara
						Escribir " La Matriz que ingresaste es:"
						Para A = 1 Hasta TamaMatriz Hacer 
							Para B = 1 Hasta TamaMatriz Hacer 
								Escribir Sin Saltar Matriz1[A,B], "   "
							FinPara
							Escribir " "
						FinPara
						Escribir " El resultado de la suma de todos los valores de la Matriz es: ", Total_Suma_Matriz
						
					FinSi
					Escribir ""
					Escribir "Desea realizar otra transacción en Suma de Matriz? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			6:
				Repetir
					Escribir " Restar Todos Los Valores De La Matriz"
					Escribir " Ingrese el Tamaño de la Matriz"
					Leer TamaMatriz
					
					Si TamaMatriz > 0 Y TamaMatriz <= 100 Entonces
						Escribir " Ingrese los valores para llenar la Matriz: "
						Escribir Sin Saltar "Matriz[1,1]: "
						Leer Matriz1[1,1]
						Total_Resta_Matriz = Matriz1[1,1]
						
						
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								
								Si NO (A = 1 Y B = 1) Entonces
									Escribir Sin Saltar "Matriz[", A, ",", B, "]: "
									Leer Matriz1[A, B]
									Total_Resta_Matriz = Total_Resta_Matriz - Matriz1[A,B]
								FinSi
							FinPara
						FinPara
						
						Escribir " La Matriz que ingresaste es:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								Escribir Sin Saltar Matriz1[A,B], "   "
							FinPara
							Escribir " "
						FinPara
						Escribir " El resultado de la resta de todos los valores de la Matriz es: ", Total_Resta_Matriz
						
					FinSi
					Escribir ""
					Escribir "Desea realizar otra transacción en Resta de Matriz? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			7:
				Repetir
					Escribir "SUMA DE MATRICES "
					Escribir Sin Saltar "Ingrese el tamaño de las matrices (N x M, por ejemplo 3 para 3x3): "
					Leer TamaMatriz
					
					Si TamaMatriz > 0 Y TamaMatriz <= 100 Entonces
						Total_Suma_De_Ambas_Matrices = 0
						Escribir "Ingrese los valores para la MATRIZ 1:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								Escribir Sin Saltar "Matriz1[", A, ",", B, "]: "
								Leer Matriz1[A,B]
							FinPara
						FinPara
						
						Escribir "Ingrese los valores para la MATRIZ 2:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								Escribir Sin Saltar "Matriz2[", A, ",", B, "]: "
								Leer Matriz2[A,B]
							FinPara
						FinPara
						
						Escribir "El resultado de la suma de las matrices es:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								resultado_De_Matriz[A,B] = Matriz1[A,B] + Matriz2[A,B]
								Escribir Sin Saltar resultado_De_Matriz[A,B], "   "
								Total_Suma_De_Ambas_Matrices = Total_Suma_De_Ambas_Matrices + resultado_De_Matriz[A,B]
							FinPara
							Escribir ""
							
						FinPara
						Escribir " Este es el resultado total de la suma de ambas Matrices: ", Total_Suma_De_Ambas_Matrices
					FinSi
					Escribir ""
					Escribir "¿Desea realizar otra  Suma de Matrices? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			8:
				Repetir
					Escribir "RESTA DE MATRICES "
					Escribir Sin Saltar "Ingrese el tamaño de las matrices (N x M, por ejemplo 2 para 2X2): "
					Leer TamaMatriz
					
					Si TamaMatriz > 0 Y TamaMatriz <= 100 Entonces
						Total_Resta_De_Ambas_Matrices = 0
						Escribir "Ingrese los valores para la MATRIZ 1:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								Escribir Sin Saltar "Matriz1[", A, ",", B, "]: "
								Leer Matriz1[A,B]
							FinPara
						FinPara
						
						Escribir "Ingrese los valores para la MATRIZ 2:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								Escribir Sin Saltar "Matriz2[", A, ",", B, "]: "
								Leer Matriz2[A,B]
							FinPara
						FinPara
						
						Escribir "El resultado de la resta de las matrices es:"
						Para A = 1 Hasta TamaMatriz Hacer
							Para B = 1 Hasta TamaMatriz Hacer
								resultado_De_Matriz[A,B] = Matriz1[A,B] - Matriz2[A,B]
								Escribir Sin Saltar resultado_De_Matriz[A,B], "   "
								Total_Resta_De_Ambas_Matrices = Total_Resta_De_Ambas_Matrices - resultado_De_Matriz[A,B]
							FinPara
							Escribir ""
							
						FinPara
						Escribir " Este es el resultado  de la resta de ambas Matrices: ", Total_Resta_De_Ambas_Matrices
					FinSi
					Escribir ""
					Escribir "¿Desea realizar otra Resta de Matrices? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
			9:
				Repetir
					Escribir "TRIÁNGULO CON NÚMEROS"
					Escribir " "
					Escribir "Ingrese un número entero para definir el tamaño del triángulo (número de filas): "
					Leer Numero_Triangulo_Filas
					
					Si Numero_Triangulo_Filas > 0 Entonces
						Para Fila_Triangulo = 0 Hasta Numero_Triangulo_Filas - 1 Hacer
							Numero_Triangulo_Actual = (2 * Fila_Triangulo) + 1
							Para Columna_Triangulo = 0 Hasta Fila_Triangulo Hacer 
								Escribir Sin Saltar Numero_Triangulo_Actual, " "
								Numero_Triangulo_Actual = Numero_Triangulo_Actual - 2
							FinPara
							Escribir ""
						FinPara
						
					FinSi
					Escribir ""
					Escribir "¿Desea realizar otro Triángulo de Números? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			10:
				Repetir
					Escribir "RECTANGULO CON ASTERISCOS *"
					Escribir Sin Saltar "  Ingrese un número para el tamaño del cuadrado: "
					Leer Numero_Rectangulo
					
					Si Numero_Rectangulo > 0 Entonces
						Para Fila_Rectangulo = 1 Hasta Numero_Rectangulo Hacer
							Para Columna_Rectangulo = 1 Hasta Numero_Rectangulo Hacer
								Si Fila_Rectangulo = 1 O Fila_Rectangulo = Numero_Rectangulo O Columna_Rectangulo = 1 O Columna_Rectangulo = Numero_Rectangulo Entonces
									Escribir Sin Saltar "* "
								Sino
									Escribir Sin Saltar "  "
								FinSi
							FinPara
							Escribir "" 
						FinPara
					Sino
						Escribir "ERROR: El tamaño debe ser un número positivo."
					FinSi
					Escribir ""
					Escribir "  Desea realizar otra transacción en Rectángulo de Asteriscos? (1=Si, 0=No): "
					Leer Realizar_Otra_Transaccion
				Hasta Que Realizar_Otra_Transaccion = 0
				
				
			11:
				Repetir 
					Escribir " ESTADÍSTICAS DE NÚMEROS "
					Escribir "  Ingrese un Máximo de 100 números. Ingrese -1 para terminar la entrada."
					
					Cantidad_De_Numeros_Ingresados = 0
					Suma_Estadistica = 0
					
					Numero_Mayor = 0
					Numero_Menor = 0
					
					
					Repetir
						Escribir Sin Saltar "  Ingrese un número: "
						Leer Numero_Ingresado
						
						
						Si Numero_Ingresado <> -1 Entonces
							
							Si Cantidad_De_Numeros_Ingresados < 100 Entonces
								
								Si Cantidad_De_Numeros_Ingresados = 0 Entonces
									Numero_Mayor = Numero_Ingresado
									Numero_Menor = Numero_Ingresado
								FinSi
								
								
								Seleccion_numeros[Cantidad_De_Numeros_Ingresados] = Numero_Ingresado
								
								Suma_Estadistica = Suma_Estadistica + Numero_Ingresado
								
								
								Si Numero_Ingresado > Numero_Mayor Entonces
									Numero_Mayor = Numero_Ingresado
								FinSi
								
								Si Numero_Ingresado < Numero_Menor Entonces
									Numero_Menor = Numero_Ingresado
								FinSi
								
								
								Cantidad_De_Numeros_Ingresados = Cantidad_De_Numeros_Ingresados + 1
							Sino 
								Escribir "AVISO: Se ha alcanzado el límite máximo de 100 números. Finalizando entrada."
								Numero_Ingresado = -1 
							FinSi
						FinSi
					Hasta Que Numero_Ingresado = -1 
					
					
					Si Cantidad_De_Numeros_Ingresados > 0 Entonces
						Promedio = Suma_Estadistica / Cantidad_De_Numeros_Ingresados
						
						Resultado_Sobre_Promedio = 0
						Resultado_Debajo_Promedio = 0
					FinSi
					
						
						Para D = 0 Hasta Cantidad_De_Numeros_Ingresados - 1 Hacer 
							Si Seleccion_numeros[D] > Promedio Entonces
								Resultado_Sobre_Promedio = Resultado_Sobre_Promedio + 1
							Sino Si Seleccion_numeros[D] < Promedio Entonces
									Resultado_Debajo_Promedio = Resultado_Debajo_Promedio + 1
								FinSi
							
							
							
							Escribir "    RESULTADOS DE LAS ESTADÍSTICAS    "
							Escribir "Cantidad de números ingresados: ", Cantidad_De_Numeros_Ingresados
							Escribir "Suma total: ", Suma_Estadistica
							Escribir "Promedio: ", Promedio
							Escribir "Número Mayor: ", Numero_Mayor
							Escribir "Número Menor: ", Numero_Menor
							Escribir "Números por encima del promedio: ", Resultado_Sobre_Promedio
							Escribir "Números por debajo del promedio: ", Resultado_Debajo_Promedio
						 
							
						FinSi
						Escribir "" 
						
						Escribir "¿Desea realizar otra Estadística de Números? (1=Si, 0=No): "
						Leer Realizar_Otra_Transaccion
					FinPara
					
					Hasta Que Realizar_Otra_Transaccion = 0 
				
				
			0:
				Escribir "¡Gracias por usar la Calculadora! Ha finalizado el proceso"
				
				
			De Otro Modo:
				Escribir "Opcion no valida"
				
		FinSegun 
		
		Escribir "" 
		
		
		Si Opcion <> 0 Entonces
			Esperar Tecla
			Limpiar Pantalla 
		FinSi
		
	Hasta Que Opcion = 0 

FinAlgoritmo
