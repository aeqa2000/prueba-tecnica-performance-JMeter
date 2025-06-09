# Prueba Técnica de Performance con JMeter
#### Arley Esteban Quintero Amaya - aeqa2000@gmail.com

Este README explica cómo preparar tu entorno en Windows y ejecutar la prueba de performance del repositorio [aeqa2000/prueba-tecnica-performance-JMeter](https://github.com/aeqa2000/prueba-tecnica-performance-JMeter).

---

## 🛠 Prerrequisitos

- **Java JDK 8+** instalado y en tu `PATH` (comprueba con `java --version`).
- **Apache JMeter 5.6.3** (ZIP)  
  La carpeta `apache-jmeter-5.6.3` se muestra en el repositorio de recursos: https://mega.nz/folder/r2wiXD4D#P1cbVQF1Q468sMGVnNYmcg.

---

## 🔧 Instalación y configuración de JMeter

1. **Descarga**  
   Asegúrate de tener el archivo ZIP de JMeter 5.6.3 (por ejemplo `apache-jmeter-5.6.3.zip`).

2. **Descomprimir**  
   - Elige una ruta fija en tu equipo, por ejemplo:  
     ```
     C:\User\apache-jmeter-5.6.3
     ```
   - Descomprime el contenido del ZIP en esa carpeta.

3. **Comprobar estructura**  
   Debes ver una carpeta `bin` dentro de `apache-jmeter-5.6.3`, con archivos como `jmeter.bat` y `ApacheJMeter.jar`.

---

## 🚀 Ejecutar JMeter GUI

1. Abre **PowerShell** o **CMD**.
2. Navega hasta la carpeta `bin` de JMeter:
     ```bash
     cd C:\User\apache-jmeter-5.6.3\bin
3. Lanza la interfaz gráfica de JMeter:
     ```bash
     jmeter.bat
Alternativa (si prefieres el JAR directamente):
     ```bash
     java -jar ApacheJMeter.jar

### 📝 Cargar y ejecutar el script
1. En la interfaz de JMeter, ve al menú File → Open....
2. Navega hasta tu copia del repositorio clonado y selecciona el archivo:
      ```bash
      prueba-tecnica-performance-JMeter/script-prueba-performance.jmx
3. Haz clic en Open; el plan de prueba aparecerá en el panel izquierdo.
4. Para iniciar la prueba, presiona el botón verde ▶ (Start) en la barra de herramientas.
5. Verás cómo comienzan a ejecutarse los grupos de hilos y los resultados se muestran en tiempo real.

### 📊 Ver resultados
Para guardar un informe:
1. Agrega un Listener (por ejemplo, View Results Tree o Summary Report) desde el árbol de elementos.
2. Después de la ejecución, haz clic en el Listener añadido y usa Save Table Data para exportar los datos.
3. Para un reporte HTML completo:
      ```bash
      jmeter.bat -n -t script-prueba-performance.jmx -l resultados.jtl -e -o C:\Herramientas\jmeter-report
Luego, abre C:\User\jmeter-report\index.html en tu navegador.
    
