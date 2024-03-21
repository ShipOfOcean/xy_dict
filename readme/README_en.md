# xy_dict

- zh_CN [简体中文](README_zh_CN.md)
- zh_TW [繁体中文](README_zh_TW.md)
- en [English](README_en.md)

## Description
Dict tools.


## 安装

```bash
pip install xy_dict
```

## How to use


```python

from xy_dict.utils import is_empty_dict, dict_get

object_map_0 = {}
is_empty_dict(object_map_0)
# True

object_map_1 = {"key_0":"object_0"}
is_empty_dict(object_map_1)
# False

dict_get(object_map_1, "key_0")
# object_0

dict_get(object_map_0, "key_0")
# None

from xy_dict.Dict import Dict

object_map_2 = {"key_0":"object_0", "key_1":{"key_2":"object_2"}, "key_3":["object_3"]}
object_dict = Dict(object_map_2)

object_dict.search_k("key_0")
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_k("key_1")
object_dict.key_map
# {'key_1': {'key_2': 'object_2'}}

object_dict.search_v("object_0")
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_v({"key_2":"object_2"})
object_dict.key_map
# {'key_1': {'key_2': 'object_2'}}

object_dict.search_kv('key_0', 'object_0')
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_kv('key_0', 'object_0')
object_dict.key_map
# {'key_0': 'object_0'}

object_dict.search_kv('key_0', 'object_01')
object_dict.key_map
# {}

```


## Donate
If you think these tools are pretty good, Can you please have a cup of coffee?
<br />
![WeChat](WeChat.png)
![Alipay](Alipay.png)

## Contact


```
Wechat: yuyangitt
Mail: 845262968@qq.com
```