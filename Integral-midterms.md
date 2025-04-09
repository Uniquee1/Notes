# PROBLEM SET DEFINITE INTEGRAL

Solutions for each definite integral, showing both the antiderivative and definite integral evaluation.

## Problem 1: $\int_0^5 \sqrt{x} - 2 \, dx$

First, split the integral:
$\int_0^5 \sqrt{x} - 2 \, dx = \int_0^5 \sqrt{x} \, dx - \int_0^5 2 \, dx$

Find the antiderivative of $\sqrt{x}$:
$\int \sqrt{x} \, dx = \int x^{1/2} \, dx = \frac{x^{3/2}}{3/2} = \frac{2}{3}x^{3/2}$

For the constant term:
$\int 2 \, dx = 2x$

Therefore, the antiderivative is:
$F(x) = \frac{2}{3}x^{3/2} - 2x$

Evaluating the definite integral:
$\int_0^5 \sqrt{x} - 2 \, dx = \left[ \frac{2}{3}x^{3/2} - 2x \right]_0^5$
$= \left( \frac{2}{3} \cdot 5^{3/2} - 2 \cdot 5 \right) - \left( \frac{2}{3} \cdot 0^{3/2} - 2 \cdot 0 \right)$
$= \frac{2}{3} \cdot 5^{3/2} - 10 - 0$
$= \frac{2}{3} \cdot 5 \sqrt{5} - 10$
$= \frac{2 \cdot 5 \sqrt{5}}{3} - 10$
$= \frac{10\sqrt{5}}{3} - 10$
$= \frac{10\sqrt{5} - 30}{3}$
$= \frac{10\sqrt{5} - 30}{3}$

## Problem 2: $\int_1^3 \frac{2x + 3x^2}{x} \, dx$

First, simplify the integrand:
$\frac{2x + 3x^2}{x} = \frac{2x}{x} + \frac{3x^2}{x} = 2 + 3x$

Find the antiderivative:
$\int (2 + 3x) \, dx = 2x + \frac{3x^2}{2}$

Therefore, the antiderivative is:
$F(x) = 2x + \frac{3x^2}{2}$

Evaluating the definite integral:
$\int_1^3 \frac{2x + 3x^2}{x} \, dx = \left[ 2x + \frac{3x^2}{2} \right]_1^3$
$= \left( 2 \cdot 3 + \frac{3 \cdot 3^2}{2} \right) - \left( 2 \cdot 1 + \frac{3 \cdot 1^2}{2} \right)$
$= \left( 6 + \frac{3 \cdot 9}{2} \right) - \left( 2 + \frac{3}{2} \right)$
$= \left( 6 + \frac{27}{2} \right) - \left( 2 + \frac{3}{2} \right)$
$= \left( 6 + \frac{27}{2} \right) - \frac{4 + 3}{2}$
$= \left( 6 + \frac{27}{2} \right) - \frac{7}{2}$
$= 6 + \frac{27}{2} - \frac{7}{2}$
$= 6 + \frac{27 - 7}{2}$
$= 6 + \frac{20}{2}$
$= 6 + 10$
$= 16$

## Problem 3: $\int_0^{\pi/2} 2\sin 2x \, dx$

Find the antiderivative:
$\int 2\sin 2x \, dx$

Use substitution: let $u = 2x$, then $du = 2dx$, or $dx = \frac{du}{2}$

$\int 2\sin 2x \, dx = \int 2\sin u \cdot \frac{du}{2} = \int \sin u \, du = -\cos u + C = -\cos 2x + C$

Therefore, the antiderivative is:
$F(x) = -\cos 2x$

Evaluating the definite integral:
$\int_0^{\pi/2} 2\sin 2x \, dx = \left[ -\cos 2x \right]_0^{\pi/2}$
$= (-\cos 2 \cdot \frac{\pi}{2}) - (-\cos 2 \cdot 0)$
$= (-\cos \pi) - (-\cos 0)$
$= (-(-1)) - (-1)$
$= 1 + 1$
$= 2$

## Problem 4: $\int_1^e \frac{x+1}{x} \, dx$

First, simplify the integrand:
$\frac{x+1}{x} = \frac{x}{x} + \frac{1}{x} = 1 + \frac{1}{x}$

Find the antiderivative:
$\int \left( 1 + \frac{1}{x} \right) \, dx = x + \ln|x| + C$

Therefore, the antiderivative is:
$F(x) = x + \ln|x|$

Evaluating the definite integral:
$\int_1^e \frac{x+1}{x} \, dx = \left[ x + \ln|x| \right]_1^e$
$= (e + \ln|e|) - (1 + \ln|1|)$
$= (e + 1) - (1 + 0)$
$= e + 1 - 1$
$= e$

## Problem 5: $\int_{-1}^1 e^{2x+1} \, dx$

Find the antiderivative:
$\int e^{2x+1} \, dx$

Note that $e^{2x+1} = e^1 \cdot e^{2x} = e \cdot e^{2x}$

$\int e \cdot e^{2x} \, dx = e \int e^{2x} \, dx$

Use substitution: let $u = 2x$, then $du = 2dx$, or $dx = \frac{du}{2}$

$e \int e^{2x} \, dx = e \int e^u \cdot \frac{du}{2} = \frac{e}{2} \int e^u \, du = \frac{e}{2} e^u + C = \frac{e}{2} e^{2x} + C$

Therefore, the antiderivative is:
$F(x) = \frac{e}{2} e^{2x}$

Evaluating the definite integral:
$\int_{-1}^1 e^{2x+1} \, dx = \left[ \frac{e}{2} e^{2x} \right]_{-1}^1$
$= \frac{e}{2} (e^{2 \cdot 1} - e^{2 \cdot (-1)})$
$= \frac{e}{2} (e^2 - e^{-2})$
$= \frac{e}{2} \cdot \frac{e^4 - 1}{e^2}$
$= \frac{e}{2} \cdot \frac{e^4 - 1}{e^2}$
$= \frac{e}{2} \cdot \frac{e^4 - 1}{e^2}$
$= \frac{e(e^4 - 1)}{2e^2}$
$= \frac{e^3 - e^{-1}}{2}$
$= \frac{e^3 - \frac{1}{e}}{2}$
$= \frac{e^4 - 1}{2e}$

## Problem 6: $\int_0^{\pi/2} \cos^2 x \, dx$

For this integral, we can use the identity $\cos^2 x = \frac{1 + \cos 2x}{2}$

$\int \cos^2 x \, dx = \int \frac{1 + \cos 2x}{2} \, dx = \frac{1}{2} \int (1 + \cos 2x) \, dx = \frac{1}{2} \left( x + \frac{\sin 2x}{2} \right) + C$
$= \frac{x}{2} + \frac{\sin 2x}{4} + C$

Therefore, the antiderivative is:
$F(x) = \frac{x}{2} + \frac{\sin 2x}{4}$

Evaluating the definite integral:
$\int_0^{\pi/2} \cos^2 x \, dx = \left[ \frac{x}{2} + \frac{\sin 2x}{4} \right]_0^{\pi/2}$
$= \left( \frac{\pi/2}{2} + \frac{\sin 2 \cdot \pi/2}{4} \right) - \left( \frac{0}{2} + \frac{\sin 2 \cdot 0}{4} \right)$
$= \left( \frac{\pi}{4} + \frac{\sin \pi}{4} \right) - \left( 0 + 0 \right)$
$= \frac{\pi}{4} + \frac{0}{4}$
$= \frac{\pi}{4}$

## Problem 7: $\int_0^{\pi/4} \frac{1}{\cos^2 2x} \, dx$

Note that $\frac{1}{\cos^2 2x} = \sec^2 2x$

Using the identity $\int \sec^2 u \, du = \tan u + C$

Let $u = 2x$, then $du = 2dx$, or $dx = \frac{du}{2}$

$\int \frac{1}{\cos^2 2x} \, dx = \int \sec^2 2x \, dx = \int \sec^2 u \cdot \frac{du}{2} = \frac{1}{2} \int \sec^2 u \, du = \frac{1}{2} \tan u + C = \frac{1}{2} \tan 2x + C$

Therefore, the antiderivative is:
$F(x) = \frac{1}{2} \tan 2x$

Evaluating the definite integral:
$\int_0^{\pi/4} \frac{1}{\cos^2 2x} \, dx = \left[ \frac{1}{2} \tan 2x \right]_0^{\pi/4}$
$= \frac{1}{2} (\tan 2 \cdot \pi/4 - \tan 2 \cdot 0)$
$= \frac{1}{2} (\tan \pi/2 - \tan 0)$
$= \frac{1}{2} (\infty - 0)$

Note: Since $\tan(\frac{\pi}{2})$ is undefined (approaches infinity), we need to be careful. This integral actually diverges, but if we evaluate the limit as we approach $\frac{\pi}{4}$ from below, we get:
$\lim_{t \to \pi/4^-} \int_0^t \frac{1}{\cos^2 2x} \, dx = \frac{1}{2} \lim_{t \to \pi/4^-} \tan 2t = \infty$

Therefore, this improper integral diverges.

## Problem 8: $\int_0^{\pi/4} \tan^2 2x \, dx$

We can use the identity $\tan^2 x = \sec^2 x - 1$

$\int \tan^2 2x \, dx = \int (\sec^2 2x - 1) \, dx$

Let $u = 2x$, then $du = 2dx$, or $dx = \frac{du}{2}$

$\int (\sec^2 2x - 1) \, dx = \int \sec^2 u \cdot \frac{du}{2} - \int 1 \cdot \frac{du}{2}$
$= \frac{1}{2} \int \sec^2 u \, du - \frac{1}{2} \int 1 \, du$
$= \frac{1}{2} \tan u - \frac{1}{2} u + C$
$= \frac{1}{2} \tan 2x - \frac{1}{2} \cdot 2x + C$
$= \frac{1}{2} \tan 2x - x + C$

Therefore, the antiderivative is:
$F(x) = \frac{1}{2} \tan 2x - x$

Evaluating the definite integral:
$\int_0^{\pi/4} \tan^2 2x \, dx = \left[ \frac{1}{2} \tan 2x - x \right]_0^{\pi/4}$
$= \left( \frac{1}{2} \tan 2 \cdot \pi/4 - \pi/4 \right) - \left( \frac{1}{2} \tan 2 \cdot 0 - 0 \right)$
$= \left( \frac{1}{2} \tan \pi/2 - \pi/4 \right) - (0 - 0)$

Again, $\tan(\frac{\pi}{2})$ is undefined, so we need to take the limit as $x$ approaches $\frac{\pi}{4}$ from below. This integral also diverges.

## Problem 9: $\int_0^{\pi} \sin^2 \frac{1}{2}x \, dx$

Using the identity $\sin^2 \frac{x}{2} = \frac{1 - \cos x}{2}$

$\int \sin^2 \frac{1}{2}x \, dx = \int \frac{1 - \cos x}{2} \, dx = \frac{1}{2} \int (1 - \cos x) \, dx = \frac{1}{2} (x - \sin x) + C$

Therefore, the antiderivative is:
$F(x) = \frac{1}{2} (x - \sin x)$

Evaluating the definite integral:
$\int_0^{\pi} \sin^2 \frac{1}{2}x \, dx = \left[ \frac{1}{2} (x - \sin x) \right]_0^{\pi}$
$= \frac{1}{2} [(\pi - \sin \pi) - (0 - \sin 0)]$
$= \frac{1}{2} [(\pi - 0) - (0 - 0)]$
$= \frac{1}{2} \pi$
$= \frac{\pi}{2}$

## Problem 10: $\int_{-2}^2 2\sin^2 x + 2\cos^2 x \, dx$

Simplify the integrand:
$2\sin^2 x + 2\cos^2 x = 2(\sin^2 x + \cos^2 x) = 2 \cdot 1 = 2$

Find the antiderivative:
$\int 2 \, dx = 2x + C$

Therefore, the antiderivative is:
$F(x) = 2x$

Evaluating the definite integral:
$\int_{-2}^2 2\sin^2 x + 2\cos^2 x \, dx = \left[ 2x \right]_{-2}^2$
$= 2 \cdot 2 - 2 \cdot (-2)$
$= 4 - (-4)$
$= 4 + 4$
$= 8$

## Problem 11: $\int_0^{\pi/2} \cos^3 x \, dx$

We can use the identity $\cos^3 x = \cos^2 x \cdot \cos x = (1-\sin^2 x) \cdot \cos x$

$\int \cos^3 x \, dx = \int (1-\sin^2 x) \cdot \cos x \, dx$

Let $u = \sin x$, then $du = \cos x \, dx$

$\int (1-\sin^2 x) \cdot \cos x \, dx = \int (1-u^2) \, du = \int (1-u^2) \, du = u - \frac{u^3}{3} + C = \sin x - \frac{\sin^3 x}{3} + C$

Therefore, the antiderivative is:
$F(x) = \sin x - \frac{\sin^3 x}{3}$

Evaluating the definite integral:
$\int_0^{\pi/2} \cos^3 x \, dx = \left[ \sin x - \frac{\sin^3 x}{3} \right]_0^{\pi/2}$
$= \left( \sin \frac{\pi}{2} - \frac{\sin^3 \frac{\pi}{2}}{3} \right) - \left( \sin 0 - \frac{\sin^3 0}{3} \right)$
$= \left( 1 - \frac{1^3}{3} \right) - \left( 0 - \frac{0^3}{3} \right)$
$= \left( 1 - \frac{1}{3} \right) - 0$
$= \frac{3}{3} - \frac{1}{3}$
$= \frac{2}{3}$

## Problem 12: $\int_0^{\pi/4} \tan^3 x \, dx$

We can rewrite this as:
$\int \tan^3 x \, dx = \int \tan^2 x \cdot \tan x \, dx = \int (\sec^2 x - 1) \cdot \tan x \, dx$

$\int \tan^3 x \, dx = \int \sec^2 x \cdot \tan x \, dx - \int \tan x \, dx$

For the first part:
Let $u = \tan x$, then $du = \sec^2 x \, dx$, which means $\sec^2 x \, dx = du$

$\int \sec^2 x \cdot \tan x \, dx = \int u \, du = \frac{u^2}{2} + C_1 = \frac{\tan^2 x}{2} + C_1$

For the second part:
$\int \tan x \, dx = \ln|\sec x| + C_2$

Therefore, the antiderivative is:
$F(x) = \frac{\tan^2 x}{2} - \ln|\sec x|$

Evaluating the definite integral:
$\int_0^{\pi/4} \tan^3 x \, dx = \left[ \frac{\tan^2 x}{2} - \ln|\sec x| \right]_0^{\pi/4}$
$= \left( \frac{\tan^2 \frac{\pi}{4}}{2} - \ln|\sec \frac{\pi}{4}| \right) - \left( \frac{\tan^2 0}{2} - \ln|\sec 0| \right)$
$= \left( \frac{1^2}{2} - \ln|\sqrt{2}| \right) - \left( \frac{0^2}{2} - \ln|1| \right)$
$= \left( \frac{1}{2} - \ln\sqrt{2} \right) - (0 - 0)$
$= \frac{1}{2} - \frac{1}{2}\ln 2$
$= \frac{1}{2}(1 - \ln 2)$
