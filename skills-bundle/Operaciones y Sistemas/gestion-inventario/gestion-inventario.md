---
name: gestion-inventario
description: "Diseña un sistema de gestión de inventario con niveles de reorden, seguimiento de existencias y auditorías regulares para evitar faltantes y derroche."
allowed-tools: Read Write Glob
metadata:
  author: Imperio Digital
  version: "1.0"
---

# Gestión de Inventario

## Cuándo Usar Este Skill

Usa este skill cuando necesites:
- Crear un sistema de seguimiento de inventario
- Definir puntos de reorden para evitar faltantes
- Auditar inventario regularmente
- Reducir el derroche y el dinero atrapado en stock

---

## Principio Fundamental

BUEN INVENTARIO NO ES SOBRE TENER MUCHO — ES SOBRE TENER LO CORRECTO EN EL MOMENTO CORRECTO PARA SERVIR A CLIENTES SIN ATRAPARTE CON EXCESO DE STOCK.

---

## Fase 1: Categorizar Artículos

Agrupa artículos por tipo y patrón de uso.

### Matriz de Inventario

| Artículo | Categoría | Uso Promedio/Mes | Tiempo de Reorden | Nivel de Seguridad |
|---------|----------|-----------------|------------------|-------------------|
| [Artículo] | [Tipo] | [X unidades] | [X días] | [X unidades] |

---

## Fase 2: Definir Puntos de Reorden

Calcula cuándo y cuánto pedir.

### Fórmula de Punto de Reorden

```
Punto de Reorden = (Uso Promedio Mensual ÷ 30) × Tiempo de Reorden + Nivel de Seguridad
```

---

## Fase 3: Sistema de Seguimiento

Crea proceso regular de auditoría.

### Cadencia de Auditoría

- Semanal: Verificación visual de artículos críticos
- Mensual: Conteo de muestra de artículos principales
- Trimestral: Auditoría completa de inventario

### Plantilla de Auditoría

| Artículo | Conteo Esperado | Conteo Real | Diferencia | Nota |
|---------|----------------|------------|-----------|------|
| [Artículo] | [X] | [X] | [X] | [Razón si hay diferencia] |

---

## Anti-Patrones

- **Demasiado stock** — dinero atrapado, riesgo de desperdicio
- **Muy poco stock** — clientes insatisfechos, pérdida de ingresos
- **Sin sistema de seguimiento** — pierdes el control
- **Auditorías irregulares** — no descubres problemas a tiempo

---

## Recuperación

- **Faltantes frecuentes:** Aumenta puntos de reorden o reduce tiempo de entrega
- **Exceso de stock:** Reduce puntos de reorden o aumenta frecuencia de auditoría
- **Diferencias en auditoría:** Investiga pérdidas, robos o errores de conteo
