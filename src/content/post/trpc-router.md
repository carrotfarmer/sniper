---
title: "tRPC Router"
publishDate: "18 Apr 2023"
description: "An example router"
tags: ["trpc", "t3", "typescript"]
---

```tsx
import { z } from "zod";

import { createTRPCRouter, publicProcedure } from "~/server/api/trpc";

export const exampleRouter = createTRPCRouter({
  hello: publicProcedure
    .input(z.object({ text: z.string() }))
    .query(({ input }) => {
      return {
        greeting: `Hello ${input.text}`,
      };
    }),
});
```
