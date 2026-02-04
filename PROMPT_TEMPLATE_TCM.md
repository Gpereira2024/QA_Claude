Necesito que generes un artifact HTML interactivo que cree un archivo Excel (.xlsx) 
descargable con la matriz TCM para Azure Test Plans del archivo [NOMBRE_ARCHIVO.md].

REQUISITOS OBLIGATORIOS:

1. **Tipo de artifact:** text/html
2. **Librería a usar:** SheetJS desde CDN
   - URL: https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js

3. **Estructura del Excel (5 pestañas obligatorias):**
   - Test Case
   - Draf-TCM
   - Variables
   - Variables Sugeridas
   - Pairwise

4. **Formato de columnas en "Test Case":**
   | ID | Work Item Type | Title | Test Step | Step Action | Step Expected | Description | Expected | Priority | Area Path | Assigned To | State |

5. **Reglas de formato:**
   - Pre-condiciones con saltos <br>
   - Work Item Type solo en primera fila de cada caso
   - Title solo en primera fila de cada caso
   - Test Step numerado desde 1 para cada caso
   - Description y Expected solo en primera fila
   - Priority, Area Path, Assigned To, State solo en primera fila
   - Agrupar pasos con mismo Step Expected usando <br> en Step Action

6. **Prioridades:**
   - Pruebas Tempranas (PT): Prioridad 1
   - Pruebas Regulares: Prioridad 1
   - Pruebas Negativas: Prioridad 2
   - Pruebas Regresión: Prioridad 3

7. **Variables dinámicas a usar:**
   - {Número}: [NUMERO_ITEM]
   - {Ítem}: [ITEM]
   - {Area Path}: [AREA_PATH]
   - {Assigned To}: [ASSIGNED_TO]
   - {State}: [STATE]

8. **Interfaz visual debe incluir:**
   - Título del proyecto
   - Información del ITEM
   - Estadísticas (casos totales, por tipo)
   - Lista de pestañas incluidas
   - Botón grande de descarga
   - Mensaje de confirmación al descargar

9. **Datos completos:**
   - TODOS los casos del archivo .md procesados
   - TODOS los pasos de cada caso
   - Precondiciones completas
   - Resultados esperados completos
   - NO resumir ni omitir información

10. **Anchos de columna optimizados:**
    - ID: 5
    - Work Item Type: 12
    - Title: 60
    - Test Step: 10
    - Step Action: 80
    - Step Expected: 80
    - Description: 100
    - Expected: 80
    - Priority: 8
    - Area Path: 45
    - Assigned To: 35
    - State: 10

