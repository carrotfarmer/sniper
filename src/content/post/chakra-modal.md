---
title: "Chakra-UI Modal"
publishDate: "16 Apr 2023"
description: "chakra modal"
tags: ["chakra-ui", "react", "typescript"]
---

```tsx
import {
  Modal,
  ModalOverlay,
  ModalContent,
  ModalHeader,
  ModalCloseButton,
  ModalBody,
  ModalFooter,
  Button,
  Text,
  IconButton,
  useDisclosure
} from "@chakra-ui/react";
import React from "react";

interface ModalProps {}

export const TweetModal: React.FC<TweetModalProps> = () => {
  const { isOpen, onClose, onOpen } = useDisclosure();
  
  return (
    <Modal isOpen={isOpen} onClose={onClose}>
      <ModalOverlay />
      <ModalContent>
        <ModalHeader>Title</ModalHeader>
        <ModalCloseButton />
        <ModalBody>
          <Text>Modal Body</Text>
        </ModalBody>

        <ModalFooter>
          <Button variant="ghost" colorScheme="twitter" onClick={onClose}>
            Close
          </Button>
        </ModalFooter>
      </ModalContent>
    </Modal>
  );
};
```
