# AFU Welland 智能体脂秤 iOS 客户端 (AntAfouScale)

基于[maoziban/smart-body-scale-IOS](https://github.com/maoziban/smart-body-scale-IOS)项目适配了IOS 15

## 🚀 快速上手

### 环境要求
- Xcode 26.0+（工程使用 Xcode 26 项目格式）
- iOS 15.0+（已适配 iOS 15.3.1）
- 物理真机（用于调试蓝牙功能）

### 运行步骤
1. 使用 Git 克隆本项目到本地，或直接在 Xcode 中打开 `体脂秤.xcodeproj`。
2. 真机本地调试时，在 `Signing & Capabilities` 中配置您自己的签名；GitHub Actions 生成的 IPA 不含签名。
3. 连接您的 iOS 设备，选择目标设备并运行 (Cmd + R)。
4. 开启手机蓝牙，光脚站在体脂秤上使其开机，App 即可自动完成首次配对与同步。

### GitHub Actions 获取 IPA
1. 将仓库推送到 GitHub，并在仓库的 `Actions` 页面启用 Actions。
2. 推送代码或在 `Build unsigned iOS IPA` 工作流中选择 `Run workflow`。成功后打开该次运行，在 `Artifacts` 下载 `unsigned-ios-ipa` 并解压取得 `体脂秤.ipa`。
3. 该 IPA 未签名，不能通过 iOS 普通方式直接安装。TrollStore 支持 iOS 15.3.1，可在设备上先安装并通过 TrollStore 打开 IPA；但 TrollStore 本身的安装方法取决于设备型号和系统版本。安装 TrollStore 后，建议在其设置中配置 Persistence Helper。也可改用其他侧载工具重新签名安装。

---

## 📄 隐私声明

本项目不包含任何网络请求 SDK，所有个人资料、成员记录和身体健康数据均**仅保存在您的 iPhone 本地**，绝不会上传至任何云端服务器。
