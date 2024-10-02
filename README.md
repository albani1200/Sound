# Sound
El amor del **sonido**
```# Cargar la librería necesaria
library(tuneR)

 Función para generar un tono
generate_tone <- function(frequency, duration = 1, sample_rate = 44100) {
  t <- seq(0, duration, by = 1/sample_rate)
  wave <- sin(2 * pi * frequency * t)
  wave <- wave * 32767  # Escalar para el rango de int16
  wave <- as.integer(wave)
  Wave(wave, samp.rate = sample_rate, bit = 16)
}

 Frecuencias a generar
frequencies <- seq(60, 380, by = 20)

 Beneficios de cada frecuencia
benefits <- c(
  "60 Hz: Ayuda a la relajación profunda y la reducción del estrés.",
  "80 Hz: Mejora la concentración y la claridad mental.",
  "100 Hz: Ayuda en la meditación y el equilibrio emocional.",
  "120 Hz: Puede estimular la creatividad y la autoexpresión.",
  "140 Hz: Favorece la estabilidad emocional y la armonía.",
  "160 Hz: Aumenta la energía y la motivación.",
  "180 Hz: Promueve la conexión espiritual y el bienestar.",
  "200 Hz: Mejora la salud física y la vitalidad.",
  "220 Hz: Fortalece el sistema inmunológico.",
  "240 Hz: Ayuda a aliviar la ansiedad y la tensión.",
  "260 Hz: Fomenta la paz interior y la tranquilidad.",
  "280 Hz: Promueve la empatía y las relaciones interpersonales.",
  "300 Hz: Aumenta la autoestima y la confianza.",
  "320 Hz: Mejora la comunicación y la expresión personal.",
  "340 Hz: Estimula la mente y mejora el estado de alerta.",
  "360 Hz: Fomenta la relajación y la recuperación.",
  "380 Hz: Ayuda a equilibrar las energías del cuerpo."
)

Generar y reproducir tonos
for (i in seq_along(frequencies)) {
  cat(benefits[i], "\n")
  tone <- generate_tone(frequencies[i])
  play(tone)
  Sys.sleep(2)  # Esperar 2 segundos entre tonos
}
```
## cargar la libreria **tuneR** en r.


![image](https://github.com/user-attachments/assets/bead3c0b-2753-4233-9b44-5b8fd1775146)
https://pixabay.com/es/sound-effects/search/nature/
