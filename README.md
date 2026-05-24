# ============================================
# UNIVERSIDAD NACIONAL ABIERTA Y A DISTANCIA
# FUNDAMENTOS DE PROGRAMACIÓN
# FASE 5 - EVALUACIÓN FINAL POA
# PROBLEMA 3 - AUDITORÍA DE INVENTARIO
# ESTUDIANTE: JHON HAROLD
# ============================================

# Matriz del inventario
inventario = [
    ["A101", "Teclado", 5, 10],
    ["A102", "Mouse", 15, 10],
    ["A103", "Monitor", 3, 8],
    ["A104", "Memoria USB", 20, 15],
    ["A105", "Impresora", 1, 5]
]

# Función para calcular cantidad a pedir
def calcular_pedido(stock_actual, stock_minimo):

    if stock_actual < stock_minimo:
        cantidad = stock_minimo - stock_actual
    else:
        cantidad = 0

    return cantidad


print("==========================================")
print("REPORTE DE REABASTECIMIENTO")
print("==========================================")

# Recorrido de la matriz
for articulo in inventario:

    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    pedido = calcular_pedido(stock_actual, stock_minimo)

    print("Código:", codigo)
    print("Artículo:", nombre)
    print("Stock actual:", stock_actual)
    print("Stock mínimo:", stock_minimo)
    print("Cantidad a pedir:", pedido)
    print("--------------------------------------")
    
