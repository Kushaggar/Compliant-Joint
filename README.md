# Translational Constraint Joint with 5 Degrees of Freedom

**Research Project | Mechatronics Lab, IIT Delhi**
**Supervised by Prof. Jitendra P. Khatait & Subrat (PhD Student)**

A compliant mechanism designed to constrain translation along the Y-axis while 
allowing controlled motion across 4 remaining DOFs. Stiffness values were derived 
analytically and validated against ANSYS static structural simulations.

---

## Overview

Traditional joints rely on sliding or rolling contact to guide motion — introducing 
friction, wear, and assembly complexity. This compliant mechanism achieves the same 
constraint behavior through elastic deformation of flexible members, with no moving 
parts, no lubrication, and no assembly required.

The joint constrains **1 DOF (Translation in Y)** while permitting:
- Rotation in X or Z axis
- Rotation in Y axis
- Translation in X axis
- Translation in Z axis

---

## Geometry

| Parameter | Value |
|---|---|
| Outer Diameter | 25 mm |
| Total Length | 106 mm |
| Flexure Thickness (t) | 0.50 mm |
| Flexure Radius (r) | R1.50 mm |
| Inner Radius | R5.00 mm |

---

## Specifications

| Motion | Displacement Range | Stiffness (Simulation) | Stiffness (Analytical) | Max Stress |
|---|---|---|---|---|
| Rotation X or Z | ±2.2° | 16.6 Nm/rad | 18.1 Nm/rad | 167.36 MPa |
| Rotation Y | ±4.6° | 21.86 Nm/rad | 21.81 Nm/rad | 308.35 MPa |
| Translation X | ±0.5 mm | 35.3 N/mm | 40.6 N/mm | 186.61 MPa |
| Translation Z | ±0.5 mm | 19.318 N/mm | 21.34 N/mm | 162.13 MPa |
| Translation Y | Constrained | 84745.76 N/mm | 94339.62 N/mm | — |

---

## Analytical Formulations

**Rotation in X or Z Axis:**

$$\theta = \sin^{-1}\left(\frac{l+r+t}{\sqrt{(l+r)^2+\left(\frac{d}{2}\right)^2}}\right) - \sin^{-1}\left(\frac{l+r}{\sqrt{(l+r)^2+\left(\frac{d}{2}\right)^2}}\right)$$

**Rotation in Y Axis:**

$$\theta = \sin^{-1}\left(\frac{2t}{\sqrt{t^2+\left(\frac{d}{2}\right)^2}}\right) - \sin^{-1}\left(\frac{t}{\sqrt{t^2+\left(\frac{d}{2}\right)^2}}\right)$$

**Translation in X or Z Axis:**

$$\delta = \pm t$$

---

## Simulation vs Analytical — Summary

| Motion | % Error |
|---|---|
| Rotation X/Z | 9% |
| Rotation Y | 0.2% |
| Translation X | 15% |
| Translation Z | 10% |
| Translation Y | 11.3% |

All results within acceptable range for compliant mechanism design at this scale.
Rotation Y shows near-perfect agreement (0.2%) between simulation and analytical model.

**Critical Buckling Load (Translation Y, Euler's formula):** 2.3 × 10⁴ N

---

## Tools & Methods
- **CAD:** SolidWorks
- **Simulation:** ANSYS Workbench — Static Structural
- **Validation:** Analytical beam theory (ML/EI, PL³/3EI, torsion stiffness formulations)

---

## Files

| File | Description |
|---|---|
| *5 DOF* | SolidWorks part file |
| `Translation Constraint Joint with 5 DOF.pdf` | Full project report with simulation results |

---

## Context
This work was completed during a research internship at the **Mechatronics Lab, IIT Delhi**
under the supervision of **Prof. Jitendra P. Khatait**.

**Portfolio:** [kushank.vercel.app](https://kushank.vercel.app)
