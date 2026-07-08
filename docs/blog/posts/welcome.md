---
date: 2026-07-09
categories:
  - General
tags:
  - meta
---

# Welcome to my site

This is the first post on my new research site. I'll use this space to write about
what I'm working on, papers worth reading, and techniques I'm figuring out.

<!-- more -->

## Why a blog?

Research is more than the polished paper at the end. A lot of the useful thinking —
the failed experiments, the "why does this peak shift?" moments, the small scripts
that save an afternoon — never makes it into a publication. This is where some of
that will live.

## What to expect

- Short write-ups of methods and characterization results
- Reading notes on papers in **[your area]**
- Occasional deeper posts on a problem I'm stuck on or excited about

Here's what the formatting looks like, so you know what tools you have when writing.

### Code

```python
import numpy as np

# Bragg's law: nλ = 2d·sinθ  →  solve for d-spacing
def d_spacing(theta_deg, wavelength=1.5406, n=1):
    theta = np.radians(theta_deg)
    return n * wavelength / (2 * np.sin(theta))

print(f"d = {d_spacing(28.4):.3f} Å")
```

### Math

Inline math like $E = h\nu$ works, and so do display equations:

$$
\sigma = \frac{F}{A}, \qquad \varepsilon = \frac{\Delta L}{L_0}
$$

### Callouts

!!! note "Tip"
    Anything in a `!!! note` block renders as one of these highlighted boxes —
    handy for caveats, definitions, or key takeaways.

That's it for now. More soon.
