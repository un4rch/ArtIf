estim:
4 10-30 verde
10 10-30 rojo
2 30-60 rojo
12 30-60 verde
5 >60 rojo
9 >60 rojo

>60: 100% rojo
10-30 50% rojo 50% verde
30-60 50% rojo 50% verde
0-10 ???? -> 50% cada

#a)
-((1/2)*log(1/2, 2)+(1/2)*log(1/2, 2))
#b)
-((4/6)*log(4/6, 2)+(2/6)*log(2/6, 2))
#c)
-((1)*log(1, 2))
#d)
-((1/3)*log(1/3, 3)+(1/3)*log(1/3, 3)+(1/3)*log(1/3, 3))
#e)
-((10/12)*log(10/12, 3)+(1/12)*log(1/12, 3)+(1/12)*log(1/12, 3))
#f)
-((1)*log(1, 2))

Ejercicio aliados/enemigos
entropía de cabeza:
triang: 2 aliados 1 enemigo
circ: 2 aliados 2 enemigos
cuadrado: 0 aliados 1 enemigo

.-----------.
|al al en en|
|al al en en|
.-----------.
P(al) = 4/8
P(en) = 4/8
4/8 = 1/2

H(aliado, enemigo) = -((1/2)*log(1/2, 2)+(1/2)*log(1/2, 2))

EH = estimación de la entropía.

## utilizando cabeza:

### si triangulo:
prob de triangulo: (3/8)
.--------.
|al al en|
.--------.
EH(aliado, enemigo) = -((2/3)*log(2/3, 2)+(1/3)*log(1/3, 2)) = 0.92
### si circulo:
prob de circulo: (4/8)
.-----------.
|al al en en|
.-----------.
EH(aliado, enemigo) =-((2/4)*log(2/4, 2)+(2/4)*log(2/4, 2)) = 1
### si cuadrado:
prob de cuadrado: (1/8)
.--.
|en|
.--.
EH(aliado, enemigo) = -((1/1)*log(1/1, 2)) = 0

EH = 3/8 * 0.92 + 4/8 * 1 + 1/8 * 0 = 0.845

IG(cabeza) = 1.0 - 0.845 = 0.155

## utilizando tronco:

### si triangulo:
prob de triangulo: (2/8)
.-----.
|al al|
.-----.
EH(aliado, enemigo) = -((2/2)*log(2/2, 2)) = 0.0
### si circulo:
prob de circulo: (3/8)
.--------.
|al al en|
.--------.
EH(aliado, enemigo) = -((2/3)*log(2/3, 2)+(1/3)*log(1/3, 2)) = 0.92
### si cuadrado:
prob de cuadrado: (3/8)
.--------.
|en en en|
.--------.
EH(aliado, enemigo) = -((3/3)*log(3/3, 2)) = 0.0

EH = 2/8 * 0 + 3/8 * 0.92 + 3/8 * 0 = 0.345

IG(tronco) = 1.0 - 0.345 = 0.655

## utilizando sonrisa:

### si si:
prob de si: (4/8)
.-----------.
|al al al en|
.-----------.
EH(aliado, enemigo) = -((3/4)*log(3/4, 2)+(1/4)*log(1/4, 2)) = 0.811
### si no:
prob de no: (4/8)
.-----------.
|al en en en|
.-----------.
EH(aliado, enemigo) = -((1/4)*log(1/4, 2)+(3/4)*log(3/4, 2)) = 0.811

EH = 4/8 * 0.811 + 4/8 * 0.811 = 0.811

IG(sonrisa) = 1.0 - 0.811 = 0.19

## utilizando cuello:

### si A:
EH(aliado, enemigo) = 
### si B:
EH(aliado, enemigo) = 
### si C:
EH(aliado, enemigo) = 

IG(cuello) =

## utilizando objeto:

### si A:
EH(aliado, enemigo) = 
### si B:
EH(aliado, enemigo) = 
### si C:
EH(aliado, enemigo) = 
### si D:
EH(aliado, enemigo) = 

IG(objeto) =

# Ronda 2
Max(IG) = IG(tronco)

.-----------.
|al al en en|
|al al en en|
.-----------.

triangulo   circulo          cuadrado
.-----.    .--------.       .--------.
|al al|    |al al en|       |en en en|
.-----.    .--------.       .--------.
  FIN    Hace falta seguir     FIN

Gini(cabeza=triangulo): 1 - ((2/3)**2 + (1/3)**2) = 0.444
Gini(cabeza=circulo): 1 - ((2/4)**2 + (2/4)**2) = 0.5
Gini(cabeza=cuadrado): 1 - ((0/1)**2 + (1/1)**2) = 0

Gini(tronco=triangulo): 1 - ((2/2)**2 + (0/2)**2) = 0
Gini(tronco=circulo): 1 - ((2/3)**2 + (1/3)**2) = 0.444
Gini(tronco=cuadrado): 1 - ((0/3)**2 + (3/3)**2) = 0

Gini(cabeza) = 3/8 * 0.444 + 4/8 * 0.5 + 1/8 * 0 = 0.4165
Gini(tronco) = 2/8 * 0.0 + 3/8 * 0.444 + 3/8 * 0 = 0.1665