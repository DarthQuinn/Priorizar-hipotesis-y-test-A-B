# Priorizar-hipotesis-y-test-A-B
Proyecto de Priorización de Hipótesis y Pruebas A/B
Toma de decisiones basada en datos para la optimización de comercio electrónico.
Este proyecto combina el framework ICE/RICE con un análisis estadístico riguroso de pruebas A/B para evaluar hipótesis de negocio y validar cambios en el producto.
📊 Priorización de Hipótesis (Puntuación ICE y RICE)
Evaluamos 9 hipótesis de negocio utilizando dos frameworks de priorización probados para determinar qué iniciativas implementar primero.


Rank	
1.Hipótesis: Agregar un formulario de suscripción a todas las páginas principales
2.Alcance: 10
3.Impacto: 7
4.Confianza: 8	
5.Esfuerzo: 5	
6.Puntaje ICE: 11.2	
7.Puntaje RICE: 112.0




🧪 Análisis de Prueba A/B: Grupo A vs Grupo B

📈 1. Dinámica de Ingresos
El Grupo B mostró un salto significativo en ingresos después del 17 de agosto de 2019, manteniendo un crecimiento sostenido paralelo a la trayectoria del Grupo A.
La correlación temporal sugiere que los cambios implementados impactaron positivamente la generación de ingresos.
📦 2. Evolución del Tamaño Promedio de Pedido
Table
Métrica	Observación
Fase Inicial	El Grupo B tuvo picos esporádicos; el Grupo A lideró cerca del 13 de agosto
Post-Implementación	El Grupo B saltó a ~160, luego se estabilizó alrededor de ~140
Análisis Visual	La mayor parte del área de diferencia acumulada se encuentra por encima de cero, confirmando tamaños de pedido más grandes en el Grupo B
✅ Conclusión: Los cambios impactaron favorablemente el volumen de compras.

🎯 3. Resultados de Significancia Estadística
Análisis de Datos Brutos
Table
Métrica	Valor P	Interpretación
Tasa de Conversión	0.017		✅ Estadísticamente significativo (p < 0.05)
Tamaño Promedio de Pedido	0.692		❌ No estadísticamente significativo (p > 0.05)
Datos Filtrados (Sin Anomalías)
Table
Métrica	Valor P		Interpretación
Tasa de Conversión	0.012		✅ Significancia confirmada — efecto más fuerte
Tamaño Promedio de Pedido	0.993		❌ Sin significancia; ligera desventaja para B

🔎 4. Distribución de Pedidos y Detección de Anomalías
Pedidos por Usuario:
La mayoría de usuarios (ambos grupos) realizan solo 1 pedido
Algunos usuarios realizan 2–4 pedidos
Anomalías detectadas: Usuarios con 5, 6 e incluso 7 pedidos — estos fueron filtrados para un análisis robusto
Distribución de Precios:
El Grupo A mostró precios de pedido más altos en bruto que el Grupo B
Diferencia en percentil 95: 34 unidades
Diferencia en percentil 99: 222 unidades

✅ Conclusiones Finales y Recomendaciones
Lo que Funcionó
🎯 El Grupo B logró tasas de conversión significativamente más altas 
📊 La tendencia de ingresos post-17 de agosto respalda el impacto positivo de los cambios
Lo que NO Funcionó
💰 El tamaño promedio de pedido NO mejoró significativamente — de hecho, los datos filtrados muestran una ligera disminución 

🎬 Veredicto: DETENER la Prueba
"El Grupo B lidera en conversión pero NO en tamaño promedio de pedido."
El objetivo principal era aumentar ambos indicadores: conversión Y tamaño promedio de pedido. Como solo se cumplió uno:
Terminar la prueba A/B — continuar no generaría insights adicionales significativos
Investigar el mecanismo de conversión — entender qué impulsó más compras sin aumentar el valor del carrito
Iterar sobre la hipótesis — probar modificaciones que apunten específicamente al aumento del valor de pedido (bundling, incentivos de monto mínimo, etc.)

🛠️ Metodología
Frameworks: ICE (Impacto × Confianza × Esfuerzo) y RICE (Alcance × Impacto × Confianza × Esfuerzo)
Pruebas Estadísticas: Mann-Whitney U / Pruebas Z para conversión; análisis bootstrap para tamaños de pedido
Filtrado de Anomalías: Eliminación de usuarios con ≥5 pedidos y valores atípicos extremos (percentil 99)
Umbral de Significancia: α = 0.05

🚀 Stack Tecnológico
 Python 

 Pandas 

 SciPy 

 Matplotlib


 📌 Conclusión Clave
Los datos superan la intuición. Si bien la prueba A/B mostró ganancias prometedoras en conversión, la falta de significancia estadística en el tamaño de pedido — combinada con la reversión de la tendencia en bruto tras el filtrado de anomalías — demuestra por qué el filtrado estadístico riguroso es esencial antes de tomar decisiones de negocio.