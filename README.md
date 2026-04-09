# TABD---Ejercicio-04---Lab01

SISTEMA DE RECOMENDACIÓN DE CURSOS - Ejercicio 4
...
CÓMO EJECUTAR:
1. Instalar dependencias: pip install chromadb sentence-transformers
2. Ejecutar: python sistema_cursos.py
3. Primera vez: se crean e insertan 20 cursos automáticamente
4. Siguientes veces: carga los datos ya persistidos desde ./sistema_cursos_db/

LIMITACIONES:
- ChromaDB EphemeralClient pierde datos al cerrar; por eso usamos PersistentClient
- Los filtros `where` solo soportan un campo con $and para múltiples condiciones
- sentence-transformers puede tardar en la primera ejecución (descarga el modelo)

POSIBLES MEJORAS:
- Añadir interfaz web con Gradio o Streamlit
- Permitir que el alumno califique recomendaciones (feedback loop)
- Integrar con un LLM para explicar por qué recomienda cada curso