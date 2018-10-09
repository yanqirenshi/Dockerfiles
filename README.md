# Dockerfiles

| Directory                       | Description |
|---------------------------------|-------------|
| opensuse-tumbleweed             |             |
| opensuse-tumbleweed-cl-user     |             |
| opensuse-tumbleweed-common-lisp |             |
| opensuse-tumbleweed-linuxbrew   |             |
| opensuse-tumbleweed-rbenv       |             |
| opensuse-tumbleweed-roswell     |             |


## Images Stack

```
+-----------+ +-------+
| roswell   | |       |
+-----------+ |       |
+-----------+ |       |
| linuxbrew | | rbenv |
+-----------+ +-------+
+---------------------+
| cl-user             |
+---------------------+
+---------------------+
| opensuse-tumbleweed |
+---------------------+
```
