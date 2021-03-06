---
title: Taro.startAccelerometer(res)
sidebar_label: startAccelerometer
id: version-1.3.38-startAccelerometer
original_id: startAccelerometer
---

开始监听加速度数据。

> [参考文档](https://developers.weixin.qq.com/miniprogram/dev/api/device/accelerometer/wx.startAccelerometer.html)

## 类型

```tsx
(res?: Option) => Promise<CallbackResult>
```

## 参数

### Option

| 参数 | 类型 | 默认值 | 必填 | 说明 |
| --- | --- | :---: | :---: | --- |
| interval | "game" or "ui" or "normal" | `"normal"` | 否 | 监听加速度数据回调函数的执行频率 |
| complete | `(res: CallbackResult) => void` |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行） |
| fail | `(res: CallbackResult) => void` |  | 否 | 接口调用失败的回调函数 |
| success | `(res: CallbackResult) => void` |  | 否 | 接口调用成功的回调函数 |

### interval

| 参数 | 类型 | 说明 |
| --- | --- | --- |
| game | `"game"` | 适用于更新游戏的回调频率，在 20ms/次 左右 |
| ui | `"ui"` | 适用于更新 UI 的回调频率，在 60ms/次 左右 |
| normal | `"normal"` | 普通的回调频率，在 200ms/次 左右 |

## 示例代码

```tsx
Taro.startAccelerometer({ interval: 'game' })
```

## API 支持度

| API | 微信小程序 | H5 | React Native |
| :---: | :---: | :---: | :---: |
| Taro.startAccelerometer | ✔️ | ✔️ | ✔️ |
