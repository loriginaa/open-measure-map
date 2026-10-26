# OpenMeasureMap

一个不隐藏地图地名标注的开源地图测距示例。使用 MapLibre GL JS 和 OpenFreeMap，无后端、无 API Key、无需安装依赖。

## 功能

- 电脑点击地图添加测量点；手机移动地图准星并点击“添加测量点”
- 保留底图上的道路、地名等标注
- 实时显示折线总长和每段长度（球面 Haversine 近似距离）
- 拖动、撤销、移除和清空测量点
- 切换不同地图样式
- 自动保存当前测量到浏览器、复制包含测量点的分享链接

## 使用

将 `index.html` 放到支持 HTTPS 的静态网站服务器，或者直接打开它测试（部分浏览器对 `file://` 下的 ES modules 有限制，推荐静态服务器）。

可以使用 Python 本地启动：

```sh
python3 -m http.server 8000
```

在浏览器打开 `http://localhost:8000`。

## GitHub Pages 发布

1. 新建公开仓库 `open-measure-map`，并初始化一个 README。
2. 上传 `index.html` 到仓库根目录（可一并上传本项目 README）。
3. 打开仓库 **Settings → Pages**。
4. 选择 **Deploy from a branch**，分支选 **main**，目录选 **/(root)**，点击 **Save**。
5. 在 Pages 设置页等待部署完成并打开站点：`https://你的用户名.github.io/open-measure-map/`。

## 技术与数据来源

- 地图库：[MapLibre GL JS](https://maplibre.org/maplibre-gl-js/)
- 底图服务：[OpenFreeMap](https://openfreemap.org/)
- 地理数据：[OpenStreetMap](https://www.openstreetmap.org/copyright)

数据及底图服务遵守各自许可证和使用政策。WebGL 地图需要联网以加载 JS 和底图；服务可用性取决于网络条件。地图距离为近似地表测地距离，不是导航路程。