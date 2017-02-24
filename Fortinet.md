# Fortinet Cheatsheet

# Zu Cluster-Member verbinden
Cluster-Member heraussuchen mit ``get system ha status``. Dann ist die Ausgabe beispielsweise:
```
Master:200   FGT400-8           FGT4002801021111  1
Slave :128   FGT400-3           FGT4002803032222  0
```

Wichtig ist die Nummer ganz hinten. Möchte man auf den Slave verbinden
```
execute ha manage 0
```

# Cluster Config-Checksum herausfinden
```
di sys ha cluster-csum
```

Dann die Differenzen mit ``diagnose system ha showsum <level>`` herausfinden.

# Cluster Config-Checksum neu berechnen
```
diag sys ha csum-recalculate
```
