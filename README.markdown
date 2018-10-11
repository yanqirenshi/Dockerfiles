# Dockerfiles

| Directory                     | Description | from                          |
|-------------------------------|-------------|-------------------------------|
| opensuse-tumbleweed           |             | opensuse/tumbleweed           |
| opensuse-tumbleweed-cl-user   |             | opensuse-tumbleweed           |
| opensuse-tumbleweed-linuxbrew |             | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-rbenv     |             | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-nodebrew  |             | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-roswell   |             | opensuse-tumbleweed-linuxbrew |
| ahan-whun-shugoi              |             | opensuse-tumbleweed-roswell   |
| jira                          |             | opensuse-tumbleweed-roswell   |
| nobit@                        |             | opensuse-tumbleweed-roswell   |
| qupool                        |             | opensuse-tumbleweed-roswell   |
| ter                           |             | opensuse-tumbleweed-roswell   |


## Images Stack

```
+-----------+ +-------+ +----------+
| roswell   | |       | |          |
+-----------+ |       | |          |
+-----------+ |       | |          |
| linuxbrew | | rbenv | | nodebrew |
+-----------+ +-------+ +----------+
+----------------------------------+
| cl-user                          |
+----------------------------------+
+----------------------------------+
| opensuse-tumbleweed              |
+----------------------------------+
```
