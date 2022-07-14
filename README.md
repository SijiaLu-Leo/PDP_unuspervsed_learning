# PDP_unuspervsed_learning
a unsupervised learning network for 10-target-mstar datasets

## Dataset

### MSTAR (Moving and Stationary Target Acquisition and Recognition) Database

#### Format

- Header
  - Type: ASCII
  - Including data shape(width, height), serial number, azimuth angle, etc.
- Data
  - Type: Two-bytes
  - Shape: W x H x 2
    - Magnitude block
    - Phase Block

## Standard Operating Condition (SOC)

|         |            | Train      |            | Test       |            |
| ------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Class   | Serial No. | Depression | No. Images | Depression | No. Images |
| BMP-2   | 9563       | 17         | 233        | 15         | 196        |
| BTR-70  | c71        | 17         | 233        | 15         | 196        |
| T-72    | 132        | 17         | 232        | 15         | 196        |
| BTR-60  | k10yt7532  | 17         | 256        | 15         | 195        |
| 2S1     | b01        | 17         | 299        | 15         | 274        |
| BRDM-2  | E-71       | 17         | 298        | 15         | 274        |
| D7      | 92v13015   | 17         | 299        | 15         | 274        |
| T-62    | A51        | 17         | 299        | 15         | 273        |
| ZIL-131 | E12        | 17         | 299        | 15         | 274        |
| ZSU-234 | d08        | 17         | 299        | 15         | 274        |

##### Training Set (Depression: 17$\degree$)

```shell
MSTAR-PublicTargetChips-T72-BMP2-BTR70-SLICY/MSTAR_PUBLIC_TARGETS_CHIPS_T72_BMP2_BTR70_SLICY
├ TARGETS/TRAIN/17_DEG
│    ├ BMP2/SN_9563/*.000 (233 images)
│    ├ BTR70/SN_C71/*.004 (233 images)
│    └ T72/SN_132/*.015   (232 images)
└ ...

MSTAR-PublicMixedTargets-CD2/MSTAR_PUBLIC_MIXED_TARGETS_CD2
├ 17_DEG
│    ├ COL1/SCENE1/BTR_60/*.003  (256 images)
│    └ COL2/SCENE1
│        ├ 2S1/*.000            (299 images)
│        ├ BRDM_2/*.001         (298 images)
│        ├ D7/*.005             (299 images)
│        ├ SLICY
│        ├ T62/*.016            (299 images)
│        ├ ZIL131/*.025         (299 images)
│        └ ZSU_23_4/*.026       (299 images)
└ ...

```

##### Test Set (Depression: 15$\degree$)

```shell
MSTAR-PublicTargetChips-T72-BMP2-BTR70-SLICY/MSTAR_PUBLIC_TARGETS_CHIPS_T72_BMP2_BTR70_SLICY
├ TARGETS/TEST/15_DEG
│    ├ BMP2/SN_9563/*.000 (195 images)
│    ├ BTR70/SN_C71/*.004 (196 images)
│    └ T72/SN_132/*.015   (196 images)
└ ...

MSTAR-PublicMixedTargets-CD1/MSTAR_PUBLIC_MIXED_TARGETS_CD1
├ 15_DEG
│    ├ COL1/SCENE1/BTR_60/*.003  (195 images)
│    └ COL2/SCENE1
│        ├ 2S1/*.000            (274 images)
│        ├ BRDM_2/*.001         (274 images)
│        ├ D7/*.005             (274 images)
│        ├ SLICY
│        ├ T62/*.016            (273 images)
│        ├ ZIL131/*.025         (274 images)
│        └ ZSU_23_4/*.026       (274 images)
└ ...

```
