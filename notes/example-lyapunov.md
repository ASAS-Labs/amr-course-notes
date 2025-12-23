---
layout: default
title: Example - Lyapunov Stability
parent: Notes
nav_order: 1
---

# Lyapunov Stability
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Introduction

This is an example note demonstrating the structure and formatting capabilities of the site.

## Mathematical Notation

Inline math: The Lyapunov function is defined as $V(x) > 0$ for all $x \neq 0$.

Display math:

$$
\dot{V}(x) = \frac{\partial V}{\partial x} f(x) \leq 0
$$

## Code Examples

```python
def lyapunov_candidate(x):
    """
    Example Lyapunov function
    """
    return x.T @ x
```

## Key Concepts

- **Positive Definite**: $V(x) > 0$ for all $x \neq 0$
- **Negative Semi-Definite**: $\dot{V}(x) \leq 0$
- **Asymptotic Stability**: $\dot{V}(x) < 0$

## References

1. Khalil, H. K. (2002). *Nonlinear Systems*. Prentice Hall.
2. Slotine, J. J. E., & Li, W. (1991). *Applied Nonlinear Control*. Prentice Hall.
