---
title: "Framer Motion Hover"
publishDate: "18 Apr 2023"
description: "A simple hover animation"
tags: ["framer-motion", "react", "typescript"]
---

```tsx
import { motion } from "framer-motion"

<motion.div
  whileTap={{
    scale: 0.95,
  }}
  whileHover={{
    scale: 1.05
  }}
>
  <div>thingy to hover</div> 
</motion.div>
```
