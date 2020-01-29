## numpy

## Pandas

### python 判断数据类型

- 判断数值是否为空用 pd.isna,pd.isnull,np.isnan
- 判断字符串是否为空用 pd.isna,pd.isnull；
- 判断时间是否为空用 pd.isna,pd.isnull,np.isnat
- pd.isna 是pandas0.21版本引入的，能判别最大范围的空值。

https://www.cnblogs.com/wqbin/p/12032073.html



## matplotlib

> 我觉着Basemap是难用的，所以自己也不想用这玩意

### 安装 matplotlib basemap

Brew install proj, geos

- https://downloads.sourceforge.net/project/matplotlib/matplotlib-toolkits/basemap-1.0.7/basemap-1.0.7.tar.gz
- python3 setup.py install
- pip install pyproj==1.9.6
- pip install matplotlib==2.1.0


### 展示问题
```python
from IPython.display import IFrame
def show_html(map, mapName):
    map.save(mapName)
    return IFrame(src=mapName, width=980, height=600)
```
```python
from IPython.core.display import HTML
HTML('<a href="">link</a>')

%%html
<a href="http://example.com">link</a>
```



## foilum

### 底图源问题

```python
import folium

map = folium.Map(
       location=[39.90, 116.40],
       zoom_start=12,
       height=400,
       width=800,
       tiles='http://webrd01.is.autonavi.com/appmaptile?lang=zh_cn&size=1&scale=1&style=8&x={x}&y={y}&z={z}',
       attr="高德地图")

map
```