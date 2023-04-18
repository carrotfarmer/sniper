---
title: "Chakra Default Dark Mode Theme Config"
publishDate: "18 Apr 2023"
description: "Override default chakra-ui color theme with dark"
tags: ["chakra-ui", "react", "typescript"]
---

```tsx
import { extendTheme, type ThemeConfig } from "@chakra-ui/react";

const config: ThemeConfig = {
  initialColorMode: "dark",
  useSystemColorMode: false,
};

const theme = extendTheme({ config });

export default theme;
```

