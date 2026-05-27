# EVALUCACION-FINAL-PROGRAMACION
# ==========================================
# FUNCIÓN / MÓDULO DE CLASIFICACIÓN
# ==========================================
def clasificar_compromiso(duracion, clicks):
    """
    Evalúa el nivel de compromiso de una sesión basado en la lógica de negocio.
    """
    if duracion > 180 and clicks > 8:
        return "Alto"
    else:
        return "Estándar / Bajo"

# ==========================================
# PROGRAMA PRINCIPAL
# ==========================================

# 1. Datos Iniciales: Matriz con 5 filas de datos [ID Cliente, Duración, Clicks]
matriz_sesiones = [
    [101, 200, 12],  # Cumple ambos (Alto)
    [102, 150, 5],   # No cumple ninguno
    [103, 300, 4],   # Solo cumple duración
    [104, 90, 15],   # Solo cumple clicks
    [105, 240, 10]   # Cumple ambos (Alto)
]

print("=== EVALUACIÓN DE COMPROMISO DE SESIONES ===")
print(f"{'ID Cliente':<12}{'Duración':<12}{'Clicks':<10}{'Nivel de Compromiso'}")
print("-" * 55)

# 2. Procesamiento de la matriz usando ciclos
for sesion in matriz_sesiones:
    id_cliente = sesion[0]
    duracion = sesion[1]
    clicks = sesion[2]
    
    # Llamada al módulo/función
    resultado = clasificar_compromiso(duracion, clicks)
    
    # Mostrar resultados formateados
    print(f"{id_cliente:<12}{duracion:<12}{clicks:<10}{resultado}") 
