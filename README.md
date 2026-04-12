# Equipo 12 - Fundamentos de Diseño
### Carrera de Ingeniería Ambiental / Informática / Industrial  
**Universidad Peruana Cayetano Heredia**

---

## 🌍 Descripción del Equipo  
Somos el **Equipo 12** del curso Fundamentos de Diseño 2026-1, conformado por estudiantes de Ingeniería Ambiental / Informática / Industrial. Nuestro objetivo es desarrollar soluciones tecnológicas aplicadas a la gestión segura y eficiente del agua en el hogar.

## 🎯 Introducción

En muchas comunidades rurales del Perú, el acceso a agua en condiciones adecuadas depende de sistemas comunitarios administrados por las Juntas Administradoras de Servicios de Saneamiento (JASS). Estos sistemas suelen basarse en tanques de almacenamiento que distribuyen agua a viviendas cercanas. Sin embargo, la gestión de la calidad del agua, especialmente en la dosificación de cloro, se realiza de manera manual y sin monitoreo continuo.

Ante esta situación, se propone el desarrollo de un sistema automatizado que permita medir parámetros básicos como pH, turbidez y nivel de agua, con el fin de optimizar la dosificación de cloro en tanques comunitarios. De esta manera, se busca mejorar la gestión del agua mediante una solución accesible, adaptable y enfocada en las necesidades reales de estas comunidades.


## ⚠️ Problemática

1. Dosificación inadecuada de cloro

   En sistemas gestionados por las Juntas Administradoras de Servicios de Saneamiento, la cloración se realiza de forma manual y sin criterios técnicos estandarizados. Esto genera variaciones en la cantidad aplicada, ocasionando periodos con niveles insuficientes o excesivos de cloro en el agua.

2. Falta de monitoreo y control continuo 

   No existen sistemas que permitan medir de manera constante parámetros clave como pH, turbidez y volumen. Las evaluaciones son esporádicas, lo que impide detectar cambios en la calidad del agua a tiempo y tomar decisiones oportunas.

3. Riesgo sanitario asociado a la calidad del agua

   La deficiente gestión de la cloración y el control del agua incrementa el riesgo de Enfermedades Diarreicas Agudas en la población, especialmente en comunidades rurales donde el acceso a agua segura es limitado.
  
## 👽 Problema integrador  
En muchas comunidades rurales, el acceso al agua potable es gestionado por las Juntas Administradoras de Servicios de Saneamiento (JASS), las cuales se encargan del almacenamiento y distribución del recurso hídrico mediante tanques cisterna. Sin embargo, en estos sistemas no siempre se cuenta con mecanismos adecuados para la dosificación controlada de cloro ni con herramientas de monitoreo continuo de la calidad del agua.  

Esta situación puede generar una desinfección ineficiente, la proliferación de microorganismos y la posible presencia de contaminantes, afectando la calidad del agua y representando un riesgo para la salud pública. Además, la falta de control técnico limita una gestión eficiente y sostenible del recurso hídrico en estas comunidades.
 
## 🤗 Presentación de la solución  
Se propone el **diseño e implementación de un sistema de dosificación de cloro en tanques cisterna para el tratamiento de agua potable dirigido a comunidades rurales gestionadas por Juntas Administradoras de Servicios de Saneamiento (JASS)**.  

Este sistema integrará sensores para el monitoreo de parámetros como el pH, la turbidez y nivel del agua junto con un mecanismo automatizado de dosificación de cloro, permitiendo mantener niveles adecuados de desinfección en sistemas de abastecimiento comunitario.  

Asimismo, contará con un sistema de alertas que facilite a los operadores de la JASS el control oportuno de la calidad del agua, contribuyendo a mejorar la salud pública, prevenir enfermedades y fortalecer la gestión comunitaria del recurso hídrico en zonas rurales.


## 🙌 El sistema sigue los pasos:
🔹Monitoreo de nivel del tanque:
 El sistema inicia con la medición del nivel de agua, mediante un sensor que determina la cantidad de agua almacenada en el tanque. Esta información permite conocer el volumen disponible y evitar errores en la dosificación, como operar sin agua o sobredosificar.

🔹Monitoreo de calidad del agua:
 El sistema analiza la calidad del agua mediante sensores de:
- pH (condición química del agua)
  El sistema verifica el nivel de acidez o alcalinidad del agua.
Para que la desinfección con cloro sea eficaz, se considera que el pH debe ser menor a 8, ya que en ese rango el cloro mantiene una mayor eficiencia desinfectante.

- Turbidez (presencia de partículas o suciedad)
  Permite identificar contaminación visible o carga de sólidos en el agua. Y este deberá ser menor de 5 unidades nefelométricas de turbiedad (UNT), ya que alta turbidez reduce la efectividad del cloro porque protege microorganismos.

Estos parámetros permiten determinar si el agua es apta, está en estado de alerta o no es apta para consumo, evaluando cambios en tiempo real.

🔹Procesamiento y control (Arduino):
 Toda la información de los sensores es enviada a un Arduino, que procesa los datos y toma decisiones automáticas según las condiciones del sistema:
- Evalúa la calidad del agua
- Verifica el nivel del tanque
- Determina si se requiere dosificación de cloro o generación de alerta
- Considera el rango de pH adecuado para una desinfección eficiente
  
🔹Dosificación automática de cloro:
Si las condiciones lo requieren, el Arduino activa una bomba dosificadora, que aplica cloro en cantidades controladas. La dosificación se ajusta según el volumen de agua disponible en el tanque, asegurando una desinfección eficiente sin sobredosificación.

🔹Sistema de alertas:
El sistema genera alertas automáticas cuando detecta:
- pH
   . 🟢 Normal: 6.5 – 8.0
   . 🔴 Crítico: < 6.5 o > 8.5 (riesgo para consumo y desinfección ineficiente)
   
- Turbidez
   . 🟢 Normal: ≤ 5 NTU
   . 🔴 Crítico: > 5 NTU (alta presencia de partículas o contaminación)


## 🎯 Objetivos de Desarrollo Sostenible

🚰 ODS 6: Agua limpia y saneamiento  

El proyecto se alinea con el ODS 6 al implementar un sistema de monitoreo continuo y tratamiento automatizado para agua almacenada en tanques cisterna, abordando la falta de control de calidad en sistemas domésticos. Desde una perspectiva de ingeniería, la solución integra sensores de pH, turbidez y nivel, permitiendo la evaluación en tiempo real de parámetros críticos según estándares sanitarios. Esta integración facilita la clasificación automática del estado del recurso (apta, alerta o crítica) y la ejecución de procesos de desinfección mediante una dosificación de cloro controlada.

Este enfoque reduce significativamente la exposición a agua no tratada y fortalece el control sanitario en zonas sin infraestructura centralizada. Asimismo, al incorporar alertas y una dosificación proporcional al volumen, el sistema optimiza la eficiencia del tratamiento, mitigando los riesgos de subdosificación o sobredosificación del desinfectante.

❤️ ODS 3: Salud y bienestar  

El proyecto contribuye al ODS 3 ya que este mecanismo reduce la proliferación de microorganismos patógenos en el almacenamiento, especialmente en entornos que carecen de vigilancia sanitaria constante. Asimismo, el sistema de alertas actúa como un dispositivo de detección temprana, permitiendo al usuario intervenir oportunamente mediante el mantenimiento del tanque o la suspensión del consumo. Esto impacta directamente en la disminución de enfermedades gastrointestinales y otros riesgos asociados al uso de agua contaminada.



## 📸 Fotografía del Equipo  
<p align="center">
<img width="1408" height="768" alt="imagen_alumnos_IA" src="Recursos/Imágenes/imagen grupal .jpeg" />
  <em>Figura 1. Fotografía del equipo 12</em>
</p>

---

## 👥 Integrantes del Equipo  

| Foto | Nombre | Rol | Intereses |
|------|--------|-----|-----------|
| <img src="/Recursos/Imágenes/60885051.jpg" width="90"/> | **Ariana Cortéz** | Líder del equipo | Innovación social, sostenibilidad. |
| <img src="/Recursos/Imágenes/Luis.jpeg" width="90"/> | **Luis Huaccha** | Responsable de investigación | Gestión ambiental, desarrollo comunitario. |
| <img src="Recursos/Imágenes/70589968.jpg" width="90"/> | **Dulce Huicho** | Diseñadora | Diseño de prototipos, creatividad visual y enfoque ambiental. |
| <img src="/Recursos/Imágenes/claudiana.jpeg" width="90"/> | **Claudiana Pineda** | Encargada de documentación | Comunicación científica, redacción técnica. |
| <img src="/Recursos/Imágenes/renato.jpeg" width="90"/> | **Giacomo Jimenez** | Programador - Modelador | Programación, análisis de datos, simulación. |

---

## 📌 Resumen Final  
Este README describe de manera clara la identidad del equipo, sus motivaciones y los Objetivos de Desarrollo Sostenible (ODS) en los que se centrará el trabajo a lo largo del curso. 
