# TofuGun 資源包使用指南

## 概述

這個資源包為TofuGun插件提供自定義音效和槍械模型。

## 功能

### 音效
- 使用原版Minecraft音效
- 重裝音效
- 命中音效
- 空彈音效

### 模型
- 13種不同槍械的2D模型
- 使用CustomModelData系統
- 簡單的2D貼圖顯示

## 安裝方法

### 方法1：手動安裝
1. 將整個`resource_pack`文件夾複製到Minecraft的`resourcepacks`目錄
2. 在遊戲中啟用資源包

### 方法2：插件自動安裝（推薦）
1. 將`resource_pack`文件夾放在插件jar文件同目錄
2. 插件會自動安裝資源包

## 文件結構

```
resource_pack/
├── pack.mcmeta                    # 資源包元數據
├── assets/
│   ├── minecraft/
│   │   └── models/
│   │       └── item/
│   │           └── stick.json     # 木棒模型覆蓋
│   └── tofugun/
│       ├── sounds.json            # 音效配置
│       ├── models/
│       │   └── guns/              # 槍械模型
│       │       ├── pistol.json
│       │       ├── ak47.json
│       │       └── ...
│       └── textures/
│           └── guns/              # 槍械貼圖
│               ├── pistol.png
│               ├── ak47.png
│               └── ...
└── README.md                      # 本文件
```

## CustomModelData 對應表

| 槍械類型 | CustomModelData | 模型文件 |
|---------|----------------|----------|
| 手槍 | 1001 | pistol.json |
| 左輪手槍 | 1002 | revolver.json |
| 衝鋒槍 | 1003 | smg.json |
| 烏茲衝鋒槍 | 1004 | uzi.json |
| 突擊步槍 | 1005 | assault_rifle.json |
| AK-47 | 1006 | ak47.json |
| M4A1 | 1007 | m4a1.json |
| 狙擊步槍 | 1008 | sniper_rifle.json |
| AWP | 1009 | awp.json |
| 霰彈槍 | 1010 | shotgun.json |
| 雙管霰彈槍 | 1011 | double_barrel.json |
| 機關槍 | 1012 | machine_gun.json |
| 加特林機槍 | 1013 | minigun.json |

## 音效說明

### 射擊音效
- 使用原版Minecraft音效
- 手槍類：`ENTITY_GENERIC_EXPLODE`
- 衝鋒槍類：`ENTITY_FIREWORK_ROCKET_BLAST`
- 步槍類：`ENTITY_LIGHTNING_BOLT_THUNDER`
- 狙擊槍類：`ENTITY_DRAGON_FIREBALL_EXPLODE`
- 霰彈槍類：`ENTITY_GENERIC_EXPLODE`
- 機槍類：`ENTITY_FIREWORK_ROCKET_BLAST_FAR`

### 其他音效
- 重裝音效：`ITEM_CROSSBOW_LOADING_END`
- 命中音效：`ENTITY_EXPERIENCE_ORB_PICKUP`
- 空彈音效：`UI_BUTTON_CLICK`

## 自定義貼圖

要添加自定義貼圖，請將PNG文件放在`assets/tofugun/textures/guns/`目錄下：

- `pistol.png` - 手槍貼圖 (16x16或32x32)
- `ak47.png` - AK47貼圖 (16x16或32x32)
- `m4a1.png` - M4A1貼圖 (16x16或32x32)
- `revolver.png` - 左輪手槍貼圖
- `smg.png` - 衝鋒槍貼圖
- `uzi.png` - 烏茲衝鋒槍貼圖
- `assault_rifle.png` - 突擊步槍貼圖
- `sniper_rifle.png` - 狙擊步槍貼圖
- `awp.png` - AWP貼圖
- `shotgun.png` - 霰彈槍貼圖
- `double_barrel.png` - 雙管霰彈槍貼圖
- `machine_gun.png` - 機關槍貼圖
- `minigun.png` - 加特林機槍貼圖

**注意**：所有貼圖都應該是16x16或32x32像素的PNG文件

## 故障排除

### 音效不播放
1. 檢查原版音效是否正常
2. 確認插件配置是否正確
3. 檢查音效音量設定

### 模型不顯示
1. 檢查CustomModelData是否正確設置
2. 確認模型文件路徑正確
3. 檢查貼圖文件是否存在

### 資源包不載入
1. 檢查pack.mcmeta文件格式
2. 確認pack_format版本正確
3. 檢查文件結構是否完整

## 技術支持

如有問題，請檢查：
1. Minecraft版本兼容性
2. 插件版本
3. 資源包載入順序

## 版本信息

- 資源包版本：1.0.0
- 支持的Minecraft版本：1.20+
- 插件版本：1.0.0
