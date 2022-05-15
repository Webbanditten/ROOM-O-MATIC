---
layout: default
title: How to edit default motto and console motto
parent: Kepler
has_children: false
nav_order: 1
---
# How to edit default motto and console motto

To edit the default motto you can execute the following SQL Command.

![](../assets/images/motto.png)

```sql 
ALTER TABLE users
ALTER motto SET DEFAULT 'New value here';
```

To edit the default console motto you can execute the following SQL Command.

![](../assets/images/console_motto.png)

```sql 
ALTER TABLE users
ALTER console_motto SET DEFAULT 'New value here';
```
