# 📊 Análisis Comparativo de los 10 Principales Índices Bursátiles Mundiales (2018–2024)

Este proyecto realiza un análisis exploratorio de los diez índices bursátiles más importantes del mundo entre 2018 y 2024. Se centra en métricas clave como rendimiento acumulado, CAGR, drawdown promedio, volatilidad y volumen de negociación.

## 🌍 Índices Analizados

- 🇺🇸 S&P 500
- 🇺🇸 Nasdaq 100
- 🇺🇸 Dow Jones Industrial Average
- 🇺🇸 Russell 2000
- 🇪🇺 Euro Stoxx 50
- 🇫🇷 CAC 40
- 🇩🇪 DAX 40
- 🇬🇧 FTSE 100
- 🇯🇵 Nikkei 225
- 🇭🇰 Hang Seng Index

## 🧰 Tecnologías Usadas

- **Python**
- **Pandas**, **NumPy**: manipulación de datos
- **Plotly**, **Seaborn**, **Matplotlib**: visualización interactiva y estática
- **yfinance**: descarga de datos financieros históricos

## 📈 Indicadores Calculados

Para cada índice, se calculan las siguientes métricas:

- `rentabilidad`: cambio porcentual diario
- `rentabilidad_%`: rentabilidad diaria en porcentaje
- `media_movil_10d` y `media_movil_50d`: tendencias de corto y medio plazo
- `rentabilidad_acumulada`: evolución del rendimiento total
- `caida_maxima`: drawdown respecto al máximo histórico
- `volatilidad_30d`: desviación estándar de rentabilidad a 30 días
- `sharpe_30d`: ratio de Sharpe simplificado
- `CAGR`: crecimiento anual compuesto (2018–2024)
- `volumen_medio`: volumen medio de negociación diaria
- `drawdown_promedio`: promedio de caídas desde máximos
- `rendimiento_18_24`: rendimiento total en porcentaje del periodo

## 🧠 Metodología

1. **Descarga de datos:** usando `yfinance` para obtener precios diarios desde el 01/01/2018 hasta el 31/12/2024.
2. **Procesamiento:** se limpian los datos, se calculan indicadores técnicos y se normalizan los formatos.
3. **Resumen global:** se genera un DataFrame con indicadores comparativos entre los diez índices.
4. **Visualización:** se crean gráficos en alta resolución (3840x2160) para facilitar análisis visual:

   - 📈 Evolución del precio de cierre
   - 📊 Rendimiento total (barra horizontal)
   - 📊 CAGR por índice
   - 🗺️ Treemap por volumen de negociación
   - 📉 Caída promedio desde máximos

## 📂 Ejemplo de Salidas

- `/data/processed/allindex_procesado.csv`: resumen de métricas por índice
- `/plots/Grafica_Crec_Anual.png`: gráfico de crecimiento anual compuesto
- `/plots/grafica_rendimiento.png`: rendimientos 2018–2024
- `/plots/Grafica_Volumen.png`: volumen medio diario por índice
- `/plots/Grafica_SP500.png` … `/plots/Grafica_Russell2000.png`: evolución de precios individuales

## 💡 Valor Añadido

Este análisis proporciona una visión clara y directa para:

- Evaluar el rendimiento relativo de los principales mercados financieros.
- Identificar índices más consistentes o volátiles.
- Apoyar decisiones estratégicas en carteras diversificadas.
- Explorar la resiliencia de los mercados ante crisis (por ejemplo, COVID-19 o inflación 2022–2023).

## 📥 Requisitos

Instala las dependencias con:

```bash
pip install pandas numpy yfinance plotly kaleido
