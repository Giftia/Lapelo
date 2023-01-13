# Lapelo
 一个简单的随机图片web服务端，随机返回一张程序所在目录下的图片，可用于在线随机壁纸服务。
 无联网权限，绿色无污染，可以作为随机壁纸站的备选方案。
 由于可执行文件使用 pkg 打包，内置了 nodejs 环境，所以体积有点大。之后会使用 Deno 来改进体积大小，但会需要联网权限。

### Lapelo 是世界语中的 `水手裙的衣襟` 的意思。

## 使用方法
1. 在 [releases](https://github.com/Giftia/Lapelo/releases) 获取最新的发行包，下载到本地并解压，应当只有一个 `lapelo.exe` 可执行文件。
2. 将程序 `lapelo.exe` 放置于图片所在文件夹，运行程序。程序会以默认配置启动。
3. 访问 [http://127.0.0.1:23333](http://127.0.0.1:23333) 即可获取一张随机图片。

## 配置文件
 程序运行时会在程序所在目录下生成 `config.json` 配置文件，可通过修改配置文件来修改程序行为。

### 配置项
| 配置项 | 默认值  | 说明         |
| ------ | ------- | ------------ |
| `code` | `777`   | 图片返回模式 |
| `port` | `23333` | 服务端口     |

### code
| code        | 说明                                                                                                                                                                                                              |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `777`       | 默认模式，图片将以直链原图形式返回，适合做随机壁纸使用。例如：在 Obsidian 的主题 `Blue Topaz` 中设置在线随机壁纸时，在 `Custom Theme Dark (url)` 中填写 `url("http://127.0.0.1:23333/")` 即可使用 Lapelo 随机壁纸 |
| `THE_BEAST` | 图片将以 base64 编码形式显示在 img 标签中，避免跨域问题，适合嵌入你自己的网站做随机图背景                                                                                                                         |

### port
 随机图片服务运行端口，如果图方便不想在访问时候加端口，可以改成 `80`。

## 为啥要做这个
 一直在用的 [iw233随机壁纸服务](https://dev.iw233.cn/API/index.php) 挂了，我的 Obsidian 就用不了随机壁纸了，所以就自己糊了个用。
