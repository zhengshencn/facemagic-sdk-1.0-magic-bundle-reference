# 创建特效文件的简易流程

本章介绍了制作图片序列帧特效文件的简要流程。其间涉及到的配置和文件说明，具体详情请详见后续相关章节。

## 1. 创建`*.bundle`目录
在当前目录创建以`.bundle`为结尾的目录，作为特效文件的根目录。例如`nijia.bundle`。命名规则请参考[目录结构](frame-structure.md)
## 2. 准备序列帧文件`*.png`
将所有组成动画的图像文件（图片序列帧）放入bundle目录下。请参考[序列帧文件规格说明](frame-spec.md)，对组成动画的图像文件进行调节。
## 3. 创建特效配置文件`config.json`
创建纯文本文件`config.json`,与`png`文件一同放置于·bundle·目录内。有关配置文件详情，请参考[配置文件](config.md)
## 4. 打包
使用任何支持`zip`压缩格式的软件，将`*.bundle`目录(在本例中是`nijia.bundle`)压缩生成任意文件名的`zip`文件, 如`nijia.zip`。请注意保证`nijia.bundle`目录存在于zip文件的根目录下，既保证`zip`文件根目录下仅有此`nijia.bundle`一个文件(序列帧文件和配置文件在`nijia.bunble`目录里)。
具体文件结构，请参考[目录结构](frame_structure.md)
## 5. 测试
使用`FaceMagic SDK`特效测试工具在设备端测试特效。请参考`FaceMagic SDK`测试工具手册。
## 6. （可选）发布
测试通过后，使用*合作伙伴帐号*特效文件上传至*魔法商店*。并在`FaceMagic SDK Demo·或任何使用`FaceMagic SDK·并集成了*魔法商店*的APP里下载、使用。
