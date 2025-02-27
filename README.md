# image_process_web
### 一、技术栈选择

- **后端框架**：Flask（轻量、易上手，适合小型 Web 应用）
- **前端**：HTML+CSS+JavaScript（原生开发，减少依赖）
- **图像处理模型**：图像去雾，图像去雨，图像增强
- **图像处理**：OpenCV（图像读取、处理、保存）

### 二、项目结构

```plaintext
image_process_web/
├── app.py               # 后端主程序（路由+任务调度）
├── static/
│   ├── css/style.css    # 页面样式
│   ├── js/script.js     # 前端交互（动态加载模型选项）
│   ├── uploads/         # 上传原图
│   └── results/         # 处理结果图
├── templates/index.html # 主页面（任务选择+模型选择）
├── models/              # 存放训练好的模型（按任务分类）
│   ├── defog/           # 去雾模型（如defog_model1.pth, defog_model2.pth）
│   ├── derain/          # 去雨模型
│   └── enhance/         # 增强模型
├── process/             # 模型处理逻辑（按任务分模块）
│   ├── base.py          # 基础处理类
│   ├── defog.py         # 去雾处理（调用对应模型）
│   ├── derain.py        # 去雨处理
│   └── enhance.py       # 增强处理
└── networks/             # 模型处理逻辑（按任务分模块）
    ├── BFFDNet.py       # 去雾网络1
    ├── PUCCNet.py       # 去雾网络2
    ├── rainNet.py          # 去雨网络
    └── enhanceNet.py       # 增强网络
```

### 三、核心代码实现

#### 1. 去雾网络（networks/defog/dehaze.py）

#### 2. 后端服务（app.py）

#### 3. 前端页面（templates/index.html）

#### 4. 前端样式（static/css/style.css）

#### 5. 前端交互（static/js/script.js）

### 四、使用方法

1. **安装依赖**：

   ```bash
   pip install flask opencv-python numpy torch
   ```

2. **运行程序**：

   ```bash
   python app.py
   ```

3. **访问网站**：打开浏览器，输入 `http://127.0.0.1:5000`，即可看到上传界面。