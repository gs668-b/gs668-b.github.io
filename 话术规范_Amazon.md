# Amazon 售后话术规范文档

> 本文档由 `售后修正模板-新（亚马逊）.docx` 全部模板整理而成。
> 维护责任：业务同事。模板正文改动请同步更新变更记录。
> 调用方式：由分诊 SKILL 定出问题分类 → 在本库按编号找到候选模板 → 检查渠道限制和前置条件 → 通过才可使用。

***

## 一、编码规则

- 售前：`A-PRE-01`、`A-PRE-02`……
- 售中：`A-MID-01`……
- 售后：`A-POST-01`、`A-POST-02`……（按二级问题分类，每个模板一个编号）
  - 二级分类下按顺序编号，如 `A-POST-01-01`、`A-POST-01-02`……

***

## 二、格式统一规则

| 项               | 规则                                                                      |
| --------------- | ----------------------------------------------------------------------- |
| 称呼统一            | `Hello [Customer Name],` 或 `Hello,`（中性称呼，不提取真名；统一用 Hello，不用 Hi / Dear）   |
| 结尾统一            | `Best regards,` + 换行 + `MelodySusie Support Team`                       |
| 第 32 条 / 第 33 条 | 原缺署名，补上 `MelodySusie Support Team`                                      |
| 第 36 条          | `MelodySusie Customer Support Team` → `MelodySusie Support Team`        |
| 第 37 条          | `Warm regards` → `Best regards`                                         |

***

## 三、参数标注规则

在模板正文中，用以下标记替代原文中的具体信息：

| 标记                | 说明                                         |
| ----------------- | ------------------------------------------ |
| `{订单号}`           | AI 从订单数据自动填充                               |
| `{物流单号}`          | AI 从物流数据自动填充                               |
| `{承运商}`           | AI 从物流数据自动填充                               |
| `{追踪链接}`          | AI 从物流数据自动填充                               |
| `{产品名}`           | AI 从订单数据自动填充                               |
| `{数量}`            | AI 从订单数据自动填充                               |
| `{客户姓名}`          | AI 填充（但称呼用中性，不提取真名）                        |
| `{收件人姓名}`         | AI 从地址数据填充                                 |
| `{地址}`            | AI 从地址数据填充                                 |
| `{电话}`            | AI 从地址数据填充                                 |
| `{手柄/主机/配件}`      | AI 根据已核实部件填充                               |
| `[CONFIRM:运费金额]`  | 需运营确认金额（如 $15 / $40 / $20）                 |
| `[CONFIRM:折扣额度]`  | 需运营确认（如 10% / 20% / 30%）                   |
| `[CONFIRM:退款比例]`  | 需运营确认（如 50%）                               |
| `[CONFIRM:服务费金额]` | 需运营确认（如 $20）                               |
| `[CONFIRM:退款金额]`  | 需运营确认（如 $5）                                |
| `[Customer Name]` | 占位符：替换为中性称呼（Hello），不提取真名        |

> 模板层级分为三级：
>
> - **即刻可用**：无前置条件、渠道为全部，AI 可直接使用。
> - **条件**：有渠道限制或场景触发条件，满足条件后可用。
> - **前置条件**：需人工确认某项事实后方可使用（如保修状态、补发已创建、退款已发起等）。

***

## 四、模板明细

### 售前（2 条）

***

#### A-PRE-01｜延保注册引导

`即刻可用`｜问题分类：PRE｜渠道：全部｜前置条件：无

场景：客户询问如何延保。

> 改写说明：原文 `you're eligible for an extended warranty service` 是资格断言，改为 `MelodySusie offers an extended warranty service`，陈述服务存在，不断言此客户是否符合。

```text
Hello,

We hope you're enjoying your MelodySusie device! We're pleased to let you know that MelodySusie offers an extended warranty service.

To activate the warranty, simply follow the steps below:

1. Visit our warranty registration page at the link below:
   https://www.melodysusie.com/pages/extend-warranty
2. Fill out the form and submit it — that's all it takes. It's quick and easy!

If you run into any issues during the registration process, just reply to this email and we'll be happy to help you right away.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

#### A-PRE-02｜发票下载路径引导

`条件`｜问题分类：PRE｜渠道：全部（仅 Amazon 订单）｜前置条件：购买渠道=Amazon

场景：客户询问发票如何下载。

> 格式调整：称呼 `Hi,` → `Hello,`；结尾 `Warm regards` → `Best regards`。

```text
Hello,

Thank you for reaching out to us. I'd be happy to guide you through downloading your invoice for record-keeping purposes.

Please follow the simple steps below:

1. Go to Your Orders on Amazon.
2. Locate the order for which you need the invoice.
   Tip: If the order isn't visible, try selecting a different time range from the "Orders placed in" menu.
3. Click on Invoice, then choose to download or print it.

This invoice serves as a helpful reference for your purchase.

If you have any further questions or need additional assistance, please let us know. Thank you for trusting MelodySusie — we're always here to help.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

### 售后（按二级问题分类）

***

## A-POST-01 产品售后问题（故障/异常）

***

#### A-POST-01-01｜引导客户发送视频与订单到 Service 邮箱

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：客户在 Amazon 站内/后台反馈产品故障，需转 Service 邮箱统一处理。发送时附件放 Service 邮箱地址截图。

```text
Hello [Customer Name],

Thank you for reaching out. This is the MelodySusie Support Team, and we'll be happy to assist you.

To help us check the issue and provide the right solution, could you please send the following information to the support email address listed in the attached note?

1. A short video or photos showing the issue;
2. Your Amazon order number (for example, 114-8100678-2703450), or a screenshot of your order details.

Once our after-sales team receives the information, we will check your case and get back to you within 24 hours.

Thank you for your cooperation.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                                     |
| ---------------- | --- | -------------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名        |

***

#### A-POST-01-02｜索要订单截图 / 订单超过 2 年后台查不到

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：后台无法定位订单，或订单时间较久，需要客户补充截图/型号。

```text
Hello [Customer Name],

Thank you for your message. We were unable to locate the order with the information currently available. Could you please send us a screenshot of your order details, including the order number, product name, and purchase date?

If the order was placed more than two years ago, please also send a photo of the model number on the product, if available. This will help us confirm the correct product and available support options.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-03｜索要视频/照片以确认问题

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：客户反馈功能异常，但没有提供可判断的证据。

```text
Hello [Customer Name],

Thank you for contacting us. I'm sorry to hear that you are experiencing an issue with your MelodySusie product. To help us understand the issue and provide the most suitable solution, could you please send a short video showing the problem?

If a video is not convenient, a few clear photos would also be helpful. Once we check the video/photos and your order information, we will follow up with the next steps.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-04｜确认是手柄/主机/其他部件问题

`条件`｜问题分类：POST-01｜渠道：全部｜前置条件：已收到故障描述

场景：客户描述不清，需要判断是 handpiece、machine 还是附件问题。

> 改写说明：原文末句 `we will arrange the appropriate support as quickly as possible` 属完成式承诺，改为核实式 `we'll advise on the next step`。

```text
Hello [Customer Name],

Thank you for your message. I'm sorry for the inconvenience this has caused. To make sure we send the correct replacement part, could you please help us confirm which part is not working as expected?

- Is the issue with the handpiece?
- Is the issue with the main machine/body?
- Or is another accessory not working properly?

A short video or a few photos would be very helpful. Once we've confirmed the issue and reviewed your order details, we'll advise on the next step.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-05｜保修期内：补发配件/整机并索要地址

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认保修状态

场景：已经确认产品或部件存在问题，且符合保修条件。

```text
Hello [Customer Name],

Thank you for sharing the details with us. Based on the information provided, we can help arrange a replacement {手柄/主机/配件} for you under the warranty.

To proceed, please reply with your full shipping address and phone number for delivery purposes. Once we receive the information, we will arrange the replacement shipment and share the tracking details when available.

Thank you for your cooperation.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型   | 说明                              |
| ---------------- | ---- | ------------------------------- |
| \[Customer Name] | 占位符  | 替换为中性称呼（Hello），不提取真名 |
| {手柄/主机/配件}       | 自动填充 | AI 根据已核实部件填充                    |

***

#### A-POST-01-06｜已安排 FBA/多渠道补发通知

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认补发已实际创建

场景：补发已创建，等待物流单号。

```text
Hello [Customer Name],

Thank you for your patience. We have arranged a replacement package to be sent to the address you provided. We will follow up with the tracking number as soon as it becomes available so you can monitor the delivery progress.

If you have any questions while waiting, please contact us at once.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-07｜已安排中国仓/CN 小包补发通知

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认补发已实际创建

场景：FBA 缺货或需从中国仓补发。

```text
Hello [Customer Name],

Thank you for your patience. We have arranged for the replacement package to be shipped from our China warehouse to the address you provided. The estimated delivery time is approximately [6-10] business days, depending on the destination and carrier schedule.

We will send you the tracking number as soon as it is available. Thank you for your understanding.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符  | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-08｜超保修：运费补发手柄/配件

`前置条件`｜问题分类：POST-01｜渠道：仅 Service 邮箱｜前置条件：需人工确认超保

场景：订单超过 12 个月保修期，但品牌愿意 goodwill 支持，客户支付运费。

> 渠道限制：仅 Service 邮箱，后台回复勿用。
> 金额标注：原文 `$15 shipping fee` 标注为 `[CONFIRM:运费金额]`。

```text
Hello [Customer Name],

Thank you for sharing the details with us. Based on the information provided, it appears that the handpiece may not be working as expected.

After checking the order information, we found that the purchase is outside our 12-month warranty period, so it is not eligible for a standard warranty replacement. However, we would still like to help as a one-time goodwill solution. We can provide a replacement handpiece at no product cost. You would only need to cover a [CONFIRM:运费金额] shipping fee.

To proceed, please use the official MelodySusie payment link below to complete the shipping fee payment:
https://www.melodysusie.com/products/shipping-fee

Please make sure the payment page URL begins with https://www.melodysusie.com/. You will be asked to complete the payment through the official checkout page. MelodySusie will never ask for your full card number, CVV, or account password by email.

After completing the payment, please reply with:
1. A screenshot of the payment confirmation page or order confirmation email;
2. Your full shipping address;
3. Your phone number for delivery purposes.

For security, you may cover or hide any sensitive payment details in the screenshot. We only need to confirm the order/payment reference and amount. Once we receive the confirmation, we will arrange the replacement shipment.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:运费金额]  | 待确认 | 需运营确认金额（如 $15）                  |

***

#### A-POST-01-09｜超保修：运费补发整机

`前置条件`｜问题分类：POST-01｜渠道：仅 Service 邮箱｜前置条件：需人工确认超保

场景：订单超过 12 个月保修期，问题需要整机补发，客户支付运费。

> 渠道限制：仅 Service 邮箱，后台回复勿用。
> 金额标注：原文 `$40` 与数量 `[40]` 均标注为 `[CONFIRM:运费金额]`。

```text
Hello [Customer Name],

Thank you for contacting MelodySusie Support. After checking the order information, we found that the purchase is outside our 12-month warranty period, so it is not eligible for a standard warranty replacement.

However, we would still like to support you with a one-time goodwill replacement option. We can provide a replacement machine at no product cost. You would only need to cover a [CONFIRM:运费金额] shipping fee.

To proceed, please use the official MelodySusie payment link below to complete the shipping fee payment:
https://www.melodysusie.com/products/shipping-fee

Please make sure the payment page URL begins with https://www.melodysusie.com/. If the page requires you to adjust the quantity to match the shipping fee amount, please set the quantity to [CONFIRM:运费金额] so the total reflects the [CONFIRM:运费金额] shipping fee.

After completing the payment, please reply with a screenshot of the payment confirmation page or order confirmation email, along with your full shipping address and phone number. For security, please cover or hide any sensitive payment details before sending the screenshot. Once we receive the confirmation, we will arrange the replacement shipment.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:运费金额]  | 待确认 | 需运营确认金额（如 $40），同时用于数量设置         |

***

#### A-POST-01-10｜客户原因/进水损坏：支付服务费

`前置条件`｜问题分类：POST-01｜渠道：仅 Service 邮箱｜前置条件：需人工确认客户原因致损

场景：客户明确说明产品进水/摔落等非标准保修问题。

> 渠道限制：仅 Service 邮箱，后台回复勿用。
> 金额标注：原文 `$20 shipping/service fee` 标注为 `[CONFIRM:服务费金额]`。

```text
Hello [Customer Name],

Thank you for sharing the details with us. Based on the information provided, the product appears to have been exposed to water, so it may not be eligible for a standard warranty replacement.

However, we would still like to help as a one-time goodwill solution. We can provide a replacement handpiece for a [CONFIRM:服务费金额] shipping/service fee.

To proceed, please use the official MelodySusie payment link below:
https://www.melodysusie.com/products/shipping-fee

Please make sure the payment page URL begins with https://www.melodysusie.com/. After completing the payment, please reply with a screenshot of the payment confirmation page or order confirmation email, your full shipping address, and your phone number. For security, please cover or hide any sensitive payment details in the screenshot.

Once we receive the confirmation, we will arrange the replacement shipment.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:服务费金额] | 待确认 | 需运营确认金额（如 $20）                  |

***

#### A-POST-01-11｜超保修：只提供折扣码（后台专用）

`前置条件`｜问题分类：POST-01｜渠道：仅 Amazon 后台｜前置条件：需人工确认超 12 月

场景：订单超过保修期，品牌不补发，仅提供优惠券购买。

> 渠道限制：仅 Amazon 后台。
> 金额标注：原文 `[10%/20%/30%]` 标注为 `[CONFIRM:折扣额度]`；"可叠加 Amazon 促销"保留。

```text
Hello [Customer Name],

Thank you for reaching out to us about your MelodySusie product. After checking the order details, we found that the purchase is outside our 12-month warranty period. Because of this, it is not eligible for a standard warranty replacement or refund.

However, we still value your experience and would like to offer a [CONFIRM:折扣额度] discount coupon toward a compatible replacement or a new MelodySusie product. This discount can be combined with eligible Amazon promotions, if applicable.

Please let us know if you would like to use this option, and we will send the coupon code to you.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:折扣额度]  | 待确认 | 需运营确认（如 10% / 20% / 30%）        |

***

#### A-POST-01-12｜视频没收到/打不开/Google Drive 无权限

`条件`｜问题分类：POST-01｜渠道：全部｜前置条件：客户称已发证据

场景：客户说已发视频，但客服未收到或无法打开。

```text
Hello [Customer Name],

Thank you for your message. We are sorry, but it looks like we did not receive the video or we are unable to open the link you shared. Could you please resend the video as an email attachment, or update the sharing permission so we can access it?

If the file is too large, you may also send a few clear photos showing the issue. Once we receive the video/photos, we will check your case promptly.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-13｜打磨机发烫但未造成伤害

`条件`｜问题分类：POST-01｜渠道：全部｜前置条件：无伤害、无冒烟、无烧焦/电气异味

场景：客户反馈机器发热/发烫，但未提到伤害。

> 安全说明：安全信号出现时（伤害、冒烟、烧焦/电气异味）此模板不适用，改用 A-POST-06 安全回信结构。

```text
Hello [Customer Name],

Thank you for contacting us. Some warmth during use can be normal depending on the speed setting, usage time, and grinding load. However, if the device feels unusually hot, emits any odor or smoke, or causes discomfort, please stop using it immediately.

To help us check this further, could you please send a short video showing the issue, along with the speed setting, approximate usage time, and whether the device was charging or unplugged during use?

Once we receive the information, we will check it and provide the appropriate support.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-14｜打磨笔噪音变大

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：客户反馈使用后噪音变大、转动不顺。

```text
Hello [Customer Name],

Thank you for letting us know. A louder noise can be caused by several factors, such as dust buildup, normal wear over time, or impact during use or storage. We are unable to determine the exact cause remotely, but we would be happy to check it further.

Could you please send us a short video of the handpiece running at low, medium, and high speed? Please also let us know approximately how long the product has been used. Once we check the video and order information, we will provide the most suitable solution.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-15｜屏幕黑点不影响正常使用

`条件`｜问题分类：POST-01｜渠道：全部｜前置条件：仅外观问题且功能正常

场景：显示屏有黑点，但功能正常。

> 金额标注：原文 `partial refund` 标注为 `[CONFIRM:退款比例]`。

```text
Hello [Customer Name],

Thank you for sharing this with us. We are sorry for the inconvenience. Could you please confirm whether the black spot affects the speed display or the normal use of the machine?

If possible, please send a clear photo of the screen while the device is turned on. If the machine works normally and the issue is only cosmetic, we can offer a [CONFIRM:退款比例] refund. If the display or function is affected, we will check the case further and provide the appropriate support.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:退款比例]  | 待确认 | 需运营确认（如 50%）                    |

***

#### A-POST-01-16｜非 MelodySusie 产品/其他品牌

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：确认非本品牌产品（需人工核验）

场景：客户误把其他品牌产品当作 MelodySusie 售后。

```text
Hello [Customer Name],

Thank you for sharing the video with us. After checking the product shown in the video, it appears that the item may not be a MelodySusie product. There may have been a small mix-up with the brand name.

We recommend checking the order details or product packaging to confirm the correct brand/seller so they can provide the right support. If you have another MelodySusie order you would like us to check, please send the order details and we will be happy to help.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-17｜告知顾客无需退还故障产品

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认补发决定已作出

场景：普通功能故障且无需回收。

```text
Hello [Customer Name],

There is no need to return the defective item for this case. You may keep it or dispose of it according to your local disposal guidelines. We hope the replacement product provides a better experience.

If you have any further questions, please contact us at once.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-18｜PC760G 磨头不兼容/无替换磨头

`条件`｜问题分类：POST-01｜渠道：全部｜前置条件：型号=PC760G

场景：客户询问 PC760G 是否兼容 3/32 bit 或普通砂圈。

> 金额标注：原文 `[20%]` 标注为 `[CONFIRM:折扣额度]`。

```text
Hello [Customer Name],

Thank you for your message. The PC760G is designed to work with its included sanding heads and is not compatible with standard 3/32" drill bits or regular sanding bands. At the moment, separate replacement sanding heads for PC760G are not available.

If the included sanding head is damaged or no longer effective, we can offer you a [CONFIRM:折扣额度] discount coupon toward a new PC760G purchase as a goodwill support option. Please let us know if you would like to use this discount, and we will send the coupon code to you.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:折扣额度]  | 待确认 | 需运营确认（如 20%）                    |

***

#### A-POST-01-19｜甲油胶无法固化

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：客户反馈 gel polish 不干/不固化。

```text
Hello [Customer Name],

Thank you for contacting us. We are sorry to hear that the gel polish is not curing as expected. Curing results can vary depending on the lamp type, wattage, application thickness, and curing time.

To help improve the result, please try applying a thinner layer and curing it under a compatible UV/LED lamp for the recommended time. If needed, you may cure for an additional cycle.

If the issue continues, could you please send us the product name/batch information, the lamp model you used, and a photo or video showing the result after curing? We will check it and provide further support.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-20｜刷子毛脱落

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：客户反馈笔刷毛脱落。

```text
Hello [Customer Name],

Thank you for reaching out. We are sorry to hear about the issue with the brush bristles. To help protect the bristles, we recommend cleaning the brush gently with brush cleaner or nail polish remover and avoiding long soaking times, hot water, or direct sunlight after cleaning.

If the bristles started falling out shortly after you received the product, please send us a photo of the brush and your order information. We will check the case and provide the appropriate support.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-21｜甲油胶颜色不同/色差

`即刻可用`｜问题分类：POST-01｜渠道：全部｜前置条件：无

场景：客户反馈实物颜色与图片不同。

```text
Hello [Customer Name],

Thank you for sharing your feedback. We understand that color accuracy is important, and we are sorry that the shade did not meet your expectations. Please note that gel polish colors may appear slightly different due to screen settings, lighting, nail base color, and the number of coats applied.

If the color difference seems significant, please send us a photo of the bottle label and the color applied on the nail or swatch under natural light. We will check it and do our best to help.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-01-22｜超保修协商部分退款（变体一：超 6 月保修期）

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认超 6 月保修期

场景：客户产品超过 6 月保修期，协商部分退款/延保方案。

> 格式调整：补上署名 `MelodySusie Support Team`；结尾 `Warm regards` → `Best regards`。
> 此变体对应超 6 月情景，正文保留 `6-month warranty period`。

```text
Hello,

Thank you for reaching out to us, and I'm truly sorry to hear that your item is no longer turning on. I completely understand how frustrating this must be, and I appreciate you giving us the opportunity to help.

After checking your purchase details, I see that your product is just beyond the 6-month warranty period. Under our standard policy, this means a refund or replacement is not available.

However, we would like to offer you a special solution. Although the usual registration window for the additional 6-month warranty has passed, as a gesture of goodwill, if you register your product on our official website now, we will activate the extended warranty and immediately arrange warranty service for your item. Once you complete the registration, our team will quickly process the service to get your tool back in working order.

We hope this shows our commitment to your satisfaction. Please visit our website to complete the registration, and let us know once you have done so. We will take care of the rest.

We sincerely apologize for any inconvenience caused, and we truly appreciate your understanding. If you have any further questions, please don't hesitate to reach out.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

#### A-POST-01-23｜超保修协商部分退款（变体二：超 12 月保修期）

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认超 12 月保修期

场景：客户产品超过 12 月保修期，协商部分退款方案。

> 格式调整：补上署名 `MelodySusie Support Team`。
> 口径修正：正文 `6-month warranty period` 改为 `12-month warranty period`（此变体对应超 12 月情景）。
> 金额标注：原文 `30%` 标注为 `[CONFIRM:退款比例]`。

```text
Hello,

Thank you for reaching out to us, and I'm truly sorry to hear that your product is no longer turning on. I completely understand how frustrating this must be.

After checking your purchase details, I see that the product is just beyond the 12-month warranty period, which typically means a refund or replacement is not available under standard policy. However, because your satisfaction and trust mean a great deal to us, we would like to offer you a partial refund of [CONFIRM:退款比例] of the purchase price as a gesture of goodwill.

We hope this solution brings you some relief, and we sincerely apologize for any inconvenience caused. We know how important your tools are to your nail care routine, and we're committed to supporting you as best we can.

Please let us know if this works for you, or if you have any further questions. We truly appreciate your understanding and are here to help.

Best regards,
MelodySusie Support Team
```

| 参数              | 类型  | 说明           |
| --------------- | --- | ------------ |
| \[CONFIRM:退款比例] | 待确认 | 需运营确认（如 30%） |

***

#### A-POST-01-24｜配件有瑕疵：补发或退款

`前置条件`｜问题分类：POST-01｜渠道：全部｜前置条件：需人工确认配件瑕疵

场景：配件有瑕疵但不影响核心功能，提供补发或退款选项。

> 格式调整：称呼 `Hi,` → `Hello,`；补上署名 `MelodySusie Support Team`。
> 金额标注：原文 `$5 refund` 标注为 `[CONFIRM:退款金额]`。

```text
Hello,

Thank you for reaching out to us. We sincerely apologize for the inconvenience caused by our product. While this issue does not affect its core functionality, we value your experience greatly and would like to make it right for you.

To express our sincere apology, we are pleased to offer you the following options:

- Refund: We can process a [CONFIRM:退款金额] refund for you.
- Replacement: We can send you a replacement.

Whichever option you prefer, we hope it reflects our commitment to your satisfaction. Please kindly reply to this email with your choice, and we will take care of the rest promptly.

Thank you for your understanding and patience.

Best regards,
MelodySusie Support Team
```

| 参数              | 类型  | 说明            |
| --------------- | --- | ------------- |
| \[CONFIRM:退款金额] | 待确认 | 需运营确认金额（如 $5） |

***

#### A-POST-01-25｜订单作为礼物收到没有订单号

`条件`｜问题分类：POST-01｜渠道：仅 Service 邮箱｜前置条件：无订单号（礼物）

场景：客户作为礼物收到产品，无 Amazon 订单号。

> 渠道限制：仅 Service 邮箱。
> 金额标注：原文 `$15` 标注为 `[CONFIRM:运费金额]`；原文 `10%` 标注为 `[CONFIRM:折扣额度]`。
> 格式调整：补上署名 `MelodySusie Support Team`。

```text
Hello,

If you don't have an Amazon order number, we can still assist you with the following options:

Option 1: Replacement Handpiece

We can offer you a replacement handpiece for a nominal shipping fee of [CONFIRM:运费金额]. To proceed, please visit the link below to pay the shipping fee:
https://www.melodysusie.com/products/shipping-fee

At the provided URL, simply adjust the quantity to [CONFIRM:运费金额] units to reflect the [CONFIRM:运费金额] fee. Once the payment is complete, please send us your shipping address along with a screenshot of the payment confirmation. We will then arrange for the replacement handpiece to be dispatched to you without delay.

Option 2: [CONFIRM:折扣额度] Discount Coupon

If you are interested in purchasing the same model, we are pleased to offer you a [CONFIRM:折扣额度] discount coupon for your next purchase. This coupon can be combined with all other promotions on Amazon. Please let us know if you would like to take advantage of this offer, and we will send the discount coupon to you right away.

We appreciate your understanding and look forward to resolving this matter for you.

Best regards,
MelodySusie Support Team
```

| 参数              | 类型  | 说明                      |
| --------------- | --- | ----------------------- |
| \[CONFIRM:运费金额] | 待确认 | 需运营确认金额（如 $15），同时用于数量设置 |
| \[CONFIRM:折扣额度] | 待确认 | 需运营确认（如 10%）            |

***

## A-POST-02 破损/发错货/用过的

***

#### A-POST-02-01｜客户说收到二手/被用过产品

`即刻可用`｜问题分类：POST-02｜渠道：全部｜前置条件：无

场景：客户认为产品不是全新、被使用过。

```text
Hello [Customer Name],

Thank you for bringing this to our attention. We are sorry to hear about your concern regarding the condition of the product you received. To help us check this properly, could you please send a few clear photos or a short video showing the product condition, packaging, and any accessories included?

Once we receive the information, our team will check the case and provide the appropriate solution, such as a replacement or refund support if needed.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-02-02｜缺件：MM400D 没有砂圈/配件

`前置条件`｜问题分类：POST-02｜渠道：全部｜前置条件：需人工确认缺件

场景：客户反馈包装缺少砂圈/配件。

```text
Hello [Customer Name],

Thank you for bringing this to our attention. We are sorry that your package may not have been complete. The package should include:

- Nail drill × 1
- Nail drill bits × 8 pcs
- 180-grit sanding bands × 50 pcs

Could you please confirm which item is missing? Once confirmed, please send us your full shipping address and phone number, and we will arrange the missing item to be resent.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

## A-POST-03 退货退款

***

#### A-POST-03-01｜客户自行退款后仍想补发

`前置条件`｜问题分类：POST-03｜渠道：全部｜前置条件：需人工确认平台已退款

场景：客户已经申请/收到全额退款，品牌不能再免费补发。

```text
Hello [Customer Name],

Thank you for contacting us. I'm sorry to hear about the issue with your product. After checking the order information, it appears that a full refund has already been requested/processed for this order. Because of this, we are unable to provide an replacement under the same order.

Please let us know if you have any other questions.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-03-02｜超 30 天想退货退款，提供 50% 退款

`前置条件`｜问题分类：POST-03｜渠道：全部｜前置条件：需人工核验下单日期 + 超 30 天

场景：超过平台退货期，但品牌愿意部分退款且无需退回。

> 金额标注：原文 `50%` 标注为 `[CONFIRM:退款比例]`。

```text
Hello [Customer Name],

Thank you for reaching out. I'm sorry for the inconvenience this has caused. After checking the order information, we found that the order was placed more than 30 days ago and is outside the standard return window. However, as a goodwill solution, we can offer a [CONFIRM:退款比例] refund, and you do not need to return the machine or the replacement item.

Please let us know if this solution works for you, and we will proceed with the refund.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |
| \[CONFIRM:退款比例]  | 待确认 | 需运营确认（如 50%）                    |

***

#### A-POST-03-03｜退款信息通知

`前置条件`｜问题分类：POST-03｜渠道：全部｜前置条件：需人工确认退款已实际发起

场景：退款已发起，通知客户退款信息与到账时效。

> 格式调整：补上署名 `MelodySusie Support Team`（原文结尾 `Best regards,` 后无团队名）。

```text
Hello,

I hope this message finds you well.

In line with your request, I have arranged for a full refund to be issued to you. Please notice your payment account, as the refunded amount will be returned via the original payment method you used. Depending on your bank or payment provider, it may take 3-5 business days for the transaction to reflect in your account.

Should you have any questions or concerns regarding the refund process, or if there is anything else I can assist you with in the future, please do not hesitate to reach out. Our commitment to providing excellent customer service remains steadfast, and we are here to support you every step of the way.

We appreciate your understanding and hope to have the opportunity to serve you better in the future.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

#### A-POST-03-04｜客户想换产品，但我们提供退款

`前置条件`｜问题分类：POST-03｜渠道：全部｜前置条件：需人工确认退款决定已作出

场景：客户想换一个产品，但因 Amazon 系统限制无法直接换货，提供退款。

> 格式调整：称呼 `Dear ,` → `Hello,`；署名 `MelodySusie Customer Support Team` → `MelodySusie Support Team`。

```text
Hello,

I sincerely apologize for the malfunction you have experienced with our product. We deeply regret any frustration or inconvenience this may have caused and truly appreciate your patience as we work to resolve the matter.

Unfortunately, due to limitations within Amazon's system, we are unable to arrange a direct replacement for a different product through their platform. However, as per your request, we would be pleased to offer you a full refund. Once the refund has been processed, you are welcome to select another product from the MelodySusie store that better meets your needs.

We hope this solution is acceptable to you. Please do not hesitate to reach out if you have any questions or require further assistance — we are here to support you every step of the way.

Thank you for giving us the opportunity to make things right.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

#### A-POST-03-05｜联系 Amazon 客服（退货退款）

`条件`｜问题分类：POST-03｜渠道：全部（仅 Amazon 订单）｜前置条件：购买渠道=Amazon

场景：订单在 30 天退货期内，引导客户直接联系 Amazon 客服发起退货退款。

> 格式调整：称呼 `Hi,` → `Hello,`；补上署名 `MelodySusie Support Team`（原文 `Best regards,` 后无团队名）。

```text
Hello,

We sincerely apologize for the inconvenience you've experienced.

After checking, we confirmed that your order was placed less than 30 days ago. Since it falls within the return window, you can contact Amazon customer service directly to initiate a return and request a refund.

If you need any further assistance, please don't hesitate to let us know. We're here to help.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

## A-POST-04 妥投未收到

***

#### A-POST-04-01｜物流显示 Delivered 但客户未收到

`条件`｜问题分类：POST-04｜渠道：全部（仅 Amazon 订单）｜前置条件：购买渠道=Amazon

场景：补发或订单物流显示签收/送达，但客户反馈未收到。

```text
Hello [Customer Name],

Thank you for contacting us. We understand how frustrating it can be when a package is marked as delivered but cannot be found. After checking the tracking information, the package appears to have been marked as delivered by the carrier. We recommend checking with household members, neighbors, the front desk, mailbox area, or any safe delivery location nearby.

Since this shipment was fulfilled by Amazon, Amazon Customer Support has the most complete access to the delivery details and can help investigate the delivery location or assist with a claim if needed. Please let us know if Amazon is unable to assist, and we will do our best to support you further.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

## A-POST-05 物流延迟

***

#### A-POST-05-01｜联系 Amazon 客服（询问物流）

`条件`｜问题分类：POST-05｜渠道：全部（仅 Amazon 订单）｜前置条件：购买渠道=Amazon

场景：订单正在加急配送，由 Amazon Logistics 承运，引导客户联系 Amazon 客服查询物流。

> 格式调整：补上署名 `MelodySusie Support Team`（原文结尾无署名）。

```text
Hello,

We have checked your order and can confirm that it is currently being expedited. Please note that this item is being delivered by Amazon Logistics. For further assistance, we recommend reaching out to Amazon Customer Service directly, as they will be best able to support you.

If you have any additional questions, please let us know. We're here to help.

Best regards,
MelodySusie Support Team
```

| 参数 | 类型 | 说明        |
| -- | -- | --------- |
| -  | -  | 本模板无非常规参数 |

***

## A-POST-06 安全事件

***

#### A-POST-06-01｜安全/烫伤首封（客户只要求退款）

`前置条件`｜问题分类：POST-06｜渠道：全部｜前置条件：安全事件（仅人工使用）

场景：客户反馈烫伤/安全体验，但当前只要求退款，未要求索赔/验证/补偿。

> 使用限制：仅人工使用，Agent 改用安全回信结构。

```text
Hello [Customer Name],

Thank you for reaching out and sharing your experience with us. We are sorry to hear about what happened and hope you are feeling better.

Please stop using the product immediately.

Since you requested a refund, we can help arrange a full refund for your order. The refund will be returned to your original payment method, and depending on your bank or payment provider, it may take a few business days to appear in your account.

If you would prefer a goodwill replacement or another support option instead of a refund, please let us know and we will be happy to assist.

We take customer feedback seriously and will share your report with our internal team for check. If you would like us to further check the product issue, you may also send photos/videos of the product and order details, but no additional information is required for us to proceed with your refund request.

Thank you for giving us the opportunity to assist you.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

#### A-POST-06-02｜安全/烫伤需进一步验证

`前置条件`｜问题分类：POST-06｜渠道：全部｜前置条件：安全事件（仅人工使用）

场景：客户要求解释原因、索赔、补偿，或问题严重，需要质安/法务复核。

> 使用限制：仅人工使用。

```text
Hello [Customer Name],

Thank you for sharing the additional information with us. We are sorry to hear about your experience and hope you are recovering well.

Please stop using the product immediately and keep the product, charger, accessories, and packaging in their current condition. Our team may need these items for further check.

To help us check the matter carefully, could you please provide the following information if available?

1. Your order number or order screenshot;
2. Photos or videos of the product, charger, accessories, and packaging;
3. A brief description of how the product was being used when the issue occurred;
4. Approximate usage time, speed setting, and whether the product was charging or unplugged;
5. Whether medical attention was needed.

As a goodwill gesture while the check is ongoing, we can help arrange a refund and/or replacement support option. This support does not determine the cause of the issue, but we want to assist you while we check the matter.

Thank you for your cooperation.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

## A-POST-07 渠道确认

***

#### A-POST-07-01｜非亚马逊平台购买/需要确认渠道

`条件`｜问题分类：POST-07｜渠道：全部（站内不得提其他平台）｜前置条件：无

场景：客户非 Amazon 购买，或购买渠道不明确。

> 渠道限制：站内回复不得提及其他平台名称。

```text
Hello [Customer Name],

Thank you for sharing the video. Based on what we can see, the handpiece may not be working as expected. To confirm the correct support channel, could you please let us know where the product was purchased, such as our official website, Amazon, Walmart, or another retailer?

If you have an order number or order screenshot, please send it to us as well. If the order was placed through our official MelodySusie website, we can check it directly. If it was purchased through another retailer, we may need the order details to confirm the available support options.

If the product is outside the applicable warranty period, we can still offer a discount toward a compatible replacement handpiece.

Best regards,
MelodySusie Support Team
```

| 参数               | 类型  | 说明                              |
| ---------------- | --- | ------------------------------- |
| \[Customer Name] | 占位符 | 替换为中性称呼（Hello），不提取真名 |

***

## 五、变更记录

| 版本   | 日期         | 改了什么                                                                                  |
| ---- | ---------- | ------------------------------------------------------------------------------------- |
| V1.0 | 2026-08-27 | 首版。从 `售后修正模板-新（亚马逊）.docx` 整理 2 条售前 + 36 条售后模板，统一编码 A-PRE / A-POST，落实格式统一、参数标注、改写与口径修正 |

