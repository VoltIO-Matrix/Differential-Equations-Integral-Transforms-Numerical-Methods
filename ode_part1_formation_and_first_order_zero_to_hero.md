# ODE Zero-to-Hero Notes — Part 1

## Formation of Differential Equations + Solving First Order Differential Equations

**Made for:** beginner level — assuming you already know basic differentiation and integration.  
**Main goal:** learn *how to recognize the type of question*, *what steps to follow*, and *how to solve it neatly*.

---

# How to Study This File

Do **not** try to memorize everything at once.

Use this order:

1. Read the **idea** of the topic.
2. Learn the **standard form**.
3. Follow the **step-by-step method**.
4. Study the **tute examples**.
5. Try the **extra examples** by yourself first, then check the solution.

---

# Very Important Symbols

| Symbol | Meaning |
|---|---|
| `y` | dependent variable |
| `x` | independent variable |
| `dy/dx` or `y'` | first derivative of `y` with respect to `x` |
| `d²y/dx²` or `y''` | second derivative |
| `C`, `C₁`, `C₂` | arbitrary constants |
| `∫` | integration |

---

# 1. Formation of Differential Equations

## 1.1 What does “formation” mean?

Sometimes we are given a **family of curves** with arbitrary constants.

Example:

```text
y = mx
```

This represents many straight lines through the origin because `m` can be any number.

To form a differential equation, we remove the arbitrary constant.

So the goal is:

```text
Equation with arbitrary constants  →  Differential equation without arbitrary constants
```

---

## 1.2 Main rule

If the given equation has `n` arbitrary constants:

1. Differentiate the equation `n` times.
2. Use the original equation and differentiated equations.
3. Eliminate the arbitrary constants.
4. The final answer is usually an `n`th order differential equation.

---

## 1.3 Tute Example 2.1

### Question

Form the differential equation of all straight lines passing through the origin.

### Given family

A straight line through origin is:

```text
y = mx
```

where `m` is an arbitrary constant.

### Step 1: Count constants

There is only one arbitrary constant: `m`.

So we differentiate once.

### Step 2: Differentiate

```text
y = mx
```

Differentiate with respect to `x`:

```text
dy/dx = m
```

### Step 3: Eliminate constant

From the original equation:

```text
y = mx
```

So:

```text
m = y/x
```

But from derivative:

```text
m = dy/dx
```

Therefore:

```text
dy/dx = y/x
```

Multiply by `x`:

```text
x dy/dx = y
```

### Final answer

```text
x dy/dx - y = 0
```

---

## 1.4 Tute Example 2.2

### Question

Form the differential equation representing:

```text
y = ax² + bx
```

### Step 1: Count constants

The constants are:

```text
a, b
```

There are 2 constants, so differentiate twice.

### Step 2: Differentiate once

```text
y = ax² + bx
```

```text
y' = 2ax + b
```

### Step 3: Differentiate again

```text
y'' = 2a
```

So:

```text
a = y''/2
```

### Step 4: Find `b`

From:

```text
y' = 2ax + b
```

```text
b = y' - 2ax
```

Since `a = y''/2`:

```text
b = y' - 2x(y''/2)
```

```text
b = y' - xy''
```

### Step 5: Substitute into original equation

Original:

```text
y = ax² + bx
```

Substitute `a = y''/2` and `b = y' - xy''`:

```text
y = (y''/2)x² + (y' - xy'')x
```

Expand:

```text
y = x²y''/2 + xy' - x²y''
```

Combine:

```text
y = xy' - x²y''/2
```

Multiply by 2:

```text
2y = 2xy' - x²y''
```

Bring all terms to one side:

```text
x²y'' - 2xy' + 2y = 0
```

### Final answer

```text
x² d²y/dx² - 2x dy/dx + 2y = 0
```

---

## 1.5 Extra Example 1

### Question

Form the differential equation for:

```text
y = ax + b
```

### Solution

Constants: `a`, `b`. So differentiate twice.

```text
y' = a
```

```text
y'' = 0
```

### Final answer

```text
d²y/dx² = 0
```

---

## 1.6 Extra Example 2

### Question

Form the differential equation for:

```text
y = ae^x
```

### Solution

One constant: `a`. Differentiate once.

```text
y' = ae^x
```

But:

```text
y = ae^x
```

So:

```text
y' = y
```

### Final answer

```text
dy/dx - y = 0
```

---

## 1.7 Extra Example 3

### Question

Form the differential equation for:

```text
y = a cos x + b sin x
```

### Solution

Constants: `a`, `b`. Differentiate twice.

Original:

```text
y = a cos x + b sin x
```

First derivative:

```text
y' = -a sin x + b cos x
```

Second derivative:

```text
y'' = -a cos x - b sin x
```

But:

```text
y = a cos x + b sin x
```

Therefore:

```text
y'' = -y
```

### Final answer

```text
y'' + y = 0
```

---

## 1.8 Extra Example 4

### Question

Form the differential equation for:

```text
y = Ce^(3x)
```

### Solution

One constant: `C`. Differentiate once.

```text
y' = 3Ce^(3x)
```

Since:

```text
y = Ce^(3x)
```

we get:

```text
y' = 3y
```

### Final answer

```text
dy/dx - 3y = 0
```

---

## 1.9 Extra Example 5

### Question

Form the differential equation for:

```text
x² + y² = a²
```

### Solution

One constant: `a`. Differentiate once.

```text
d/dx(x² + y²) = d/dx(a²)
```

```text
2x + 2y dy/dx = 0
```

Divide by 2:

```text
x + y dy/dx = 0
```

### Final answer

```text
x + y dy/dx = 0
```

---

# 2. Solving First Order Differential Equations

A first order differential equation contains only the first derivative `dy/dx`.

General form:

```text
dy/dx = F(x,y)
```

There are several methods. The main challenge is choosing the correct method.

In this file we cover:

1. General and particular solutions
2. Variable separable method
3. Homogeneous differential equations
4. Integrating factor method
5. Exact differential equations

---

# 3. General and Particular Solutions

## 3.1 General solution

A **general solution** contains arbitrary constants.

Example:

```text
y = Cx²
```

Here `C` is arbitrary.

## 3.2 Particular solution

A **particular solution** is obtained after using given conditions.

Example:

```text
y = Cx²
```

If given `y(1)=5`, then:

```text
5 = C(1)²
```

```text
C = 5
```

So particular solution:

```text
y = 5x²
```

---

## 3.3 Tute Example 3.1

### Question

Show that:

```text
y = C₁ sin x + C₂ cos x
```

is a solution of:

```text
y'' + y = 0
```

### Solution

Differentiate once:

```text
y' = C₁ cos x - C₂ sin x
```

Differentiate again:

```text
y'' = -C₁ sin x - C₂ cos x
```

But:

```text
y = C₁ sin x + C₂ cos x
```

So:

```text
y'' = -y
```

Substitute into the differential equation:

```text
y'' + y = -y + y = 0
```

### Final statement

Yes, it is a solution.

---

## 3.4 Tute Example 3.2

### Question

Verify that:

```text
y = e^(-3x)
```

is a solution of:

```text
y'' + y' - 6y = 0
```

### Solution

Given:

```text
y = e^(-3x)
```

Differentiate:

```text
y' = -3e^(-3x)
```

Differentiate again:

```text
y'' = 9e^(-3x)
```

Substitute into equation:

```text
y'' + y' - 6y
```

```text
= 9e^(-3x) - 3e^(-3x) - 6e^(-3x)
```

```text
= (9 - 3 - 6)e^(-3x)
```

```text
= 0
```

### Final statement

Yes, `y = e^(-3x)` is a solution.

---

## 3.5 Extra Example 1

### Question

Verify that:

```text
y = x²
```

satisfies:

```text
y' = 2x
```

### Solution

Differentiate:

```text
y' = d/dx(x²) = 2x
```

This equals the right side.

### Final answer

Yes, it satisfies the equation.

---

## 3.6 Extra Example 2

### Question

Find the particular solution if:

```text
y = Cx³
```

and:

```text
y(2) = 16
```

### Solution

Substitute `x=2`, `y=16`:

```text
16 = C(2³)
```

```text
16 = 8C
```

```text
C = 2
```

### Final answer

```text
y = 2x³
```

---

## 3.7 Extra Example 3

### Question

Verify that:

```text
y = sin x
```

satisfies:

```text
y'' + y = 0
```

### Solution

```text
y' = cos x
```

```text
y'' = -sin x
```

Substitute:

```text
y'' + y = -sin x + sin x = 0
```

### Final answer

Yes, it satisfies the equation.

---

## 3.8 Extra Example 4

### Question

Find the particular solution:

```text
y = C₁e^x + C₂e^(-x)
```

with:

```text
y(0)=4,     y'(0)=2
```

### Solution

First derivative:

```text
y' = C₁e^x - C₂e^(-x)
```

Use `y(0)=4`:

```text
C₁ + C₂ = 4
```

Use `y'(0)=2`:

```text
C₁ - C₂ = 2
```

Add equations:

```text
2C₁ = 6
```

```text
C₁ = 3
```

Then:

```text
C₂ = 1
```

### Final answer

```text
y = 3e^x + e^(-x)
```

---

## 3.9 Extra Example 5

### Question

Check whether:

```text
y = 3e^(2x)
```

solves:

```text
y' - 2y = 0
```

### Solution

```text
y' = 6e^(2x)
```

Substitute:

```text
y' - 2y = 6e^(2x) - 2(3e^(2x))
```

```text
= 6e^(2x) - 6e^(2x) = 0
```

### Final answer

Yes, it is a solution.

---

# 4. Variable Separable Method

## 4.1 When to use this method

Use variable separable method when the equation can be arranged like this:

```text
dy/dx = g(x)h(y)
```

That means:

- all `y` terms can go with `dy`
- all `x` terms can go with `dx`

---

## 4.2 Main steps

Given:

```text
dy/dx = g(x)h(y)
```

Step 1:

```text
dy/h(y) = g(x) dx
```

Step 2:

```text
∫ dy/h(y) = ∫ g(x) dx
```

Step 3:

Add constant `C`.

---

## 4.3 Tute Example 3.3

### Question

Find the general solution:

```text
dy/dx = (x + 1)/(2 - y),     y ≠ 2
```

### Solution

Separate variables:

```text
(2 - y) dy = (x + 1) dx
```

Integrate both sides:

```text
∫(2 - y) dy = ∫(x + 1) dx
```

Left side:

```text
∫(2 - y) dy = 2y - y²/2
```

Right side:

```text
∫(x + 1) dx = x²/2 + x
```

So:

```text
2y - y²/2 = x²/2 + x + C
```

Multiply by 2:

```text
4y - y² = x² + 2x + C
```

### Final answer

```text
4y - y² = x² + 2x + C
```

---

## 4.4 Tute Example 3.4

### Question

Find the particular solution:

```text
dy/dx = -4xy²
```

with:

```text
y = 1 when x = 0
```

### Solution

Separate variables:

```text
dy/y² = -4x dx
```

Write `1/y²` as `y⁻²`:

```text
y⁻² dy = -4x dx
```

Integrate:

```text
∫y⁻² dy = ∫-4x dx
```

```text
-1/y = -2x² + C
```

Use condition `y(0)=1`:

```text
-1/1 = -2(0)² + C
```

```text
C = -1
```

So:

```text
-1/y = -2x² - 1
```

Multiply by `-1`:

```text
1/y = 2x² + 1
```

### Final answer

```text
y = 1/(2x² + 1)
```

---

## 4.5 Extra Example 1

### Question

Solve:

```text
dy/dx = xy
```

### Solution

Separate:

```text
dy/y = x dx
```

Integrate:

```text
∫dy/y = ∫x dx
```

```text
ln|y| = x²/2 + C
```

Convert to exponential form:

```text
y = Ce^(x²/2)
```

### Final answer

```text
y = Ce^(x²/2)
```

---

## 4.6 Extra Example 2

### Question

Solve:

```text
dy/dx = x/y
```

### Solution

Separate:

```text
y dy = x dx
```

Integrate:

```text
∫y dy = ∫x dx
```

```text
y²/2 = x²/2 + C
```

Multiply by 2:

```text
y² = x² + C
```

### Final answer

```text
y² - x² = C
```

---

## 4.7 Extra Example 3

### Question

Solve:

```text
dy/dx = e^x cos y
```

### Solution

Separate:

```text
dy/cos y = e^x dx
```

Since `1/cos y = sec y`:

```text
sec y dy = e^x dx
```

Integrate:

```text
∫sec y dy = ∫e^x dx
```

```text
ln|sec y + tan y| = e^x + C
```

### Final answer

```text
ln|sec y + tan y| = e^x + C
```

---

## 4.8 Extra Example 4

### Question

Solve:

```text
dy/dx = 3x²/y²
```

### Solution

Separate:

```text
y² dy = 3x² dx
```

Integrate:

```text
∫y² dy = ∫3x² dx
```

```text
y³/3 = x³ + C
```

Multiply by 3:

```text
y³ = 3x³ + C
```

### Final answer

```text
y³ = 3x³ + C
```

---

## 4.9 Extra Example 5

### Question

Solve:

```text
dy/dx = (1 + x)(1 + y)
```

### Solution

Separate:

```text
dy/(1+y) = (1+x) dx
```

Integrate:

```text
ln|1+y| = x + x²/2 + C
```

### Final answer

```text
ln|1+y| = x + x²/2 + C
```

or:

```text
1+y = Ce^(x + x²/2)
```

---

# 5. Homogeneous Differential Equations

## 5.1 Basic idea

A first order differential equation is homogeneous if it can be written as:

```text
dy/dx = f(y/x)
```

That means the right side depends only on `y/x`.

---

## 5.2 Main substitution

Use:

```text
y = vx
```

where `v` is a new function of `x`.

Then:

```text
dy/dx = v + x dv/dx
```

After substitution, the equation becomes separable.

---

## 5.3 Tute Example 3.5

### Question

Show that the equation is homogeneous and solve:

```text
(x - y) dy/dx = x + 2y
```

### Solution

Rewrite:

```text
dy/dx = (x + 2y)/(x - y)
```

Divide top and bottom by `x`:

```text
dy/dx = (1 + 2y/x)/(1 - y/x)
```

This depends only on `y/x`, so it is homogeneous.

Let:

```text
y = vx
```

Then:

```text
dy/dx = v + x dv/dx
```

Substitute:

```text
v + x dv/dx = (1 + 2v)/(1 - v)
```

Move `v` to the right:

```text
x dv/dx = (1 + 2v)/(1 - v) - v
```

Simplify:

```text
x dv/dx = (1 + 2v - v + v²)/(1 - v)
```

```text
x dv/dx = (1 + v + v²)/(1 - v)
```

Separate:

```text
(1 - v)/(1 + v + v²) dv = dx/x
```

Integrate:

```text
∫(1 - v)/(v² + v + 1) dv = ∫dx/x
```

For the left side, write:

```text
1 - v = -1/2(2v+1) + 3/2
```

So:

```text
∫(1-v)/(v²+v+1) dv
= -1/2 ln(v²+v+1) + √3 arctan((2v+1)/√3)
```

Therefore:

```text
-1/2 ln(v²+v+1) + √3 arctan((2v+1)/√3) = ln|x| + C
```

Replace:

```text
v = y/x
```

### Final answer

```text
-1/2 ln((y/x)² + y/x + 1) + √3 arctan((2y/x + 1)/√3) = ln|x| + C
```

---

## 5.4 Tute Example 3.6

### Question

Solve:

```text
x cos(y/x) dy/dx = y cos(y/x) + x
```

### Solution

Divide by `x cos(y/x)`:

```text
dy/dx = y/x + sec(y/x)
```

This depends on `y/x`, so it is homogeneous.

Let:

```text
y = vx
```

Then:

```text
dy/dx = v + x dv/dx
```

Substitute:

```text
v + x dv/dx = v + sec v
```

Cancel `v`:

```text
x dv/dx = sec v
```

Separate:

```text
cos v dv = dx/x
```

Integrate:

```text
∫cos v dv = ∫dx/x
```

```text
sin v = ln|x| + C
```

Replace `v = y/x`:

### Final answer

```text
sin(y/x) = ln|x| + C
```

---

## 5.5 Extra Example 1

### Question

Solve:

```text
dy/dx = (x + y)/x
```

### Solution

Rewrite:

```text
dy/dx = 1 + y/x
```

Let:

```text
y = vx
```

Then:

```text
v + x dv/dx = 1 + v
```

Cancel `v`:

```text
x dv/dx = 1
```

```text
dv = dx/x
```

Integrate:

```text
v = ln|x| + C
```

Replace `v = y/x`:

```text
y/x = ln|x| + C
```

### Final answer

```text
y = x(ln|x| + C)
```

---

## 5.6 Extra Example 2

### Question

Solve:

```text
dy/dx = (y - x)/x
```

### Solution

```text
dy/dx = y/x - 1
```

Let `y = vx`:

```text
v + x dv/dx = v - 1
```

Cancel `v`:

```text
x dv/dx = -1
```

```text
dv = -dx/x
```

Integrate:

```text
v = -ln|x| + C
```

Replace `v = y/x`:

### Final answer

```text
y = x(C - ln|x|)
```

---

## 5.7 Extra Example 3

### Question

Solve:

```text
dy/dx = (x² + y²)/(xy)
```

### Solution

Rewrite:

```text
dy/dx = x/y + y/x
```

Let `y = vx`. Then:

```text
x/y = 1/v,     y/x = v
```

So:

```text
v + x dv/dx = 1/v + v
```

Cancel `v`:

```text
x dv/dx = 1/v
```

Separate:

```text
v dv = dx/x
```

Integrate:

```text
v²/2 = ln|x| + C
```

Replace `v = y/x`:

```text
(y/x)² = 2ln|x| + C
```

### Final answer

```text
y²/x² = 2ln|x| + C
```

---

## 5.8 Extra Example 4

### Question

Solve:

```text
dy/dx = (2x + y)/(x)
```

### Solution

```text
dy/dx = 2 + y/x
```

Let `y = vx`:

```text
v + x dv/dx = 2 + v
```

```text
x dv/dx = 2
```

```text
dv = 2 dx/x
```

Integrate:

```text
v = 2ln|x| + C
```

Replace `v = y/x`:

### Final answer

```text
y = x(2ln|x| + C)
```

---

## 5.9 Extra Example 5

### Question

Solve:

```text
dy/dx = (x + 2y)/(2x)
```

### Solution

```text
dy/dx = 1/2 + y/x
```

Let `y = vx`:

```text
v + x dv/dx = 1/2 + v
```

Cancel `v`:

```text
x dv/dx = 1/2
```

```text
dv = (1/2) dx/x
```

Integrate:

```text
v = (1/2)ln|x| + C
```

Replace `v = y/x`:

### Final answer

```text
y = x[(1/2)ln|x| + C]
```

---

# 6. Integrating Factor Method

## 6.1 When to use

Use this for first order linear equations.

Standard form:

```text
dy/dx + P(x)y = Q(x)
```

Important: the coefficient of `dy/dx` must be 1.

---

## 6.2 Formula

Integrating factor:

```text
I.F. = e^(∫P dx)
```

Solution:

```text
y(I.F.) = ∫Q(I.F.) dx + C
```

---

## 6.3 Tute Example 3.7

### Question

Solve:

```text
dy/dx - y = cos x
```

### Solution

Compare with:

```text
dy/dx + Py = Q
```

Here:

```text
P = -1,     Q = cos x
```

Find integrating factor:

```text
I.F. = e^(∫-1 dx) = e^(-x)
```

Use formula:

```text
y e^(-x) = ∫e^(-x)cos x dx + C
```

Using standard integration:

```text
∫e^(-x)cos x dx = e^(-x)(-cos x + sin x)/2
```

So:

```text
y e^(-x) = e^(-x)(-cos x + sin x)/2 + C
```

Multiply by `e^x`:

### Final answer

```text
y = (-cos x + sin x)/2 + Ce^x
```

---

## 6.4 Tute Example 3.8

### Question

Solve:

```text
x dy/dx + 2y = x²,     x ≠ 0
```

### Solution

First divide by `x`:

```text
dy/dx + (2/x)y = x
```

So:

```text
P = 2/x,     Q = x
```

Integrating factor:

```text
I.F. = e^(∫2/x dx)
```

```text
= e^(2ln|x|)
```

```text
= x²
```

Use formula:

```text
yx² = ∫x · x² dx + C
```

```text
yx² = ∫x³ dx + C
```

```text
yx² = x⁴/4 + C
```

Divide by `x²`:

### Final answer

```text
y = x²/4 + C/x²
```

---

## 6.5 Tute Example 3.9

### Question

Solve:

```text
y dx - (x + 2y²) dy = 0
```

### Solution

This equation is easier if we treat `x` as a function of `y`.

Rewrite:

```text
y dx = (x + 2y²) dy
```

Divide by `dy`:

```text
y dx/dy = x + 2y²
```

Divide by `y`:

```text
dx/dy = x/y + 2y
```

Bring `x/y` to left:

```text
dx/dy - (1/y)x = 2y
```

This is linear in `x`.

Compare:

```text
dx/dy + P₁(y)x = Q₁(y)
```

Here:

```text
P₁ = -1/y,     Q₁ = 2y
```

Integrating factor:

```text
I.F. = e^(∫-1/y dy)
```

```text
= e^(-ln|y|)
```

```text
= 1/y
```

Use formula:

```text
x(1/y) = ∫2y(1/y) dy + C
```

```text
x/y = ∫2 dy + C
```

```text
x/y = 2y + C
```

Multiply by `y`:

### Final answer

```text
x = 2y² + Cy
```

---

## 6.6 Extra Example 1

### Question

Solve:

```text
dy/dx + y = e^x
```

### Solution

```text
P = 1,     Q = e^x
```

```text
I.F. = e^(∫1 dx) = e^x
```

```text
ye^x = ∫e^x · e^x dx + C
```

```text
ye^x = ∫e^(2x) dx + C
```

```text
ye^x = e^(2x)/2 + C
```

### Final answer

```text
y = e^x/2 + Ce^(-x)
```

---

## 6.7 Extra Example 2

### Question

Solve:

```text
dy/dx + 2y = 4
```

### Solution

```text
P = 2,     Q = 4
```

```text
I.F. = e^(2x)
```

```text
ye^(2x) = ∫4e^(2x) dx + C
```

```text
ye^(2x) = 2e^(2x) + C
```

### Final answer

```text
y = 2 + Ce^(-2x)
```

---

## 6.8 Extra Example 3

### Question

Solve:

```text
dy/dx + (1/x)y = x²,     x ≠ 0
```

### Solution

```text
P = 1/x,     Q = x²
```

```text
I.F. = e^(∫1/x dx) = x
```

```text
xy = ∫x² · x dx + C
```

```text
xy = ∫x³ dx + C
```

```text
xy = x⁴/4 + C
```

### Final answer

```text
y = x³/4 + C/x
```

---

## 6.9 Extra Example 4

### Question

Solve:

```text
dy/dx - (3/x)y = x⁴
```

### Solution

```text
P = -3/x,     Q = x⁴
```

```text
I.F. = e^(∫-3/x dx) = x^(-3)
```

```text
yx^(-3) = ∫x⁴x^(-3) dx + C
```

```text
y/x³ = ∫x dx + C
```

```text
y/x³ = x²/2 + C
```

### Final answer

```text
y = x⁵/2 + Cx³
```

---

## 6.10 Extra Example 5

### Question

Solve:

```text
dy/dx + 3y = sin x
```

### Solution

```text
P = 3,     Q = sin x
```

```text
I.F. = e^(3x)
```

```text
ye^(3x) = ∫e^(3x) sin x dx + C
```

Use formula:

```text
∫e^(ax)sin bx dx = e^(ax)(a sin bx - b cos bx)/(a²+b²)
```

Here `a=3`, `b=1`:

```text
∫e^(3x)sin x dx = e^(3x)(3sin x - cos x)/10
```

So:

```text
ye^(3x) = e^(3x)(3sin x - cos x)/10 + C
```

### Final answer

```text
y = (3sin x - cos x)/10 + Ce^(-3x)
```

---

# 7. Exact Differential Equations

## 7.1 When to use

Use this method when the equation is in the form:

```text
M(x,y) dx + N(x,y) dy = 0
```

or:

```text
M(x,y) + N(x,y)y' = 0
```

---

## 7.2 Exactness test

The equation is exact if:

```text
∂M/∂y = ∂N/∂x
```

This means:

- differentiate `M` with respect to `y`
- differentiate `N` with respect to `x`
- check if they are equal

---

## 7.3 Main steps

1. Identify `M` and `N`.
2. Check `M_y = N_x`.
3. Integrate `M` with respect to `x`:

```text
ψ = ∫M dx + h(y)
```

4. Differentiate `ψ` with respect to `y`.
5. Set it equal to `N`.
6. Find `h(y)`.
7. Final answer:

```text
ψ(x,y) = C
```

---

## 7.4 Tute Example 3.10

### Question

Solve:

```text
2x + y² + 2xyy' = 0
```

### Solution

Write in differential form:

```text
(2x + y²) dx + (2xy) dy = 0
```

So:

```text
M = 2x + y²
N = 2xy
```

Check exactness:

```text
M_y = 2y
```

```text
N_x = 2y
```

Since `M_y = N_x`, it is exact.

Now integrate `M` with respect to `x`:

```text
ψ = ∫(2x + y²) dx
```

Treat `y` as constant:

```text
ψ = x² + xy² + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = 2xy + h'(y)
```

But:

```text
ψ_y = N = 2xy
```

So:

```text
2xy + h'(y) = 2xy
```

```text
h'(y) = 0
```

Therefore:

```text
h(y) = constant
```

### Final answer

```text
x² + xy² = C
```

---

## 7.5 Tute Example 3.11

### Question

Solve:

```text
(y cos x + 2xe^y) + (sin x + x²e^y - 1)y' = 0
```

### Solution

Write:

```text
M = y cos x + 2xe^y
```

```text
N = sin x + x²e^y - 1
```

Check exactness:

```text
M_y = cos x + 2xe^y
```

```text
N_x = cos x + 2xe^y
```

Exact.

Now integrate `M` with respect to `x`:

```text
ψ = ∫(y cos x + 2xe^y) dx
```

Treat `y` as constant:

```text
ψ = y sin x + x²e^y + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = sin x + x²e^y + h'(y)
```

Set equal to `N`:

```text
sin x + x²e^y + h'(y) = sin x + x²e^y - 1
```

So:

```text
h'(y) = -1
```

Integrate:

```text
h(y) = -y
```

### Final answer

```text
y sin x + x²e^y - y = C
```

---

## 7.6 Tute Example 3.12

### Question

Solve:

```text
(3xy + y²) + (x² + xy)y' = 0
```

### Solution

Write:

```text
M = 3xy + y²
```

```text
N = x² + xy
```

Check exactness:

```text
M_y = 3x + 2y
```

```text
N_x = 2x + y
```

These are not equal.

So this equation is **not exact** directly.

For this tute example, the correct next step depends on whether an integrating factor is expected. In beginner level, just remember:

```text
If M_y ≠ N_x, the equation is not exact by the basic exact method.
```

### Final statement

```text
Not exact directly because 3x + 2y ≠ 2x + y.
```

---

## 7.7 Extra Example 1

### Question

Solve:

```text
(2x + 3y)dx + (3x + 4y)dy = 0
```

### Solution

```text
M = 2x + 3y
N = 3x + 4y
```

Check:

```text
M_y = 3
N_x = 3
```

Exact.

Integrate `M` with respect to `x`:

```text
ψ = ∫(2x + 3y)dx
```

```text
ψ = x² + 3xy + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = 3x + h'(y)
```

Set equal to `N`:

```text
3x + h'(y) = 3x + 4y
```

```text
h'(y) = 4y
```

```text
h(y) = 2y²
```

### Final answer

```text
x² + 3xy + 2y² = C
```

---

## 7.8 Extra Example 2

### Question

Solve:

```text
(3x² + y)dx + (x + 2y)dy = 0
```

### Solution

```text
M = 3x² + y
N = x + 2y
```

Check:

```text
M_y = 1
N_x = 1
```

Exact.

Integrate `M` with respect to `x`:

```text
ψ = ∫(3x² + y)dx
```

```text
ψ = x³ + xy + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = x + h'(y)
```

Set equal to `N`:

```text
x + h'(y) = x + 2y
```

```text
h'(y) = 2y
```

```text
h(y) = y²
```

### Final answer

```text
x³ + xy + y² = C
```

---

## 7.9 Extra Example 3

### Question

Solve:

```text
(y + cos x)dx + (x + 2y)dy = 0
```

### Solution

```text
M = y + cos x
N = x + 2y
```

Check:

```text
M_y = 1
N_x = 1
```

Exact.

Integrate `M` with respect to `x`:

```text
ψ = ∫(y + cos x)dx
```

```text
ψ = xy + sin x + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = x + h'(y)
```

Set equal to `N`:

```text
x + h'(y) = x + 2y
```

```text
h'(y) = 2y
```

```text
h(y) = y²
```

### Final answer

```text
xy + sin x + y² = C
```

---

## 7.10 Extra Example 4

### Question

Solve:

```text
(4x³ + 2xy)dx + (x² + 3y²)dy = 0
```

### Solution

```text
M = 4x³ + 2xy
N = x² + 3y²
```

Check:

```text
M_y = 2x
N_x = 2x
```

Exact.

Integrate `M` with respect to `x`:

```text
ψ = ∫(4x³ + 2xy)dx
```

```text
ψ = x⁴ + x²y + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = x² + h'(y)
```

Set equal to `N`:

```text
x² + h'(y) = x² + 3y²
```

```text
h'(y) = 3y²
```

```text
h(y) = y³
```

### Final answer

```text
x⁴ + x²y + y³ = C
```

---

## 7.11 Extra Example 5

### Question

Solve:

```text
(e^x + y)dx + (x + e^y)dy = 0
```

### Solution

```text
M = e^x + y
N = x + e^y
```

Check:

```text
M_y = 1
N_x = 1
```

Exact.

Integrate `M` with respect to `x`:

```text
ψ = ∫(e^x + y)dx
```

```text
ψ = e^x + xy + h(y)
```

Differentiate with respect to `y`:

```text
ψ_y = x + h'(y)
```

Set equal to `N`:

```text
x + h'(y) = x + e^y
```

```text
h'(y) = e^y
```

```text
h(y) = e^y
```

### Final answer

```text
e^x + xy + e^y = C
```

---

# 8. Method Selection Cheat Sheet

| If equation looks like | Use this method |
|---|---|
| Given family with constants like `y=ax+b` | Formation of differential equation |
| Need to verify a function | Differentiate and substitute |
| Need constants from conditions | Use initial conditions |
| `dy/dx = g(x)h(y)` | Variable separable |
| `dy/dx = f(y/x)` | Homogeneous, use `y=vx` |
| `dy/dx + P(x)y = Q(x)` | Integrating factor |
| `Mdx + Ndy = 0` and `M_y = N_x` | Exact equation |

---

# 9. Common Mistakes to Avoid

## Mistake 1: Not dividing first

Example:

```text
x dy/dx + 2y = x²
```

Before integrating factor, divide by `x`:

```text
dy/dx + (2/x)y = x
```

## Mistake 2: Forgetting `+ C`

Always add constant after integration.

## Mistake 3: Treating `y` incorrectly in exact equations

When integrating `M` with respect to `x`, treat `y` as constant.

Example:

```text
∫xy dx = x²y/2
```

not:

```text
x²y²/2
```

## Mistake 4: Using homogeneous method for every equation

Only use homogeneous method when the equation depends on `y/x`.

## Mistake 5: Not checking exactness

For exact equations, always check:

```text
M_y = N_x
```

before solving.

---

# 10. Mini Practice Set Without Solutions

Try these after studying.

## Formation

1. `y = ax²`
2. `y = ae^(-x)`
3. `y = a sin x + b cos x`

## Variable separable

1. `dy/dx = 2xy`
2. `dy/dx = x²/y`
3. `dy/dx = (1+x)y`

## Homogeneous

1. `dy/dx = 1 + y/x`
2. `dy/dx = y/x - 2`
3. `dy/dx = (x²+y²)/(xy)`

## Integrating factor

1. `dy/dx + y = 1`
2. `dy/dx + (2/x)y = x²`
3. `dy/dx - y = e^x`

## Exact

1. `(2x+y)dx + (x+2y)dy = 0`
2. `(cos x + y)dx + (x+1)dy = 0`
3. `(3x²+2y)dx + (2x+4y)dy = 0`

---

# Final Advice

If you only know differentiation and integration, that is enough to start.

For these topics, the main skill is not difficult theory. The main skill is recognizing the pattern:

```text
What type of equation is this?
```

Then follow the correct steps slowly.

Study one method per day:

1. Formation
2. General/particular solutions
3. Variable separable
4. Homogeneous
5. Integrating factor
6. Exact equations

After that, first order differential equations will feel much easier.

---

# End of Part 1
