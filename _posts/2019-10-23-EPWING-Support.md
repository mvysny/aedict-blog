---
layout: post
title: EPWING Support
---

Several users has been asking to add support for EPWING-based dictionaries such as
Daijisen 大辞泉, 日本史辞典 or Kojien 広辞苑 to Aedict.

The only EPWING dictionary currently supported by Aedict is Daijirin 大辞林;
please see [Daijirin 大辞泉](../Daijirin/) for more details on how to download it
to your Aedict.

Unfortunately no other EPWING dictionary support is planned. The reason for that is
that EPWING is a horrible old binary database file format. The format only supports
(weak) searching via an old C library; the possibility to get the data to Aedict index
is very limited. What's even worse, every EPWING dictionary uses its own separate
format, which makes it impossible to create one tool which extracts data from EPWING.

However, if you manage to get the data out of the EPWING dictionary into JMDict format,
just let me know at martin@vysny.me and I will happily add the dictionary into Aedict.
Since the dictionaries are commercial, the dictionaries will only be available for users
which provide a proof-of-purchase. See [Daijirin 大辞泉](../Daijirin/) for more details.

I've used the [NOJ Dumpers Docker port](https://github.com/mvysny/noj_dumpers_docker)
to extract data from Daijirin - maybe the tool could prove useful to extract data
from other EPWING-based dictionaries as well.
