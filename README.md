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

Debido a lo anterior, se optó por sustituir el sensor de reflectancia modificado por un sensor integrado de concentración de oxígeno y ritmo cardiaco MAX30102, el cual está diseñado específicamente para la adquisición de señales fotopletismográficas con alta sensibilidad y estabilidad. Este dispositivo incorpora emisores de luz (generalmente en el espectro rojo e infrarrojo) y un fotodetector, junto con etapas internas de acondicionamiento y conversión analógica-digital, lo que permite obtener directamente una señal PPG con menor susceptibilidad al ruido y a variaciones externas. Gracias a estas características, el MAX30102 resulta más adecuado para la detección de las pequeñas variaciones en el volumen sanguíneo periférico, facilitando la adquisición de una señal más clara y consistente en comparación con el montaje previamente implementado:

<div align="center">
<img width="231" height="146" alt="image" src="https://github.com/user-attachments/assets/23ff2c6b-0ba3-4ea2-ae08-967880b06f82" />
</div>

## Cold Pressor Test (CPT)


# PARTE B
# PARTE C
