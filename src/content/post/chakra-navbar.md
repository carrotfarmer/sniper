---
title: "Chakra-UI Navbar"
publishDate: "16 Apr 2023"
description: "A simple chakra navbar"
tags: ["chakra-ui", "react", "typescript"]
---

```tsx
import {
  Box,
  Flex,
  Button,
  Heading,
  Avatar,
} from "@chakra-ui/react";

import Link from "next/link";

export const Navbar = () => {
  return (
    <Box>
      <Flex bg="blue.400" p={6}>
        <Link href="/">
          <Heading size="xl" color="white">
            rettiwt
          </Heading>
        </Link>
        <Box ml={"auto"}>
            <Button
              colorScheme="twitter"
              onClick={() => signOut()}
              size="lg"
            >
              sign out
            </Button>

            <Avatar ml={4} src={session?.user?.image as string} />
        </Box>
      </Flex>
    </Box>
  );
};
```
