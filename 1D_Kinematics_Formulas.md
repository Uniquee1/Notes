
# 📘 Physics 1D Kinematics Formula Sheet

This document summarizes the essential formulas from the "Displacement", "Instantaneous Velocity and Acceleration", and "Motion Graphs" lessons. Each formula includes a brief explanation and a sample example.

---

## 📍 Section 1: Displacement, Velocity & Acceleration

### Distance and Displacement
- **Distance** (scalar):  
  `d = |x_f - x_i|`  
- **Displacement** (vector):  
  `Δx = x_f - x_i`

**Example:** A student walks 10 m east and 3 m west.  
Total distance = 13 m, Displacement = 7 m

---

### Speed and Velocity
- **Speed**:  
  `s = |Δx| / Δt`
- **Velocity**:  
  `v̄ = Δx / Δt`

**Example:** 50 m east in 5 s, then 10 m west in 2 s  
Speed = 15 m/s, Velocity = 5 m/s

---

### Instantaneous Velocity and Acceleration
- **Instantaneous Velocity**:  
  `v(t) = dx/dt`
- **Instantaneous Acceleration**:  
  `a(t) = dv/dt = d²x/dt²`

**Example:**  
`x(t) = t² − 2t`  
Then `v(t) = 2t − 2`, and `a(t) = 2`

---

### Kinematic Equations (Constant Acceleration)
1. `x = x_i + v̄t`
2. `v̄ = (v_i + v_f)/2`
3. `v_f = v_i + at`
4. `x = x_i + v_it + ½at²`
5. `v_f² = v_i² + 2a(x - x_i)`

---

## 📍 Section 2: Instantaneous Velocity & Acceleration (Calculus-based)

### Position Function
`x(t) = x_i + vt + ½at²`

### Derivatives for Velocity and Acceleration
- `v(t) = dx/dt`
- `a(t) = dv/dt`

**Example:**  
`x(t) = 0.2t² − t`  
Then `v(t) = 0.4t − 1`, `a(t) = 0.4`

---

### Integration for Displacement
- If velocity `v(t)` is given, then  
  `Displacement = ∫ₐᵇ v(t) dt`

**Example:**  
`v(t) = 0.1t²`, from 0 to 5 s  
Displacement = ∫₀⁵ 0.1t² dt = 4.1625 m

---

## 📍 Section 3: Motion-Time Graphs

### Derivatives and Integrals in Graphs
- `v = dx/dt`: Slope of position-time graph
- `a = dv/dt`: Slope of velocity-time graph
- Displacement = Area under velocity-time graph
- Change in velocity = Area under acceleration-time graph

---

### Graphical Example
If `x(t) = 2t³ − 5t² + 2t`  
Then:
- `v(t) = 6t² − 10t + 2`  
- `a(t) = 12t − 10`

---

### Area Under Curves for Displacement and Distance
If velocity is piecewise:

**Example:**  
From t = 0 to 10 s: velocity = 4 m/s  
Displacement = 10 × 4 = 40 m  
From t = 10 to 14 s: triangle with base 4, height 4  
Area = 0.5 × 4 × 4 = 8 m  
Total = 48 m

Total distance: Sum of absolute values of all areas

---

## 📍 Special Cases

- **Free fall**: Use `g = −9.8 m/s²`
- **Peak of projectile**: `v = 0`, solve using  
  `v² = v_i² + 2aΔx` or `v = v_i + at`

**Example:**  
Ball thrown up at 10 m/s  
Max height = `−(10)² / 2(−9.8)` = 5.10 m  
Time to max height = `−v_i / g = 1.02 s`

---

## 🧮 Notation Recap

| Symbol | Meaning              |
|--------|----------------------|
| x      | Position (m)         |
| Δx     | Displacement (m)     |
| v      | Instantaneous velocity (m/s) |
| v̄     | Average velocity (m/s) |
| a      | Acceleration (m/s²)  |
| t      | Time (s)             |
| g      | Gravity (≈ -9.8 m/s²)|

---

**End of Summary**  
Derived from General Physics Chapter 3 PDFs: Displacement, Instantaneous Velocity and Acceleration, and Motion-Time Graphs.
