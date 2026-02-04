
# {Ítem} {Número} – Plan de Pruebas (Piloto)  
> Generado a partir del Gherkin proporcionado para **{Ítem} {Número}**.

---

## Pruebas Tempranas (PT)

## PT - [{Ítem} {Número} - 01] – {Título del caso}

### Pre-condición
-----------------<br>
**Pre-condición**<br>
-----------------<br>
0. Considerar entorno según caso de TCM.<br>
1. Tener acceso al sistema "VRS 2.0".<br>
2. Tener al menos un usuario.<br>
3. Tener al menos una persona con vehículo registrado.<br>
4. Tener documento "Hojas de recursos.xls".<br>
5. Tener documento "Figma.pdf".<br>
6. Tener documento "CEM".<br>
7. Tener documento "Manifiesto Funcional".<br>
8. Tener documento "Doc técnico con info de BD".<br>
9. Tener acceso a la BD.

### Pasos y resultados esperados de cada paso
1. {Paso 1}  
   **Resultado esperado:** {Resultado esperado 1}
2. {Paso 2}  
   **Resultado esperado:** {Resultado esperado 2}
(...)

### Resultado Esperado General
{Resultado general del escenario}

---

## Pruebas Regulares 

## [{Ítem} {Número} - 02] – {Título del caso} - {Servicio} - {Navegador} - {Idioma}

### Pre-condición
-----------------<br>
**Pre-condición**<br>
-----------------<br>
0. Considerar entorno según caso de TCM.<br>
1. Tener acceso al sistema "VRS 2.0".<br>
2. Tener al menos un usuario.<br>
3. Tener al menos una persona con vehículo registrado.<br>
4. Tener documento "Hojas de recursos.xls".<br>
5. Tener documento "Figma.pdf".<br>
6. Tener documento "CEM".<br>
7. Tener documento "Manifiesto Funcional".<br>
8. Tener documento "Doc técnico con info de BD".<br>
9. Tener acceso a la BD.

### Pasos y resultados esperados de cada paso
1. {Paso 1}  
   **Resultado esperado:** {Resultado esperado 1}
2. {Paso 2}  
   **Resultado esperado:** {Resultado esperado 2}
(...)

### Resultado Esperado General
{Resultado general del escenario}

---
### ANTECEDENTES

* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** se está generado un Caso de Servicios.
* **Entonces** se selecciona servicio de cambio de propietario (VCO/VCO+) y completan los requisitos del sistema.


<!--
* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** se está generado un Caso de Servicios.
* **Entonces** no se encuentra la persona registrada en el sistema.
* **Y** el botón **"Register person"** está visible y **habilitado**.

* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** se está generado un Caso de Servicios.
* **Entonces** llega al módulo de **"Payment"**.
* **Y** el botón **"Issue Invoice"** está visible y **habilitado**.

* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** se está generado un Caso de Servicios.
* **Entonces** se selecciona servicio de cambio de propietario (VCO/VCO+) y completan los requisitos del sistema.
* **Y** el botón **"Request Authorization"** se encuentra visible  y **habilitado**.

* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** se está generado un Caso de Servicios (VCO/VCO+).
* **Entonces** llega al módulo de **"Payment"**.
* **Y** el botón **"Check out"** está visible y **habilitado**.

* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** se ha completado los requisitos para completar un Caso de Servicios (VCO/VCO+).
* **Entonces** el botón **"Issue Invoice"** está visible y **habilitado**.
* **Y** se logra **"Completar"** el servicio sin inconvenientes.

* **Dado** que el usuario tiene acceso al sistema VRS 2.0 y ha iniciado sesión en el sistema (Según TCM).
* **Cuando** el operador ha completado el proceso de pago exitosamente de un servicio (VCO/VCO+).
* **Entonces** el sistema redirige y carga la pantalla de **"Case Summary"**.


-->

---
### CONFIG_VARIABLES:
  principales: [Servicio, Persona <!-- Autrización, Pago , Periodo Renovación, Periodo Gracia -->]        # <- aquí indicas las PRINCIPALES (orden importa)
  secundarias: [Navegador, Idioma <!--, Pantalla , Caso,-->]    # <- las demás van como SECUNDARIAS

### VARIABLES (renderizadas para nombres de caso)

- Servicio:
  - "serv: VCO"
  - "serv: VCO(+)"

- Persona:
  - "per: Natural"
  - "per: Organización"

- Navegador:
  - "nav: CH"
  - "nav: ED"
  - "nav: FF"
  
- Idioma:
  - "idi: ES"
  - "idi: EN"
  - "idi: DE"
  - "idi: FR"

<!-- PARA OTROS CASOS 
- Pantalla:
  - "pant: EX"
  - "pant: LP"
  
- Cerificado Seguro:
  - "cert: VIGENTE"
  - "cert: EXPIRADO"

- Cerificado Inpección:
  - "cert: VIGENTE"
  - "cert: EXPIRADO"

- Periodo Renovación:
  - "perR: ANTICIPADO"
  - "perR: VENCIDO"

- Periodo Gracia:
  - "perG: RANGO"
  - "perG: EXCEDIDO"

  - Pago:
  - "pag: Lic"
  - "pag: Seg+Lic"
  - "pag: Insp+Lic"
  - "pag: Seg+Insp+Lic"
  
- Caso:
  - "caso: Flotar"
  - "caso: Asignar"
  - "caso: Completar" 

- Autrización:
  - "aut: Aprobada"
  - "aut: Rehazada"

  -->

### GENERAR MATRIZ DE COMBINACIONES

   Considear generar la Matriz de combnaciones entre Escenarios, Variables Principales y Variables Secundarias, para tener una tablas de referencia para luego armar una hoja aparte en el excel que llamarás "Variables"

---

### COBERTURAS DE PRUEBAS
  Considerar crear casos negativos "ESCENARIOS NEGATIVOS"
  Considerar crear casos regresión "ESCENARIOS REGRESIÓN" 
  Considerar todas las variables *principales* de alto riesgo/impacto para el negocio
  Considerar todas las variables *secundarias* de contexto/entorno
  Aplicar Particiones de Equivalencia (válidas/inválidas) y Valores Límite (mín, mín±1, máx, máx±1)
  Usa Pairwise (2-way) como base para TODO el conjunto.	
  Garantiza cobertura de valores en las variables demarcadas como *principales*
  No se requiere la cobertura de valores en las variables demarcadas como *secundarias* 
  Se requiere incluir valores de las variable demarcadas como *secundarias* de forma aleatoria en los escenarios sin ingerencia en la cobertura, pero consideara todas estas e las combinaciones

---

### REGLAS DE EXTRACCIÓN (en orden de prioridad):
1) OVERRIDES (si el usuario los incluye en esta ejecución)
2) Evidencia en Gherkin (tags, tablas, Given/When/Then, Examples)
3) DEFAULTS_PROYECTO (si el usuario los incluye)
4) Fallbacks definidos arriba

---

### INSTRUCCIONES DE SALIDA:
1) Construye una "Matriz de Variables Resueltas" (columna: variable, valor, fuente: override|gherkin|default|fallback).
2) Genera los casos de "Pruebas Regulares". El título debe seguir EXACTAMENTE este formato:
   [{Ítem} {Número}-{XX}]–{Título del caso}-{Servicio}-{Persona}-{Navegador}-{Idioma} <!---{Autorización}-{Pago}-{Periodo Renovación}-{Periodo Gracia}-{Pantalla}-->
3) Incliur la estructura suministrada de la "Pre-condición" en cada escenario de pruebas.
4) Crea combinaciones mínimas útiles (smoke + error) en vez de cartesiano completo si no aporta.
5) Mantener la referencia a las reglas de negocio suministradas por ejemplo RG-CALC-XXX.
6) No muestres razonamiento interno.

---

### Buenas Prácticas ISTQB a aplicar
- **Oráculo de prueba:** Definir mensajes y estados exactos.  
- **Datos y entorno:** Especificar datos iniciales y verificaciones de persistencia en BD cuando aplique.  
- **Resultados esperados:** Redactar en forma **precisa y mesurable**, iniciando con *“El sistema debería…”*.  
- **Brevedad y claridad:** Evitar redundancias y pasos innecesarios.  
- **Priorización:** Asignar nivel de riesgo/prioridad.  
- **Revisabilidad:** Formato claro y estructurado para su análisis automático.  

---

# Con este enfoque, el modelo recibe instrucciones claras:  
- **Qué generar** (casos de prueba funcionales).  
- **Cómo estructurarlos** (Markdown + Gherkin + metadatos).  
- **Qué reglas seguir** (ISTQB + trazabilidad + independencia).  
- **Qué estilo usar** (machine-friendly: bloques definidos, etiquetas fijas, sin ambigüedad).


