---
title: "a fancy chakra-ui button"
publishDate: "18 Apr 2023"
description: "literally a fancy button"
tags: ["chakra-ui", "framer-motion", "react", "typescript"]
---

```tsx
<Box>
  <Flex justifyContent="center" alignItems="center">
    <motion.button
      whileTap={{
        scale: 0.95,
      }}
      whileHover={{
        scale: 1.05
      }}
    >
      <Button
        flex={1}
        px={4}
        fontSize={"sm"}
        rounded={"xl"}
        bg={"blue.500"}
        color={"white"}
        boxShadow={
          "0px 1px 25px -5px rgb(66 153 225 / 48%), 0 10px 10px -5px rgb(69 159 235 / 43%)"
        }
        _hover={{
          bg: "blue.600",
        }}
        _focus={{
          bg: "blue.600",
        }}
        onClick={onOpen}
      >
        omg fancy button
      </Button>
    </motion.button>
  </Flex>
</Box>
```
