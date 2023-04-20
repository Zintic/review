# yaml

yaml是一个文本管理工具，使用该工具能实现参数，配置的管理

## 基本语法

- 对大小写敏感
- 使用缩进管理上下级
- 冒号在使用时作为一个字典

支持的数据类型
- 对象，字典
- 数组
- 纯量： 不可再分的值，如bool值，整数，时间

```yaml

# 键值对
- key1: value1
- key2: value2
...


# 数组
- ...
- ... 


# 纯量
xx: True    
```

## 安装
在Python中，需要安装pyyaml包
```bash
pip install pyyaml  
```

## 使用

python中
```python

# notes: 读入的yaml是字典形式，需要以key索引
import yaml
yaml_path = '...'

with open(yaml_path) as rf:
    yml_conf = yaml.safe_load(rf)
```

```python
# 如果需要将yaml转为类属性，方法如下：
class LoadConfig(object):
    def __init__(self, cfg_path='config\cfg.yaml'):
        with open(cfg_path) as f:
            yml_conf = yaml.safe_load(f)
            
            assert yml_conf['model_dir'], 'model_dir not exists!'
            self.__dict__.update(**yml_conf)
```
