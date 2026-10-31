# 🗺️ Hoja de Ruta (Roadmap) — Godot Beehave 3D AI

Este documento define la evolución técnica, mejoras arquitectónicas y expansión de sistemas de inteligencia artificial para juegos 3D en Godot 4 basados en **Árboles de Comportamiento (Behavior Trees)** con el framework **Beehave**.

---

## 📌 Fase 1: Arquitectura Base e Integración (Completado ✅)
- [x] Estructura limpia y estandarizada para Godot 4 / 4.5.
- [x] Eliminación de caché voluminosa (`.godot`) y exclusión adecuada en `.gitignore`.
- [x] Controlador de personaje 3D en tercera persona completamente funcional.
- [x] Implementación de enemigo tipo Slime con estados: Patrulla (Wander), Detección/Persecución (Chase) y Ataque (Attack).
- [x] Nodos decoradores personalizados (ej. `UntilSuccess`).

---

## 📌 Fase 2: Sistemas Sensoriales y Coordinación Táctica (En Progreso 🔄)
- [ ] **Módulo de Percepción Sensorial Multicanal**:
  - Visión con cono angular configurable (FOV) y oclusión por mallas (`RayCast3D` / `Shapecast3D`).
  - Detección acústica (ruido de pasos, disparos o impactos de objetos físicos).
- [ ] **Blackboard Compartido para Tácticas de Grupo**:
  - Comunicación entre múltiples agentes para flanqueo coordinado y relevo de atacantes.
  - Asignación de ranuras de ataque (*attack slots*) para evitar amontonamiento de enemigos sobre el jugador.
- [ ] **Integración con Navegación 3D Dinámica (`NavigationServer3D`)**:
  - Evasión de obstáculos móviles mediante `NavigationObstacle3D`.
  - Rutas de escape procedurales hacia cobertura en caso de baja salud.

---

## 📌 Fase 3: Variaciones de Arquetipos y Depuración Visual 🚀
- [ ] **Nuevos Arquetipos de IA**:
  - *Enemigo Tirador a Distancia (Ranged)*: Mantenimiento de distancia óptima, puntería predictiva y recarga.
  - *Jefe de Fase (Boss)*: Fases secuenciales con transiciones de estados inmunes y ataques de área (AoE).
- [ ] **Herramienta de Depuración Visual en Runtime**:
  - Renderizado en pantalla de nodos activos del árbol de comportamiento (Overlay UI).
  - Visualización gráfica de conos de visión y vectores de navegación en modo depuración.
