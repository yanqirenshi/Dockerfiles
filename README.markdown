# Dockerfiles

## Structures

```
  opensuse/tumbleweed
         |
         +----------------------------------------------+-----------------+
         |                                              |                 |
         V                                              V                 V
  renshi/opensuse                                  renshi/base         renshi/docs
  (Dockerfile.OpenSUSE)                           (Dockerfile.Base)   (Dockerfile.Docs)
         |                                              |
         |                                              |
         +--------------------------+                   V
         |                          |              renshi/dev
         V                          V             (Dockerfile.Dev)
  renshi/common-lisp           renshi/node
  (Dockerfile.Common-Lisp)    (Dockerfile.Node)
         |                          |
         |                          +---------------------+
         |                          |                     |
         |                          V                     V
         |                     renshi/react           renshi/riot
         |                    (Dockerfile.React)     (Dockerfile.Riot)
         |
         |
         V
  renshi/strobolights
  (Dockerfile.Strobolights)
```
