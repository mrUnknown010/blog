---
title: Móvil Notas
---
# **1. Herramientas**
### **1.1. Herramientas de diagnóstico**

- _Multímetro o tester ()_
- _Fuente de alimentación ()_
- _usbTester ()_
- _Cámara térmica ()_
	- _Localizador de fallas o Removedor de partículas_
- _Microscopio ()_
	- _Lupa_

###  **1.2. Herramientas de desarme y armado**

- _Destornilladores de precisión ()_
- _Púas plásticas y espátulas de desarme ()_
- _Plancha separadora o de calor ()_
	- _Pistola de calor ()_
- _Ventosa ()_

### 1.3. Herramientas para soldadura

- Estación de soldadura ()
	- Cautin o soldador ()
- Estaño ()
- Flux ()
- Malla desoldante ()
	- Succionador de estaño ()
- Cinta metálica y/o Kapton ()
- Pinzas bruselas
- Holder ()

### 1.4. Herramientas de limpieza

- Batea de ultrasonido ()
	- Alcohol isopropílico ()
	- WD-40 ()
	- Bencina
- Removedor de flux ()
- Cepillo y/o Hisopos

### 1.5. Herramientas de seguridad anti-estática

- Pulsera antiestática ()
	- Guantes antiestáticos ()
- Manta de trabajo antiestática

### 1.6. Herramientas complementarias

- Alicate de precisión ()
- Pegamento para pantallas ()
- Pinzas sujetadoras y/o morsas ()
- Recipientes herméticos y/o táper ()

# 2. Conceptos de electrónica básica

### 2.1. Tensión, Corriente y Resistencia

Tensión o Voltage

	unidad de medida: V (voltio)
	Fuerza que se ejerce sobre los electrones para que se muevan.
	Mayor fuerza mas voltage

	Bateria
	+V +A

corriente

	Cantidad de electrones que estan circulando en un circuito.
	unidad de medida: A (ampere)

resistencia

	Opocision al paso de la corriente o electrones
	unidad de medida: Ω (ohmio)

	+R -A

### 2.2. Corriente Alterna y Corriente Continua

Corriente alterna **AC (~)

	El curso de los electrones cambia de sentido todo el tiempo.
	No tiene polaridad

Corriente continua **DC/CC (-)

	Los electrones siempre van en una misma direccion.
	Tiene polaridad

### 2.3. Multiplicadores y Divisores

|prefijo |Simbolo |Valor |Equivalencia en unidades|
|-------|---------|------|------------------------|
|exa    |E        |1x10(18)|trillón               |
|peta   |P        |1x10(15)|mil billones          |
|tera   |T        |1x10(12)|billón                |
|giga   |G        |1x10(9) |mil millones          |
|mega   |M        |1x10(6) |millón                |
|**kilo**   |k        |1x10(3) |mil                   |
|hecto  |h        |1x10(2) |cien                  |
|deca   |da       |1x10    |diez                  |
|**unidad** |**1**        |**1**       |**uno**                   |
|deci   |d        |1x10(-1)|décima                |
|centi  |c        |1x10(-2)|centésima             |
|**mili**   |m        |1x10(-3)|milésima              |
|       |         |1x10(-6)|millonésima           |
|       |         |1x10(-9)|mil millonésima       |

_Ejemplo:_

	1A = 1 mA (miliAmpere)
	
	0,550 -> 550 mA
	1,25  -> 1250 mA
	
### 2.4. Serie y Paralelo

#### Serie
	Uno al lado del otro

_Ejemplo:_

	Tenemos 3 leds cada uno necesita 2v y consumen 3mA
		-> Voltage necesario para encenderlos: 
			2v+2v+2v = 6V    se suman
			3mA
	Potencia usado 6V*3mA=18

#### Paralelo
	cada conexión es independiente

_Ejemplo:_

	Tenemos 3 leds cada uno necesita 2V y consumen 3mA
		-> voltage necesario para encenderlos:
			2V
			3mA+3mA+3mA = 9mA   se suman
	Potencia usado 2V*9mA=18

##### Mediciones comunes en móviles
- voltages V
- ohmios Ω
- continuidad -
- diodos ->|-

### 2.5. Cortocircuitos

#### Circuito abierto
	Cuando el circuito esta abierto no funciona  Ejp:un cable cortado

#### Circuito cerrado
	Cuando el circuito esta cerrado si funciona

#### Cortocircuito
	Ocurre cuando Positivo y Negativo se unen sin ninguna resistencia en el medio.
	Ocurre una avalancha de electrones en ese punto que producen una disipacion colorica mayor.

### 2.6 Utilización del Tester

	⏚  Cable Negro (COM)
	Ω  Cable Rojo  (mA)

**Uno siempre debe elegir la escala inmediatamente superior a la que quiere medir**

	Medicion de tension en las Baterias.
	cargadas al 100% entregan 4.2V  4.3V
	En el tester elegir la escale superior a ello ej 20V

# 3. Componentes electrónicos

#### Tipos de componentes electrones según su soldadura
##### THT (tecnología de agujeros pasantes)
	Los contactos de los componentes estan soldados pasando la placa

##### SMT o SMD (Tecnología de montaje superficial)
	Tienen contactos para ser soldados de manera superficial sobre la placa

### 3.1. Resistencias R

	Componentes que se oponen al paso de la corriente.
	
	No tienen polaridad
	No continuidad
	En general los smd son de color negro con extremos plateados.

_Medición de resistencia_

- Colocamos la perilla del tester en la parte del simbolo Ω
- Colocamos cada punta en cada extremo del resistor.
- Probar con la escala menor _(si marca 1 o 0 ir subiendo de escala)_
	- si ya llegamos a las escalas de k, multiplicar el valor que nos da por mil

### 3.2. Condensadores C

	Son como pequeñas baterias, capaces de almacenar cierta energia.
	Logra estabilizar la linea ante fluctuaciones. Absorve y/o suelta energia.
	casi todos los capacitores estan conectadas en paralelo.(Contacto en + el otro en -).
	
	No continuidad.
	No tiene polaridad
	En general los capacitores son color Marron(Mas claro o Oscuro) y/o grises.

_Medición de capacitores_
- Colocamos el Tester en escala de Continuidad.
- Colocamos cada punta en cada extremos del capacitor.
	- No debe de haber continuidad (Sonido).
- Otra Forma de medir es colocar cualquier punta a tierra (Chapa).
	- Con la otra punta medimos cada extremo del capacitor.
		- En un extremo debe de haber continuidad(Sonido/Conexión a tierra) y en la otra no.
### 3.3. Bobinas L

	Cable enrollado en un nucleo aislado entre si.
	Capaz de cargarse pero con muy poca energia(electromagnetico).
		-A falta de corriente es capaz de elevar la tension.
		-A excesivo corriente es capaz de bajar la tension.
	Por lo general usados en serie y en linea positivo.
	
	A diferencia de capacitores o resistencia; normalmente son mas grandesitas.
	Si continuidad.

_Medición de inductores_

- Colocar la perilla en - y/o ->I-
- Medir continuidad entre sus puntas.
- luego poner el cable ⏚ en cualquier chapa a tierra.
	- No debe tener continuidad ya que esta en la linea positiva
	- Si se encuentra una bobina en _continuidad a tierra_
		- Posible estar en linea en corto; pero el culpable de ese corto siempre es otro.

### 3.4. Diodos D

	Son semiconductores bajo ciertas condiciones.
		Permite el paso de electrones en una sola direccion y la otra lo bloquea.
	Genera caida de tension al paso de la corriente.
	
	Normalmente tienes sus conectores un poco mas delgadas y tienen una raya en un lado

_Medición de diodos_

- Colocar la perilla en ->I- 
- Medir sus puntas luego invertir los cables hasta que nos muestre un valor.
	- Porque permite el paso de corriente en un sentido.
	- Si marca en ambas mediciones es que esta defectuoso el diodo.
- Ejplo:  el tester nos marca 780 (mili) -> 0.780 -> 0.8 ; si tenemos 5V de corriente nos queda 4.2V.

# 4. Circuito de carga

	1. El inicio del circuito es el pin de carga.
	2. De por medio esta el IC (circuito integrado de carga).
	3. El final es la bateria.

	Universalmente la entrega del cargador es de 5V.
##### Proteccion del IC

	Casi siempre despues del puerto de carga se encuentran capacitores.
	Ademas de diodos.
	O incluso un OVP (protector de sobrevoltage).

	- Estos se encargan de proteger el IC, haciendo que le lleguen los 5V correctos.
	- El IC se encarga de bajar la tension reduciendo a 4.3V que es la maxima carga de una bateria al 100%.
	- El IC tambien se encarga de cortar el paso de energia una vez llegado la 100% o consumido.

### 4.1. Pin de carga

##### Estructura
- tienen 5  o 7 contactos.
	- Si es de 7, los extremos no lo tenemos en cuenta
- Orden 1-2-3-4-5  o  5-4-3-2-1 , depende

##### Función de cada contacto
- 1 (C+) , 5 (C\-)
- 2 (D-) , 3 (D+ o GND)
- 4 (id/n-c)

#### 4.1.1 Diagnostico de Pin de Carga

	Dock test
	(placa con pin de carga con puntos dispersos conectados a cada contacto)

- Colocamos el tester en escala de diodos.
- Colocamos el cable Rojo en tierra (chapa de carga) y medimos con la Negra.
- Tiene que marcar en cada punto un valor, tierra (000 o 001), mas importante los pines de C+ y C-.
	- Si esta dañada el pin de carga nos marca 1 en los puntos.

### 4.2. Medición con USB tester

El USB tester muestra 1ero Voltage, y 2do Ampere (consumo)
Un cargador que tenga un USB de manera estandar da entre 4.9V - 5.2V (USB tester conectado al cargador).

	- Colocamos el USB tester al cargador y el cable del movil al USB tester (movil sin la bateria).
	- El consumo minimo de A es normal ya que el IC comprueba si esta disponible la bateria.
	- Sin la bateria el consumo no debe ser elevado en tal caso podemos estar ante un corto.
###### Gama Baja
	- Consumo de ampere A minimo hasta 150mA = 0.15(USBtester), (Sin bateria)
	- Consumo de A: consumen por debajo de 1A = 0.99(USBtester), (Con bateria)
###### Teléfonos de Mayor Gama
	- Consumo de A: consumen entre 1A hasta 1.5A (Con bateria).

###### Carga turbo
- al conectar el cable turbo, (El cargador y el móvil) tienen un chip y ambos se comunican.
	- Si el móvil acepta carga turbo, el cargador eleva la tensión a 9V (Carga turbo).
- Si usamos un cable de menor calidad, _No se activa la Carga turbo_ (los 9V), aunque el A sea aceptable.
	- Esto afecta la Velocidad de carga.
		- El cargador muestra info Ejplo: 5V 2.0A /  9V 1.67A.   (esto indica lo máximo que entrega el cargador)
		- Si el móvil le pide 0.5A entonces el cargador le entrega los 0,5V necesarios.

### 4.3. Medición de Voltage

#### Tips de búsqueda en Google
	Modelo charging ways
_Ejplo:_
	G532 charging ways

##### Voltages a medir

	 - Entrada pin de carga (conector 1)
	- sector de filtrado y proteccion (bobina,diodo)
	- Entrada al IC (capacitores y/o diodos)
	- Salida del IC (bobina-conector + de bateria)

- Colocamos en la escala de Corriente Continua escala superior a 5V.
- Colocamos una punta en la tierra (chapa pin carga).
- La otra punta en el 1 (C+) del pin de carga. Nos debe dar los 5V
	- Seguido de medir las bobinas , puede haber un diodo protector (PA) inversion de polaridad (Cable al revés).
- Vamos al IC,siempre trabaja con una bobina grande, y suele estar cerca al conector de batería.
	- Generalmente medimos en algún capacitor cerca están los 5V de entrada que alimentan el IC.
	- La salida de carga 4.3 (caida de tension) lo medimos en la Bobina o en conector positivo de la batería.
		- _El valor baja y sube si no esta conectado la batería._

### 4.4. Circuitos Integrados

- IC circuitos integrados, tienen la soldadura BGA (matriz de malla de bolas).
- Lo que se hace para medirlos es buscar componentes del costado y medirlos ya que están conectados al chip.

# 5. Encendido

### 5.1. ¿Que es un PMIC?

	Tambien conocido como IC de Power.
	Es el distribuye o gestiona la energia 

	Es un chip generalmente cuadrado, rodeado de bobinas grandes.
	Siempre tiene un oscilador cerca.
		Oscilador: parecido a un microfono tiene como una chapita por encima.

### 5.2. Ciclo de arranque
	
	La batería alimenta de energía al PMIC, para que esto funcione la batería 
	debe de tener 3.7V (10% aprox), cargada al 100% es de 4.3V aprox

- PMIC
- CPU
- Memoria

1. El PMIC esta conectado directamente por una linea al botón de encendido.
	- El botón de encendido suele tener 2 contactos.
		- Si hay 4 contactos suelen repetirse(dos de cada uno).
	- El segundo contacto del botón suele ir a tierra.
	- Al colocar la batería, en el botón de encendido siempre se encuentra voltage enviado por el PMIC.
		- Ej: si tenemos 4V (Voltage de batería), o en algunos casos 1.8V(depende de cada fabricante).
	- Al presionar el botón de encendido, provocamos un corto controlado(se une positivo con tierra).
		- El voltage que teníamos se vuelve a 0V, y esa condición lo controla el PMIC para encender.
			- Si esta encendido el PMIC lo contrala según el tiempo que se tiene presionado el botón power.
2. El segundo en encenderse es el procesador.
3. El tercero en encenderse es la memoria que tiene las instrucciones para el procesador.

	En algunos móviles el otro contacto del botón power no esta puesta a tierra, vuelve al PMIC y/o subPMIC (dividen funciones con PMIC);
	Entonces si teniamos 4V, por el otro contacto aparece los 4V al presionarlo y esto es controlado por el PMIC y/o subPMIC.

### 5.3. Falla de encendido - Revisiones

1. Medimos el voltage se la batería, debe tener lo mínimo necesario para que el teléfono encienda(3.7V).
2. Medimos continuidad entre los pines + y - del conector de la batería (placa).

#### Medición con fuente de alimentación

- Simulamos ser la batería del móvil.
	Conectamos los cocodrilo al conector de la batería + y -
	El negativo tierra podemos conectarlo en cualquier chapa
- El consumo de A debe ser 0
	- Un móvil no debe consumir batería si está apagado.
	- Presionamos power brevemente (fijarse en el consumo que nos muestra).
		- Un consumo de 300mA indica cortocircuito en una etapa posterior al arranque.
- Encendemos el móvil.
	- Durante el encendido el consumo es por debajo de 1A por lo general.
		- En teléfonos de alta gama puede ser mayor consumo.
	- Esperamos a que el móvil entre en modo reposo (1 o 2 min).
		- El consumo debe ser de 20mA hasta 30mA.

	Es muy común que al tener un problema con un móvil al que le dura poco la batería,
	se le haga cambio de batería, y que luego el tiempo de duración incluso sea peor.
	_Quizá nunca la batería era el problema, sino un cortocircuito en alguna parte._
	_Quizá el móvil nunca entro en modo reposo y por ende sigue consumiendo energia._

### 5.4. Botón de encendido

- Revisamos continuidad entre sus 2 contactos del botón power (Presionando el Botón).
- Verificamos que le llegue voltage a una de los contactos del power (el otro lo ponemos en chapa).
	- Según su configuración si precionamos el power:
		- nos mantiene el voltage(Pasa el V al otro contacto) o desaparece (Corto con tierra).
	- Si no hay voltage en ninguno de los contactos, puede ser un problema en el PMIC.

### 5.5. PMIC - Mediciones

_Sin alimentar el móvil_
- Ponemos el tester en continuidad
- Revisamos las bobinas, capacitores; cercanos...
	- Las boninas no deben de marcar continuidad.
	- Revisar continuidad los capacitores ...

_Con alimentación_
- Ponemos en escala de voltage.
- Por lo general en un capacitor encontraremos el voltage que entrega la batería al PMIC.
- Mantenemos presionado power, medimos las bobinas 
	- La salida de V por las bobinas la mayoría es para alimentar el procesador
		- Es posible que una de las bobinas de salida no tenga V.
			- Es para alimentar al procesador de llamadas, pero no se habilita mientras no haya un SIM.

### 6. Pantallas - IPS

#### Tipos de pantallas

- IPS  ->  _lcd, tft, ln-cell _
- OLED  ->  _amoled, superamoled_

#### IPS
- Son pantallas que tienen un LCD(display de cristal liquido) incorporado.
- Pueden generar colores.
	- pero no puede mostrar esos colores por si mismos ya que no emiten luz.
- Tienen backlight (tira de led que retroiluminan la pantalla).
	- Principal característica de IPS, sin esto no se ve imagen.
	- Consume mas corriente.
	- No existe el color negro, sino blue oscuro y el backlight siempre esta consumiendo.

#### OLED
- Son pantallas super finas.
	- Con años de uso suele aparecer la pantalla fantasma.
	- Vida util mas corta.
- No necesitan backlight, cada pixel es un led RGB.
	- Consume menos corriente.
	- Cada vez que se tiene un color negro, se apaga el pixel.

```
Buscar en google caracteristicas de moviles:  
	modelo caracteristicas 
Ingresar en la pagina smart-gsm.com -> https://www.smart-gsm.com/moviles
```

### Tipos de repuestos - Recomendaciones

| calidad  | descripción  |
|----------|--------------|
|Original  |Solo en servicios técnicos oficiales|
|AAAAA (5A)|Calidad Original(Fabricado por terceros)|
|AAAA (4A) |Alta Copia - HC(High Copy)|
|AAA       |Triple A|
|AA        ||
|A         ||

**Los repuestos 100% originales solo se consiguen en servicios técnicos oficiales o extrayendo el componente de otro equipo.**

- Como el reemplazo de las pantallas OLED  es muy costoso, los fabricantes tuvieron una idea: inventaron adaptaciones que permiten sustituir pantallas OLED con una pantalla IPS.
- Se les denominan como: AAA, TFT , Metal, In-cell...

#### Desventajas
- Recuerda que las pantallas IPS son mas gruesas que las OLED, en este tipo de adaptaciones la pantalla queda más expuesta a roturas  por golpes ya que sobresale del marco.
- Al ser mas gruesas, muchas veces la funcionalidad de los botones inferiores queda afectada.
- Notable disminución de la calidad de imagen, ya que pasamos de un display OLED a uno IPS.

### Micrófonos

#### Tipos de micrófonos
- Analógicos
- Digitales

##### Analógicos
Son muy escasos, en la actualidad , la inmensa mayoría de los teléfonos incluye micrófonos digitales.

##### Diferencias
- Un micrófono analógico tiene dos contactos(+y-),  
	- La linea positiva es la encargada de alimentar el micrófono y de transportar los datos hacia el codificador o codec de audio.
- La mayoría es circular.

- Un micrófono digital tiene por lo menos tres contactos(+(1.8V) y -, y linea de datos independiente).
- La mayoría es rectangular.

_Cuando se tiene 4 contactos (alimentación, linea de datos y dos tierras)_
- Debajo de un micrófono digital siempre se encuentra dos contactos sin continuidad a tierra(alimentación y datos).
	Y todos los demás es tierra.

_Si al equipo no le ingresa señal de audio no siempre debemos culpar al micrófono_
_Puede tratarse de una falla del CODEC de audio_

	En la mayoría de los equipos de gama media y baja esta adentro del PMIC.
	Algunos teléfonos tienes dos micrófonos(uno arriba y otro abajo).

### Micrófonos: Medición y revisiones

1. Determinar si tiene 1 o 2 micrófonos.
2. Testeamos de que tenga dos tierras(Continuidad - 4 contactos).
3. En uno de los contactos sin continuidad controlamos el voltage.
	1. Encendemos el móvil y hacer uso del micrófono(ej: llamada, grabando, ...)
		1. Solo ahí el PMIC entregara alimentación al micrófono,casi siempre el V es 1.8V.
4. Verificar que no nos falten componentes cerca,(no las de fabrica con soldadura perfecta)
5. Cambiamos el micrófono.
6. 












