---
layout: post
title: "Mysql query from binary to uuid"
date: 2015-11-17 15:40:44 -0500
categories: mysql 
---


<h3>From binary to uuid</h3>

{% highlight ruby %}
SELECT
  LOWER(
    CONCAT(
      LEFT(HEX(binary_field), 8),
      '-',
      MID(HEX(binary_field), 9, 4),
      '-',
      MID(HEX(binary_field), 13, 4),
      '-',
      MID(HEX(binary_field), 17, 4),
      '-',
      RIGHT(HEX(binary_field), 12)
    )
  ) AS uuid
FROM some_table
{% endhighlight%}
