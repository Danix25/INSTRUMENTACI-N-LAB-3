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

## Índice Pletismográfico Quirúrgico (SPI)

El índice pletismográfico quirúrgico (SPI) es una herramienta de monitoreo continuo y no invasivo, diseñada para cuantificar el equilibrio entre la nocicepción (respuesta fisiológica ante un estímulo doloroso) y la analgesia (efecto de los fármacos analgésicos) en pacientes bajo anestesia general.

<div align="center">
<img width="321" height="280" alt="image" src="https://github.com/user-attachments/assets/73a2252b-d554-4006-b7b3-4d3952ac9c2d" />
</div>

Este índice se obtiene a partir de la señal de fotopletismografía (PPG), adquirida mediante un oxímetro de pulso colocado típicamente en el dedo. A través de esta señal, es posible inferir la actividad del sistema nervioso simpático. En presencia de un estímulo nociceptivo, se produce un aumento del tono simpático, lo que conlleva a fenómenos como la vasoconstricción periférica y el incremento de la frecuencia cardíaca.

El SPI toma valores en un rango de 0 a 100, donde el intervalo entre 20 y 50 se considera óptimo para una analgesia adecuada durante el procedimiento quirúrgico. Valores superiores a 50 indican un incremento en el nivel de estrés nociceptivo, lo que sugiere la necesidad de una mayor administración de analgésicos.

<div align="center">
<img width="487" height="387" alt="image" src="https://github.com/user-attachments/assets/fc1fe37a-c29d-494f-ae61-cc28e0f7ea3e" />
</div>




La formula estándar del índice pletismográfico quirurgico es:

$$
**{SPI} = 100 - (0.33 \cdot {HBI} + 0.67 \cdot {PPGA})**
$$

Donde:
- **HBI (Heart Beat Interval):** Corresponde al intervalo de tiempo entre latidos sucesivos. En este contexto, es importante resaltar que, ante la presencia de un estímulo doloroso, se produce un incremento en la frecuencia cardíaca, lo que conlleva a una disminución del HBI.

- **PPGA (Photoplethysmographic Pulse Wave Amplitude):** Representa la amplitud de la onda de pulso y se define como la diferencia entre el valor máximo (sístole) y el mínimo (diástole) de la señal fotopletismográfica. Dado que el estrés induce vasoconstricción periférica, se reduce el flujo sanguíneo hacia las extremidades, lo que se traduce en una disminución de la amplitud de la señal, es decir, del PPGA.

- **Constantes 0.33 y 0.67:** Estos coeficientes corresponden a los pesos asignados al intervalo entre latidos y a la amplitud de la onda de pulso, respectivamente. En la formulación del índice, se otorga mayor ponderación a la PPGA (67 %) en comparación con el HBI (33 %), debido a que la amplitud de la señal constituye un indicador más sensible y de respuesta más rápida frente a cambios en la actividad del sistema nervioso simpático que las variaciones en la frecuencia cardíaca por sí solas.

## Codigo de Adquisión en ESP32

```c++
#include <Wire.h>
#include "MAX30105.h"

MAX30105 sensor;

unsigned long lastSampleTime = 0;
const int sampleInterval = 10;

long maxValue = 0;

void setup() {
  Serial.begin(115200);
  Wire.begin(21, 22);

  if (!sensor.begin(Wire, I2C_SPEED_FAST)) {
    while (1);
  }

  sensor.setup();
  sensor.setPulseAmplitudeRed(0x00);
  sensor.setPulseAmplitudeIR(0x2F);
}

void loop() {
  if (millis() - lastSampleTime >= sampleInterval) {
    lastSampleTime = millis();

    long irValue = sensor.getIR();

    if (irValue > maxValue) {
      maxValue = irValue;
    }

    Serial.println(maxValue - irValue);
  }
}
```


Este código usa el sensor MAX30105 para leer una señal PPG con luz infrarroja y enviarla en tiempo real al computador. Primero configura la comunicación y activa solo el LED infrarrojo, y luego en el loop toma muestras cada 10 ms. En cada lectura obtiene el valor de la señal (irValue) y guarda el valor máximo observado (maxValue). Después calcula maxValue - irValue y eso es lo que envía por el puerto serial. Esto se hace porque el sensor, por su funcionamiento normal, entrega la señal “invertida”: cuando hay un latido hay más sangre, se absorbe más luz y el valor baja, formando valles. Al hacer esa resta, esos valles se convierten en picos hacia arriba.

## Procesamiento en Matlab

```MATLAB
clc; clear; close all 

s = serialport("COM10",115200);
configureTerminator(s,"LF");
flush(s);

N = 300;
bufferV = nan(1,N);
bufferT = nan(1,N);

x = input("Ingrese el tiempo deseado de lectura: ");

tiempo = [];
senal = [];

psi_t = [];
psi_val = [];

num_upsteps = 0;
threshold = 6;
prev_dato = NaN;
prev_t = NaN;

picos_t = [];
picos_v = [];

valles_t = [];
valles_v = [];

ultimo_pico_t = NaN;

valle_actual = Inf;
valle_t = NaN;

ventana_norm = 200;
SPI_prev = NaN;
PPGA_hist = [];

figure(1);
h = plot(bufferT, bufferV, 'b', 'LineWidth', 2); hold on
h_picos = plot(nan, nan, 'ro', 'MarkerFaceColor','r');
h_valles = plot(nan, nan, 'go', 'MarkerFaceColor','g');

grid on
xlabel("Tiempo (s)")
ylabel("Amplitud")
title("Señal PPG en tiempo real")

set(gcf,'Color','k')  
set(gca,'Color','k') 
set(gca,'XColor','w','YColor','w')

tic
while toc < x
    if s.NumBytesAvailable > 0
        dato = str2double(readline(s));
        
        if ~isnan(dato)
            t = toc;

            tiempo(end+1) = t;
            senal(end+1) = dato;

            bufferV = [bufferV(2:end) dato];
            bufferT = [bufferT(2:end) t];

            if dato < valle_actual
                valle_actual = dato;
                valle_t = t;
            end

            if ~isnan(prev_dato)
                
                if dato > prev_dato
                    num_upsteps = num_upsteps + 1;
                else
                    if num_upsteps >= threshold
                        
                        if ~isnan(ultimo_pico_t)
                            delta_t = prev_t - ultimo_pico_t;
                        else
                            delta_t = Inf;
                        end

                        if delta_t <= 0.4
                            num_upsteps = 0;
                            continue;
                        end

                        pico_t = prev_t;
                        pico_v = prev_dato;

                        if pico_v > 1e5
                            num_upsteps = 0;
                            valle_actual = pico_v;
                            valle_t = pico_t;
                            continue;
                        end

                        valle_v = valle_actual;
                        valle_t_local = valle_t;

                        PPGA = pico_v - valle_v;

                        if ~isempty(PPGA_hist)
                            if PPGA < 0.3 * mean(PPGA_hist)
                                num_upsteps = 0;
                                continue;
                            end
                        end

                        picos_t(end+1) = pico_t;
                        picos_v(end+1) = pico_v;

                        valles_t(end+1) = valle_t_local;
                        valles_v(end+1) = valle_v;

                        ultimo_pico_t = pico_t;

                        if length(picos_t) > 1
                            HBI = pico_t - picos_t(end-1);
                        else
                            HBI = NaN;
                        end

                        if HBI < 0.4 || HBI > 1.5
                            HBI = NaN;
                        end

                        PPGA_hist(end+1) = PPGA;

                        if length(PPGA_hist) > ventana_norm
                            segmento = PPGA_hist(end-ventana_norm+1:end);
                        else
                            segmento = PPGA_hist;
                        end

                        min_ppga = min(segmento);
                        max_ppga = max(segmento);

                        PPGA_norm = (PPGA - min_ppga) / (max_ppga - min_ppga + eps);
                        PPGA_norm = min(max(PPGA_norm, 0), 1);

                        if ~isnan(HBI)
                            HBI_norm = (HBI - 0.4) / (1.2 - 0.4);
                            HBI_norm = min(max(HBI_norm, 0), 1);

                            HR_component = 1 - HBI_norm;
                            AMP_component = 1 - PPGA_norm;

                            SPI = 100 * (0.5 * HR_component + 0.5 * AMP_component);
                        else
                            SPI = NaN;
                        end

                        if ~isnan(SPI)
                            if ~isnan(SPI_prev)
                                SPI = 0.8 * SPI_prev + 0.2 * SPI;
                            end
                            SPI_prev = SPI;
                        end

                        if ~isnan(SPI)
                            psi_t(end+1) = pico_t;
                            psi_val(end+1) = SPI;
                        end

                        fprintf('SPI: %.0f\n', SPI);

                        valle_actual = pico_v;
                        valle_t = pico_t;

                        threshold = max(3, 0.3 * num_upsteps);
                    end
                    
                    num_upsteps = 0;
                end
            end

            prev_dato = dato;
            prev_t = t;

            if ~isempty(bufferT)
                t_min = bufferT(1);
                idx = picos_t >= t_min;
                picos_t = picos_t(idx);
                picos_v = picos_v(idx);

                idx = valles_t >= t_min;
                valles_t = valles_t(idx);
                valles_v = valles_v(idx);
            end

            set(h, 'XData', bufferT, 'YData', bufferV);
            set(h_picos, 'XData', picos_t, 'YData', picos_v);
            set(h_valles, 'XData', valles_t, 'YData', valles_v);

            ymin = min(bufferV);
            ymax = max(bufferV);

            if ~isnan(ymin) && ~isnan(ymax) && ymin ~= ymax
                margen = 0.1 * (ymax - ymin);
                ylim([ymin - margen, ymax + margen])
            end

            drawnow limitrate
        end
    end
end



close(1);
figure
plot(psi_t, psi_val, 'm', 'LineWidth', 2); hold on
grid on
xlabel("Tiempo (s)")
ylabel("SPI")
title("Índice SPI en el tiempo")
set(gcf,'Color','k')  
set(gca,'Color','k') 
set(gca,'XColor','w','YColor','w')

```
Este código en MATLAB está diseñado para leer una señal PPG en tiempo real desde un sensor (como el MAX30105) a través del puerto serial, procesarla y visualizarla mientras se adquiere. Al inicio, se configura la conexión, se definen buffers para mostrar una ventana de la señal en vivo y se inicializan varias variables que servirán para guardar datos, detectar eventos importantes (como picos y valles) y calcular el SPI. También se prepara la gráfica donde se verá la señal en tiempo real junto con los puntos detectados.

Una vez empieza el programa, entra en un ciclo que dura el tiempo que el usuario indicó. Dentro de este ciclo se leen los datos que llegan del sensor y se van almacenando junto con su tiempo correspondiente. Al mismo tiempo, se actualiza una ventana móvil de datos para poder graficar la señal de forma continua. Esto permite ver cómo cambia la señal PPG en vivo, lo cual es clave para monitoreo y análisis en tiempo real.

Luego viene la parte más importante: la detección de picos y valles. El código usa una lógica basada en contar cuántas veces seguidas la señal sube (método del alpinista). Cuando detecta suficientes subidas y luego una bajada, identifica un posible pico (latido). Antes de confirmarlo, aplica varios filtros para evitar errores, como verificar que no haya picos muy seguidos, que los valores no sean absurdos y que la amplitud del pulso sea suficientemente grande. Además, va registrando el valle previo a cada pico, lo cual es necesario para calcular la amplitud de la señal.

Con cada pico válido detectado, el código calcula dos variables fisiológicas importantes: el HBI (intervalo entre latidos), que está relacionado con la frecuencia cardíaca, y el PPGA (amplitud del pulso), que refleja la fuerza del flujo sanguíneo. Estos valores luego se normalizan para llevarlos a un rango común entre 0 y 1, lo que permite combinarlos de forma consistente.

Finalmente, se calcula el SPI, que es un índice que combina tanto la frecuencia cardíaca como la amplitud del pulso para dar una medida más global del estado fisiológico.  Mientras todo esto ocurre, la gráfica se actualiza en tiempo real mostrando la señal, los picos, los valles y al final se presenta una gráfica adicional con la evolución del SPI a lo largo del tiempo.

## Resultados y Analisis


<div align="center">
<img width="600" height="612" alt="Captura de pantalla 2026-03-26 185017" src="https://github.com/user-attachments/assets/db94f21b-cd69-48db-8485-87b374ab508f" />
</div>

Ahora mostramos cómo funciona el algoritmo en tiempo real, donde se puede ver la señal PPG junto con los picos y valles detectados. Estos puntos indican los latidos y los mínimos de la señal, lo que permite entender fácilmente cómo el algoritmo identifica cada pulso. La gráfica ayuda a ver de forma clara que la detección está funcionando correctamente.

<div align="center">
<img width="600" height="618" alt="Captura de pantalla 2026-03-26 185540" src="https://github.com/user-attachments/assets/76870a8d-0fb7-426a-9c06-b357e5db0f65" />
</div>

Finalmente, se observa la gráfica de la evolución del SPI en el tiempo. Durante los primeros 40 minutos aproximadamente, el SPI oscila entre 30 y 60, lo cual es un comportamiento normal en reposo, ya que la persona no está completamente bajo el efecto de la analgesia. Después de este periodo, el SPI aumenta al aplicar el estímulo de cold pressor, que genera vasoconstricción y disminuye la amplitud de la señal, es decir, el PPGA. Luego, al retirar el estímulo, el SPI vuelve a disminuir, regresando a valores más cercanos a los iniciales.




# PARTE C


# CONCLUSIONES


# REFERENCIAS

- E. J. Argüello-Prada, “The mountaineer’s method for peak detection in photoplethysmographic signals,” Revista Facultad de Ingeniería, Universidad de Antioquia, no. 90, pp. 42–50, Jan.–Mar. 2019, doi: 10.17533/udea.redin.n90a0642.
- C. L. von Baeyer, T. Piira, C. T. Chambers, M. Trapanotto y L. K. Zeltzer, “Guidelines for the Cold Pressor Task as an experimental pain stimulus for use with children,” The Journal of Pain, vol. 6, no. 4, pp. 218–227, Apr. 2005, doi: 10.1016/j.jpain.2005.01.349. [Online]. Available: https://www.jpain.org/article/S1526-5900(05)00366-4/fulltext
- Ferretronica, “Sensor MAX30102 frecuencia cardiaca y oxígeno en sangre,” Ferretronica, 2026. [Online]. Available: https://www.ferretronica.com/products/sensor-max30102-frecuencia-cardiaca-y-oxigeno-en-sangre
- S. K. Oh, Y. J. Won y B. G. Lim, “Surgical pleth index monitoring in perioperative pain management: usefulness and limitations,” Korean J. Anesthesiol., vol. 77, no. 1, pp. 31–45, Feb. 2024, doi: 10.4097/kja.23158. [Online]. Available: https://pmc.ncbi.nlm.nih.gov/articles/PMC10834712/
- A. Reyes, J. Márquez y J. Athié, “Comparing analgesic nociception index to surgical plethysmographic index in laparoscopic opioid analgesia,” Revista Mexicana (SciELO), 2024. [Online]. Available: https://www.scielo.org.mx/scielo.php?script=sci_arttext&pid=S0484-79032024000300151
