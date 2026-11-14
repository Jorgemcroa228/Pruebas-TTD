# Laboratorio TDD: carrito de compras

Taller práctico de Desarrollo Guiado por Pruebas (TDD) con JavaScript puro,
usando solo Node.js y `node:test`. Ciclo: **Rojo → Verde → Refactor**.

## Requisitos

- Node.js 20 o superior
- Git

## Uso

```bash
npm test
```

No requiere `npm install`: el proyecto no tiene dependencias.

## Estructura

```
├── package.json        ← configuración y comando de pruebas
├── src/carrito.js      ← código de producción
└── test/carrito.test.js← pruebas
```

## Criterios de aceptación

1. Un carrito nuevo está vacío: 0 ítems y subtotal $0.
2. Se pueden agregar productos con nombre, precio y cantidad (por defecto, 1).
3. Si se agrega un producto que ya está, se suma la cantidad.
4. No se aceptan precios ≤ 0 ni cantidades que no sean enteros positivos.
5. Se pueden eliminar productos; eliminar uno inexistente es un error.
6. Cupones válidos: DESC10 (10 %) y DESC20 (20 %).
7. IVA del 19 % calculado después del descuento.
