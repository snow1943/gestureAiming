# 🎮 Gesture Aiming - 赛博朋克手势粒子系统

一个基于Three.js和MediaPipe Hands的交互式粒子系统，通过手势控制12,000个霓虹粒子形成文字和3D效果。

## ✨ 特性

- 🌟 **12,000个发光粒子** - AdditiveBlending霓虹效果
- 👋 **双手手势识别** - MediaPipe Hands实时追踪
- 🎨 **赛博朋克风格** - 移动网格、扫描线、暗角效果
- 📊 **实时HUD显示** - FPS、粒子数、手势状态
- 🎯 **多种交互模式** - 文字变换、物理散射、星云模式、3D篮球

## 🎮 交互说明

### 左手（形状控制器）
- **1个手指** → "Hello" | 霓虹蓝
- **2个手指** → "我是Aiming" | 霓虹黄
- **3个手指** → "太有用了" | 霓虹粉
- **4个手指** → "再见" | 霓虹绿
- **5个手指（张开）** → 进入"接球模式"

### 右手（物理交互器）
- **指点/握拳** → 强力XY平面斥力散射
- **张开手掌** → 星云模式 + 水波纹效果

### 双手组合（终极效果）
当**左右手同时张开**时：
- 粒子以弹跳轨迹飞向左手
- 形成旋转的3D篮球（橙色 + 斐波那契球分布）

## 🚀 在线体验

访问：[https://snow1943.github.io/gestureAiming/](https://snow1943.github.io/gestureAiming/)

⚠️ **注意**：需要允许摄像头权限才能使用

## 💻 本地运行

```bash
# 克隆仓库
git clone https://github.com/snow1943/gestureAiming.git
cd gestureAiming

# 启动本地服务器（任选其一）
python3 -m http.server 8080
# 或
npx http-server -p 8080

# 访问 http://localhost:8080
```

## 🛠️ 技术栈

- **Three.js** - 3D粒子渲染
- **MediaPipe Hands** - 手势识别
- **Canvas API** - 文字坐标生成
- **纯HTML/CSS/JS** - 无需构建工具

## 📋 系统要求

- ✅ 现代浏览器（Chrome、Edge、Firefox）
- ✅ 摄像头设备
- ✅ HTTPS环境（或localhost）
- ⚠️ 建议使用桌面设备（移动端性能可能不足）

## 🎨 配置参数

可在代码中调整以下参数：

```javascript
const CONFIG = {
    PARTICLE_COUNT: 12000,      // 粒子数量
    PARTICLE_SIZE: 2.4,         // 粒子大小
    LERP_FACTOR: 0.16,          // 归位速度
    REPULSION_STRENGTH: 80,     // 斥力强度
    REPULSION_RADIUS: 150,      // 斥力半径
    TEXT_FONT_SIZE: 280,        // 文字字体大小
    BASKETBALL_RADIUS: 100,     // 篮球半径
};
```

## 📄 许可证

MIT License

## 👨‍💻 作者

Created by Aiming

---

⭐ 如果你喜欢这个项目，请给个Star！
