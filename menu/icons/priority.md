---
description: ลำดับความสำคัญของไอคอนที่มีเงื่อนไข
---

# Priority

## ตัวอย่าง

```yaml
priority: 20
```

## หมายเหตุ

* This property is only available on conditionnal icons
* **If not set, the priority will be -1**
* When checking for conditions, the conditionnal icons will be checked by their priority starting from the one with the highest number

{% hint style="info" %}
If an icon has only 1 conditionnal icon, the priority is not required
{% endhint %}

