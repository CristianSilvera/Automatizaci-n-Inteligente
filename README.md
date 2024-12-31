# Automatización Inteligente: Testing Funcional con IA.

Este documento es un extracto de la idea fundamental derivada del trabajo final presentado en la defensa del Diploma Gerencia de Calidad y Testing de Software 2024, como trabajo final. 

El trabajo original del cual deriva este extracto es de la autoría de Valentina Prado, Cristian Silvera.

Explica los conceptos, procesos y beneficios de integrar Inteligencia Artificial en el testing funcional mediante un sistema de automatización inteligente con capacidades de autocorrección.

Para facilitar su comprensión, realicé una simplificación del trabajo realizado. Esta abstracción pretende explicar el ciclo de vida de los tres componentes fundamentales que participan del sistema.

---

---

### **Planteo del sistema.**

---

La idea fundamental de este trabajo es diseñar un **sistema de automatización con capacidades de autocorrección (Self-Healing)**, compuesto por tres elementos principales:

1. **Test Automatizado**:
    - Ejecuta pruebas sobre una aplicación (por ejemplo, una calculadora Android).
    - Monitorea los logs de la aplicación en busca de errores que puedan ocurrir debido a cambios en los selectores o la interfaz.
2. **Modelo LLM-RAG (Language Model + Retrieval-Augmented Generation)**:
    - Recibe consultas derivadas de los logs con detalles de errores.
    - Procesa y analiza los datos mediante vectorización y un motor de consulta, generando una respuesta enriquecida, como selectores actualizados y funcionales.
3. **Aplicación**:
    - Actúa como el entorno bajo prueba.
    - Proporciona los datos (logs) que desencadenan la retroalimentación en el sistema.

### **Flujo del Sistema:**

1. El Test Automatizado ejecuta un script y monitorea los logs de la aplicación.
2. Ante un error, el Test genera una consulta con los detalles del problema y la envía al Modelo LLM-RAG.
3. El Modelo procesa la consulta, busca en su base de datos vectorizada y devuelve una respuesta con información actualizada (nuevos selectores).
4. El Test aplica la información para corregir el error y re ejecutar la prueba (Self-Healing).
5. Si la corrección falla después de varios intentos, el sistema registra los detalles del error para una intervención manual.

### **Propósito:**

El objetivo del sistema es reducir la dependencia de la intervención humana en la automatización de pruebas, permitiendo que las pruebas puedan adaptarse automáticamente a cambios en la aplicación, mejorando así la eficiencia y confiabilidad en el proceso de testing.
