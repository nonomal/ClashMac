<div align="center">

**语言版本：** [English](README.md) | [简体中文](README.zh-CN.md)

</div>


<p align="center">
  <img src="assets/Logo-Default.png" alt="ClashMac Logo" width="300" style="filter: drop-shadow(0 4px 12px rgba(0, 0, 0, 0.15));">
</p>
<h1 align="center">ClashMac</h1>
<h3 align="center" style="margin-top: 0; margin-bottom: 10px;">轻量级 macOS Clash 菜单栏客户端</h3>
<p align="center">
  🌐 <a href="https://clashmac.app"><strong>官方网站：clashmac.app</strong></a>
</p>

<p align="center" style="margin-top: 0; margin-bottom: 20px;">
  <a href="https://github.com/666OS/ClashMac/releases/latest">
    <img src="https://img.shields.io/github/v/release/666OS/ClashMac?style=flat-square&logo=github&color=green" alt="Latest Release">
  </a>
  <a href="https://github.com/666OS/ClashMac/releases">
    <img src="https://img.shields.io/github/downloads/666OS/ClashMac/total?style=flat-square&logo=dropbox&logoColor=white&color=gold" alt="Downloads">
  </a>
  <a href="https://clashmac.app">
    <img src="https://img.shields.io/badge/官方-网站-orange?style=flat-square&logo=safari" alt="官方网站">
  </a>
  <a href="https://t.me/Pinched666">
    <img src="https://img.shields.io/badge/Telegram-Channel-blue?style=flat-square&logo=telegram">
  </a>
</p>

<p align="center">
  <a href="https://clashmac.app">
    <img src="assets/website.png" alt="ClashMac 官网" width="800">
  </a>
</p>

## 预览
| 深色                             | 浅色                             |
| -------------------------------- | --------------------------------- |
| ![Dark](./assets/preview_dark.png) | ![Light](./assets/preview_light.png) |

## 特色功能

- **原生应用**：SwiftUI 开发，完美融入 macOS 系统
- **轻量高效**：菜单栏应用，资源占用低
- **双代理模式**：系统代理（HTTP/SOCKS5）+ 增强模式（TUN），可独立或同时启用
- **控制中心**：macOS 13+ 集成 Zashboard，内嵌概览、代理、连接、规则、日志等模块
- **免密操作**：特权助手一键安装，系统代理和内核管理全程无需输入密码
- **本地配置**：支持导入本地 YAML/YML 配置文件，自动切换并应用
- **远程订阅**：支持远程配置导入、自动更新、智能命名、URL 验证
- **实时统计**：菜单栏实时显示上下行速度、活跃连接数、内存占用
- **智能配置**：DNS、TUN、GEO 数据库等必要参数自动补全，尊重用户自定义
- **策略组**：菜单直接切换代理节点，支持延迟测速
- **快捷键**：`⌘S` 系统代理 | `⌘E` 增强模式 | `⌘D` 控制中心 | `⌥G/R/D` 全局/规则/直连等
- **配置预检**：切换或导入配置前自动验证，错误时弹窗提示并支持快速编辑
- **崩溃检测**：自动识别内核崩溃原因（Smart 策略、TUN 权限等），提供解决建议
- **自定义界面**：菜单项显示/隐藏可配置，界面按需精简
- **应用更新**：自动检测新版本，一键下载安装，进度实时显示
- **开机启动**：macOS 11.5+ 支持开机自动启动应用
- **多语言**：中英文双语界面，自动跟随系统语言
- **探头小猫**：全新应用图标，深浅色模式自适应
- **网页规则**：一键为当前网页添加代理规则，适配主流浏览器

## 下载

在 [Releases 页面](https://github.com/666OS/ClashMac/releases/latest) 下载最新版本：

- **Apple Silicon (M1/M2/M3/M4)**: `ClashMac-v*-macos-arm64.zip`
- **Intel Mac**: `ClashMac-v*-macos-x86_64.zip`

**兼容方案**：请参阅 [测试配置](https://github.com/666OS/YYDS/tree/main/mihomo/config)

**安装步骤**：
1. 解压下载的 zip 文件
2. 将 `ClashMac.app` 拖到"应用程序"文件夹
3. 首次打开时，右键点击并选择"打开"（绕过安全检查）

**提示**: 不确定您的 Mac 类型？点击左上角  → 关于本机，查看"芯片"信息。

> **注意：Mac Gatekeeper 可能会拦截未签名应用**  
> 因为 ClashMac 没有经过 Apple notarize（公证），macOS 默认不允许直接打开。

### 解决方法

#### 方法 1：系统设置中允许打开
1. 尝试打开 ClashMac，出现安全警告时点击"完成"
2. 打开 **系统设置** → **隐私与安全性**
3. 向下滚动，找到提示："ClashMac 已被阻止打开"
4. 点击旁边的"仍要打开"
5. 在弹出框再点击"仍要打开"即可

#### 方法 2：终端解除限制
在"终端"中输入：

```bash
xattr -cr /Applications/ClashMac.app
```
回车后重新打开应用


#### 方法 3：移除隔离属性

在"终端"中输入：
```bash
xattr -d com.apple.quarantine /Applications/ClashMac.app
```
回车后重新打开应用

## ⚠️ 重要说明

本项目本体暂不开源，当前仓库主要用于发布版本和接受反馈。  
应用使用的第三方开源组件我们均已按要求公开 License。

未来会根据项目进展评估是否开放更多内容。  
感谢理解与支持！ 详细请参阅 [置顶说明](https://github.com/666OS/ClashMac/issues/15)

## 许可证

ClashMac 是一个专有的闭源应用程序。  
本仓库仅提供二进制发布版本。

本项目使用了第三方开源组件。  
完整的许可证列表可在此处查看：

[第三方许可证](https://github.com/666OS/ClashMac/blob/main/THIRD_PARTY_LICENSES.txt) 

## 致谢

- [mihomo](https://github.com/MetaCubeX/mihomo)
- [Vernesong](https://github.com/vernesong/mihomo)
- [Zashboard](https://github.com/Zephyruso/zashboard)

## Star History
[![Star History Chart](https://api.star-history.com/svg?repos=666OS/ClashMac&type=Date)](https://star-history.com/#666OS/ClashMac&Date)

---

<p align="center">
  Made with ❤️ for macOS
</p>
