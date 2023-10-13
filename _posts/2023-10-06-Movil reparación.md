------
# 1. Herramientas
### 1.1. Herramientas de diagnóstico

- Multímetro o tester ()
- Fuente de alimentación ()
- usbTester ()
- Cámara térmica ()
	- Localizador de fallas o Removedor de partículas 
- Microscopio ()
	- Lupa

###  1.2. Herramientas de desarme y armado

- Destornilladores de precisión ()
- Púas plásticas y espátulas de desarme ()
- Plancha separadora o de calor ()
	- Pistola de calor ()
- Ventosa ()

### 1.3. Herramientas para soldadura

- Estación de soldadura ()
	- Cautín o soldador ()
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

### _Diagnóstico de Pin de Carga_

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

# 6. Tipos de pantallas

- IPS  ->  _lcd, tft, ln-cell _
- OLED  ->  _amoled, superamoled_

### 6.1. IPS
- Son pantallas que tienen un LCD(display de cristal liquido) incorporado.
- Pueden generar colores.
	- pero no puede mostrar esos colores por si mismos ya que no emiten luz.
- Tienen backlight (tira de led que retroiluminan la pantalla).
	- Principal característica de IPS, sin esto no se ve imagen.
	- Consume mas corriente.
	- No existe el color negro, sino blue oscuro y el backlight siempre esta consumiendo.

### 6.2. OLED
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

### 6.3. Tipos de repuestos - Recomendaciones 

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

# 7. Micrófonos

### 7.1. Tipos de micrófonos
- Analógicos
- Digitales

#### Analógicos
Son muy escasos, en la actualidad , la inmensa mayoría de los teléfonos incluye micrófonos digitales.

#### Diferencias
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

### 7.2. Micrófonos: Medición y revisiones

1. Determinar si tiene 1 o 2 micrófonos.
2. Testeamos de que tenga dos tierras(Continuidad - 4 contactos).
	1. Cuando falla una de las tierras puede que no funcione o que funcione con mucho ruido.
3. En uno de los contactos sin continuidad controlamos el voltage.
	1. _Encendemos_ el móvil y hacer uso del micrófono(ej: llamada, grabando, ...)
		1. Solo ahí el PMIC entregara alimentación al micrófono,casi siempre el V es 1.8V.
4. Verificar que no nos falten componentes cerca,(no las de fabrica con soldadura perfecta)
5. Cambiamos el micrófono.
6. Si aun no funciona, revisar los contactos '+ y datos',cada 1  debe tener continuidad con alguna bobina...
	1. Colocamos el micrófono, cable rojo a tierra y el negro a los componentes con los que tenia continuidad.
		1. En escala de diodo deben mostrar valor, en los dos contactos de ese componente(bobina...)

```
Buscar en google: 
modelo mic way
imagenes
```
# 8. ¿Sin señal o sin SIM?

```	
No es lo mismo que el movil no detecte la SIM
	a que te reconozca pero no levante señal.
```

### 8.1. Líneas del portasim

Lo normal es tener 6 contactos; en caso de tener 8, los últimos de cada fila no se usan.

|Nª |Funct     |Nª |Funct|
|---|----------|---|---|
|1  |_VCC (1.8V)_|5  |_GND (tierra)_      |
|2  |_RST_       |6  |VPP (V de Program)|
|3  |_CLK_       |7  |_I/O (in/out)_      |
|4  |          |8  |                  |

###### Lineas RST,CLK,I/O estas tienen comunicación con la CPU.

#### PortaSim con Sistema de bandeja

Tienen un sistema de identificación que detecta cuando se coloca o extrae la sim.
Posee dos contactos que funcionan como un resorte que al momento de extraer la bandeja,
ambos contactos se unen y al colocar la bandeja empuja un contacto cortando dicha union.

### 8.2. PortaSim: Diagnostico

- verificamos que los contactos estén es buen estado.
- En escala de continuidad buscamos el contacto a tierra(el de lado es positivo).
	- Una punta a tierra(chapa) y medimos cada contacto.
	- Verificamos que los demás contactos no tengan continuidad.
- Escala de diodos, punta roja a tierra y medimos con la otra.
	- Deben de mostrar valor a excepción del VPP (1).
- Escala de voltage, punta negra a tierra, roja en VCC.
	- Al encender el equipo debe mostrar un voltage(entre 1.8V y 3V).

_Si estas comprobraciones son correctos y aun así no detecta la SIM, cambiar el lector no lo solucionará._

```
	Buscar en Google
	modelo SIM ways
```


### 8.3. Circuitos de señal: revisión

La zona de radio frecuencia esta compuesta por muchos componentes en una zona,
muchos chip IC (con soldadura por fuera- ~~no por debajo~~).

- Los switch de antena(circulares) deben tener continuidad(entre entrada y salida).

##### Transceiver o WTR
Los demás IC(_amplificadores de potencia 2G,3G,..._) tienen soldaduras por fuera,en cambio el transceiver tiene soldadura bga(por debajo).

Solucionar este tipo de problemas es complejo, para una reparación inicial es recomendable:
  - Si el equipo se quedó sin señal luego de un golpe, se recomienda volver a soldar el WTR.

_Hay amplificadores de potencia que vienen directo de la batería o linea principal, si ponemos en corto esa linea podemos dejar el móvil apagado._

# 9. Soldadura y Malla desoldante

### 9.1. Soldadura

- estaño de pasta
- flux

```
Mezclar flux con estaño, asi tenemos un estaño diluido y mas facil de aplicar 
```

### 9.2. Malla desoldante

```
Solo usamos la punta de la malla, una vez usado lo cortamos
```


### 9.3. Extracción de componentes

capacitores, resistencias, bobinas, diodos.... ~~I C~~

- Aplicamos flux sobre el componente
- Temperatura alrededor de 400 (varia)
- Cogemos con la pinza el componente
	- Levantamos unos milímetros la placa
- Aplicamos el calor en circular (sin frenar) desde el diagonal
	- Posicionar al lado donde el calor afecte menos a otros componentes

#### Uso de malla desoldante

- Siempre se usa solo la punta de la malla
	- Para evitar daños evitar usar lejos de la punta
- Aplicamos un poco de flux a donde limpiar
- Apoyamos el soldador de costado
	- Quien guía a la malla es el soldador
- Limpiamos la placa con removedor de flux

### 9.3.1. Colocación de componentes

- Coloca  _estaño en pasta_ semi liquido en los contactos
	- No importa si el estaño puesto une los contactos
		- Aplicándole aire caliente necesario, el estaño de dividirá en los contactos
 - Colocamos el componente mas ó menos correcto si no es perfecto
	- Al aplicar aire caliente dicho componente se acomodara solo

- Calienta el contactos y derrite el _estaño en alambre_ (entre el contacto y el soldador)

- Coloca _estaño en alambre_ en la punta del soldador
	- Aplica un poco de flux sobre los contactos

### 9.4. Pin de carga: _extracción_

#### Tradicional

- Aplica flux en los contactos del pin de carga
- Aplica estaño en alambre sobre los contactos
- Tira aire caliente en circular (dirige el flujo de aire hacia afuera)
	- _No tironear el pin_

#### Otro

- Aplica flux en el pin de carga
- Apoya el soldador en el pin de carga
	- Mientras aplicamos estaño en alambre
	- Hasta remover el pin de carga

#### _Limpieza_

#### Tradicional

- Aplica un poco de flux en los contactos
- Apoya la malla desoldante en el contacto
	- Y sobre la malla el soldador apoyando de costado
- Ir moviendo con el soldador la malla, al final limpia con removedor de flux 

#### Otro

- Colocamos la placa con el pin de carga sobre el vació
- Aplica un poco de flux en los contactos
- Activamos el succionador de estaño
	- Lo colocamos justo por debajo del agujero del contacto a limpiar
- Colocamos un poco de estaño a la punta del soldador
- Apoyamos el soldador de contado en el contacto
	- Una vez se derrite el estaño activamos el succionador


### 9.5. Botón de encendido: _extracción_

- Aplica estaño en pasta sobre los contactos
- Con el soldador unimos el estaño viejo con el aplicado
- Aplicamos flux
- Tomamos el botón con las pinzas
	- Levantamos unos milímetros
- Aplicamos aire caliente hacia afuera
_si se va a reutilizar el botón, limpiarlo con flux_

##### _Limpieza_

- Colocamos estaño nuevo sobre los contactos
- Pon la malla desoldante sobre los contactos
	- Y sobre esta el soldador (de costado) y movemos
	- No importa si queda un poco de estaño en los agujeros del contacto

##### _Colocación_

- Aplica flux en los agujeros del contacto
- Colocamos el botón con sus dos contactos(pines) en el agujero
	- El flux nos ayuda a mantenerlo en ese lugar
	- _Volteamos la placa_
- Sobre el otro lado colocamos flux el los agujeros del contacto
- Aplica un poco de estaño en el soldador
- Derretimos el estaño sobre el contacto
	- Luego volvemos a la parte superior de la placa
1. Aplicamos _estaño en pasta_ sobre los contactos restantes
	- Aplicamos el soldador sobre ella
	- El contacto del centro es solo para el buen agarre del botón

### 9.6. Micrófonos: _extracción_

- Si se aplica flux, aplicar muy poca
	- _Si el flux ingresa dentro del micrófono puede dañarlo_
- Sostenemos el micrófono con la pinza desde la base
	- _No sostener solo de encima ya que puede salir solo la carcasa del micrófono_
	- Una vez sacado esperar a que se enfríe el estaño que une la carcasa con su base
- Aplicamos aire caliente en circular

##### _Colocación_

- _Primero limpiamos los contactos con estaño viejo_
- Aplica flux en los contactos (Placa o la del micrófono)
1. Colocamos estaño en pasta sobre los contactos (aplicar soldador)
2. Aplicar estaño en alambre en el soldador luego sobre los contactos
- Aplicar un poco de flux sobre los contactos en la placa
- Colocamos el micrófono en su misma posición inicial 
- Aplicamos aire caliente en circular
_No rociar productos de limpieza directamente sobre el micrófono_
_Hay micrófonos sensibles al alcohol_
_Aplicar aire caliente a la zona del micrófono, no directamente al mismo_
- Puede usarse opcional un hisopo para limpiarlo

### 9.7. Desarme de pantallas OLED

```
Calentar el equipo para facilitar su despegue
entre 5-10min en la plancha a 90ª-95ª
o aplicar calor con metodo alternativo
```

- Dispersamos bencina en todo el marco (facilita aflojar el pegamento)
- Ingresar la espátula entre la pantalla y el marco
- Luego de ingresar la espátula aplicar más bencina y deslizar en todo el marco
	- Si se pone dura(aplicar mas bencina) ,si se enfría(calentar un poco)
	- _Buscar y verificar la posición del flex de esa pantalla para no dañarlo_
	- _Las laminas que cubren las pantallas de repuesto son una excelente herramienta para el proceso de despegue sin dañar el flex_
		- Estas son mas flexibles
	- Una vez descubierto los bordes, sustituye la espátula por la lámina
		- Terminamos el proceso de despegue aplicando bencina para facilitar

### 9.7.1. Desarme de pantallas IPS

```
Calentar el equipo entre 5-10 min en la pancha a 90ª-95ª
o aplicar calor con metodo altenativo
```

_El aplicar químicos que faciliten el despegue puede provocar manchas en la pantalla_

- Mantener encendida la pantalla si el teléfono aun muestra imagen
	- Esto nos ayuda cuando ingresemos la espátula
		- Al ingresar mal la espátula(entre los papeles) se verá por la pantalla
- Humedecer la espátula con muy poca bencina(que no gotee)
- Luego de soltar los bordes, reemplazamos la espátula con la lámina

### 9.8. Pegado de pantallas

- Remover el pegamento viejo con bencina
	- El marco tiene que estar limpio
- Antes de pegar la pantalla, probar que este en funcionamiento.
- Aplicar pegamento en ambos marcos(base y pantalla)
	- Dejar secar entre 3 y 5min
- Una vez unido, colocar pinzas durante le secado
	- Dejar el equipo secar como mínimo 30min, lo ideal 1h

### 9.8.1. Desarme de tapas traseras

- Colocar el equipo en la plancha a 95ª durante 5min
- Ingresamos la espátula entre la tapa y el marco
	- Siempre con ayuda de bencina para aflojar el pegamento
	- Nunca trabajar en frío, puede dañarse la tapa

### 9.8.2. Baño químico

##### Batea de ultrasonido

```
Limpia un telefono mojado,
llega a los lugares que manualmente no podemos llegar,
evita que se sulfate
```

- Seleccionamos 50 wats y el tiempo 10min
- Vibra y calienta el químico que se le coloca

###### Químicos
- Alcohol isopropílico
- Agua destilada
- WD-40 (_recomendado_)

###### Proceso
- Cubrimos los orificios del micrófono
	- Con Silicona o con el pegamento de pantallas
- Colocamos la placa en la batea
- Agrega el químico hasta cubrir completamente el equipo
- Lo dejamos 5min a 6min aprox
	- Cumplido el tiempo pausar la batea
- Voltea la placa y dejamos 5min a 6min aprox

























