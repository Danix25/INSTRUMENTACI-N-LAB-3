# Cálculo ambulatorio del índice pletismográfico quirúrgico (SPI)

Samuel Joel Peña Rojas

Paula Vanessa Vera Caro

Daniel Leonardo López Castillo

# PARTE A

Para el desarrollo de la práctica, se inició con el montaje del circuito mostrado a continuación, cuya función es la adquisición de la señal fotopletismográfica (PPG) mediante el uso de un acoplador óptico TCST110, permitiendo registrar las variaciones del volumen sanguíneo periférico a partir de cambios en la intensidad de la luz reflejada. 

<div align="center">
<img width="517" height="285" alt="image" src="https://github.com/user-attachments/assets/7a67b6c8-be41-4db8-ab40-1b75aa588c9e" />
</div>

Adicionalmente, se realizó la modificación del acoplador óptico TCST110 con el fin de optimizar la captura de la señal, adaptándolo para su funcionamiento como sensor de reflectancia. Esta configuración permite que la emisión y detección de la luz se realicen en la misma superficie, facilitando la medición de las variaciones en la intensidad de la luz reflejada por el tejido, las cuales están directamente relacionadas con los cambios en el volumen sanguíneo periférico.

<div align="center">
<img width="400" height="187" alt="image" src="https://github.com/user-attachments/assets/00de536d-990a-4d36-9fb9-f48f14742b2a" />
</div>

Para verificar el correcto funcionamiento del montaje, se procedió a ubicar el dedo sobre el sensor previamente modificado, con el objetivo de observar en la señal adquirida las variaciones asociadas a los cambios en la intensidad de luz incidente sobre el dispositivo. No obstante, al analizar la gráfica obtenida, no se evidenciaron cambios significativos en la señal al colocar o retirar el dedo del sensor.

Ante esta situación, se realizó una verificación del estado de operación del LED infrarrojo integrado en el sensor, con el fin de descartar posibles errores en el montaje del circuito. Dado que la radiación infrarroja no es visible al ojo humano, se empleó la cámara de un dispositivo móvil para confirmar su emisión. Mediante este procedimiento, se constató que el LED se encontraba encendido, lo que sugiere que el circuito estaba correctamente alimentado y funcional desde el punto de vista de emisión óptica:

<div align="center">
<img width="225" height="257" alt="image" src="https://github.com/user-attachments/assets/938778f6-914a-4ed2-8b96-5ec797344bb3" />
</div>

Con base en lo anterior, se optó por realizar una prueba adicional consistente en acercar una fuente de iluminación externa al sensor, con el fin de evaluar su respuesta ante variaciones más evidentes en la intensidad luminosa. Para ello, se utilizó una linterna, la cual se acercaba y alejaba del sensor en distintos intervalos de tiempo, permitiendo observar cambios claramente distinguibles en la señal registrada. A partir de esta prueba, se evidenció que el sistema respondía adecuadamente a variaciones significativas de luz; sin embargo, se concluyó que el sensor implementado no presentaba la sensibilidad suficiente para detectar las pequeñas variaciones asociadas al volumen sanguíneo periférico. En consecuencia, la señal fotopletismográfica no pudo ser visualizada de manera adecuada bajo las condiciones del montaje realizado.

<div align="center">
<img width="231" height="146" alt="image" src="https://github.com/user-attachments/assets/23ff2c6b-0ba3-4ea2-ae08-967880b06f82" />
</div>

Debido a lo anterior, se optó por sustituir el sensor de reflectancia modificado por un sensor integrado de concentración de oxígeno y ritmo cardiaco MAX30102, el cual está diseñado específicamente para la adquisición de señales fotopletismográficas con alta sensibilidad y estabilidad. Este dispositivo incorpora emisores de luz (generalmente en el espectro rojo e infrarrojo) y un fotodetector, junto con etapas internas de acondicionamiento y conversión analógica-digital, lo que permite obtener directamente una señal PPG con menor susceptibilidad al ruido y a variaciones externas. Gracias a estas características, el MAX30102 resulta más adecuado para la detección de las pequeñas variaciones en el volumen sanguíneo periférico, facilitando la adquisición de una señal más clara y consistente en comparación con el montaje previamente implementado:

<div align="center">
<img width="600" height="300" alt="image" src="https://github.com/user-attachments/assets/8cdd763b-1f35-487c-9b58-ca236ecbd44c" />
</div>


## Cold Pressor Test (CPT)

El Cold Pressor Test (CPT) constituye una metodología ampliamente utilizada en la investigación biomédica para evaluar, de manera controlada, la reactividad cardiovascular y la respuesta fisiológica asociada a estímulos nociceptivos. Esta prueba consiste en la inmersión de una extremidad, generalmente la mano (o el pie), en agua con hielo a temperaturas comprendidas entre 0 y 4 °C, durante un intervalo de tiempo definido que típicamente oscila entre 1 y 3 minutos. 

<div align="center">
<img width="320" height="238" alt="image" src="https://github.com/user-attachments/assets/5b4369a6-242a-47d6-b0cf-53ae5ee86dc4" />
</div>

El estímulo aplicado corresponde a un agente térmico de carácter nociceptivo sostenido, el cual induce una respuesta fisiológica sistémica. Como consecuencia de este estímulo, se activa el sistema nervioso simpático, generando la liberación de catecolaminas, principalmente noradrenalina. Esta activación desencadena una serie de respuestas fisiológicas, entre las que se incluyen el aumento de la presión arterial debido a la vasoconstricción periférica, el incremento de la frecuencia cardíaca y la disminución de la amplitud de la onda de pulso en regiones periféricas, asociada a la reducción del flujo sanguíneo en dichas zonas.

Para la implementación del procedimiento en la práctica de laboratorio, se estableció un protocolo experimental dividido en tres fases:

1. **Línea base (condición basal):** El voluntario permanece en estado de reposo, manteniendo uno de sus dedos sobre el sensor durante los primeros 40 segundos, con el fin de registrar las condiciones fisiológicas iniciales sin la presencia de estímulos externos.

2. **Fase de estrés (CPT):** Transcurridos los 40 segundos iniciales, el voluntario introduce la mano contraria (aquella que no se encuentra en contacto con el sensor) en un recipiente con agua helada, manteniéndola en esta condición durante un intervalo de 40 segundos, con el propósito de inducir una respuesta nociceptiva controlada.

3. **Fase de recuperación:** Posteriormente, se retira la mano del agua y el voluntario retorna a la condición de reposo, manteniendo el dedo sobre el sensor hasta completar un tiempo total de adquisición de 2 minutos, permitiendo así observar la evolución y retorno de las variables fisiológicas hacia su estado basal.



# PARTE B
# PARTE C
