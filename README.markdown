# Dockerfiles

| Directory                     | from                          |
|-------------------------------|-------------------------------|
| ahan-whun-shugoi              | opensuse-tumbleweed-slime     |
| jira                          | opensuse-tumbleweed-slime     |
| nobit@                        | opensuse-tumbleweed-slime     |
| qupool                        | opensuse-tumbleweed-slime     |
| ter                           | opensuse-tumbleweed-slime     |
| opensuse-tumbleweed-slime     | opensuse-tumbleweed-roswell   |
| opensuse-tumbleweed-roswell   | opensuse-tumbleweed-linuxbrew |
| opensuse-tumbleweed-emacs     | opensuse-tumbleweed-cl-git    |
| opensuse-tumbleweed-git       | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-linuxbrew | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-rbenv     | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-nodebrew  | opensuse-tumbleweed-cl-user   |
| opensuse-tumbleweed-nginx     | opensuse-tumbleweed           |
| opensuse-tumbleweed-cl-user   | opensuse-tumbleweed           |
| opensuse-tumbleweed           | opensuse/tumbleweed           |


## Images Stack

```
+-----------------------+ +-------+ +----------+ +-------+
| slime                 | |       | |          | |       |
+-----------------------+ |       | |          | |       |
+---------+ +-----------+ |       | |          | |       |
| emacs   | | roswell   | |       | |          | |       |
+---------+ +-----------+ |       | |          | |       |
+---------+ +-----------+ |       | |          | |       |
| git     | | linuxbrew | | rbenv | | nodebrew | |       |
+---------+ +-----------+ +-------+ +----------+ |       |
+----------------------------------------------+ |       |
| cl-user                                      | | nginx |
+----------------------------------------------+ +-------+
+--------------------------------------------------------+
| opensuse-tumbleweed                                    |
+--------------------------------------------------------+
```
