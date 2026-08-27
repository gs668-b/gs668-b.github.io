# 售后话术规范 - 品牌官网（Website）

> 适用渠道：MelodySusie 官网（Website）售后邮件、站内信  
> 数据来源：售后问题分类收集（网站）.xlsx  
> 文档版本：v1.0

---

## 一、规范总则

### 1. 编码规则

| 阶段 | 前缀 | 示例 |
|---|---|---|
| 售前 | W-PRE | W-PRE-01, W-PRE-02 ... |
| 售中 | W-MID | W-MID-01, W-MID-02 ... |
| 售后 | W-POST | W-POST-01, W-POST-02 ...（按二级问题分类） |

### 2. 格式统一规则

- 称呼统一：`Hello [Customer Name],` 或 `Hello,`
- 结尾统一：`Best regards,` + 换行 + `MelodySusie Customer Service Team`
- 原文中 `Best Wishes` / `Warm regards` / `Warmest Regards` / `Yours sincerely` / `Kind regards` 全部改为 `Best regards,`
- 原文中 `MelodySusie Support Team` 统一改为 `MelodySusie Customer Service Team`
- 原文直接使用客户真名的（`Hello Martina` / `Hello Lisa` / `Hello Jazmin` / `Hello Sonya` 等）改为 `Hello [Customer Name],`
- 原文 `Hello[Customer Name],,`（多逗号）修正为 `Hello [Customer Name],`
- 感叹号在普通语境改句号（保留热情场景，如宣布给客户的利好）

### 3. 内部人名清理

- 原文 E 列（建议的解决方案）中出现的内部人名（如"联系 liqun"）仅用于内部流转，**不得出现在模板正文中**。
- F 列回复正文中不含内部人名，全部保留原文。

### 4. 错别字修正

| 原文 | 修正 |
|---|---|
| Teameam | Team |
| Claim6Claim | Claim |
| provide9provide | provide |
| do5do | do |
| systerm | system（CRM systerm → system） |

### 5. 参数标注规则

AI 从对应数据源自动填充，运营确认类参数需人工确认后填入。

| 参数 | 数据源 | 说明 |
|---|---|---|
| {订单号} | 订单数据 | 官网订单号通常 MS 开头 |
| {物流单号} | 物流数据 | 运单号 |
| {承运商} | 物流数据 | 物流商 |
| {追踪链接} | 物流数据 | 物流查询链接 |
| {产品名} | 订单数据 | 产品名称 |
| {数量} | 订单数据 | 产品数量 |
| {收件人姓名} | 地址数据 | 收件人 |
| {地址} | 地址数据 | 完整收货地址 |
| {电话} | 地址数据 | 联系电话 |
| {发货日期} | 物流数据 | 发出日期 |
| {预计送达日期} | 物流数据 | 预计送达 |
| {物流状态} | 物流数据 | 当前物流状态 |
| {客户询问的国家} | 客户输入 | 客户询问是否发货的国家 |
| {产品型号} | 产品数据库 | 具体型号 |
| {扭矩} | 产品数据库 | 扭矩参数 |
| {转速范围} | 产品数据库 | RPM 范围 |
| {折扣码} | 运营确认 | 优惠码 |
| {Draft Order链接} | 运营确认 | 加单 draft order 链接 |
| [CONFIRM:折扣额度] | 运营确认 | 折扣比例需运营确认 |
| [CONFIRM:退款金额] | 运营确认 | 退款金额需运营确认 |

### 6. 承诺强度规则

- **回复一（首封 / 索证版）**：完成式承诺需降级为核实式。
  - `we will arrange a replacement` → `we will review your case and confirm the next step`
  - `we can offer a replacement` → `we will check the available options and follow up with you`
  - `we have processed a refund` → `your request has been passed to our team for review`
  - `we'll arrange for a new replacement` → `we are reviewing your case and will confirm the next step`
- **回复二（确认后动作版）**：保留承诺，标记为「前置条件」层级（需人工确认对应动作已执行）。
- 层级说明：
  - `即刻可用`：AI 可直接填充参数后发送，无需人工前置动作。
  - `前置条件`：发送前需人工确认对应业务动作（取消 / 退款 / 重发等）已执行。

---

## 二、售前话术（W-PRE）

---

#### W-PRE-01｜延保注册引导

`即刻可用`｜问题分类：PRE-01｜渠道：官网｜前置条件：无  
场景：客户询问如何延长保修。

```text
Hello,

Thank you for reaching out. Please click the following link to claim a free extended warranty:
https://www.melodysusie.com/pages/extend-warranty

How to Claim A Free Extended Warranty
1. Send an extended warranty request with your Amazon orders via the form. Please enter your 17-digit Amazon order ID#, 18-digit TikTok order ID# or Shein order ID#.
2. We will have your order recorded in our system. You've extended your warranty to 12 months already.

If you require our assistance, please feel free to contact us. We are at your service at all times.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 客户按表单自行提交订单号 |

> 修正：`systerm`→`system`；`Best Wishes`→`Best regards`；普通感叹号改句号。

---

#### W-PRE-02｜产品参数查询回复

`即刻可用`｜问题分类：PRE-02｜渠道：官网｜前置条件：无  
场景：客户询问产品参数（转速 / 扭矩 / 电池等）。

```text
Hello,

Thank you for your inquiry. The {产品型号} nail drill features a torque of {扭矩} (gf.cm) and a speed range of {转速范围} RPM. It is suitable for beginners.

If you need more details about other models, please let us know.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品型号} | 产品数据库 | AI 从产品数据库填充，如 PC760G |
| {扭矩} | 产品数据库 | 扭矩数值 |
| {转速范围} | 产品数据库 | RPM 范围 |

> 修正：具体产品参数标注为参数，AI 从产品数据库填充。

---

#### W-PRE-03｜产品推荐引导对比页

`即刻可用`｜问题分类：PRE-03｜渠道：官网｜前置条件：无  
场景：客户求推荐产品（新手 / 去除 top coat / 角质处理等）。

```text
Hello,

Thank you for reaching out. Since you're just starting out, it's important to have a drill that's easy to use yet powerful enough for tasks like removing top coat and gently working on cuticles without cutting.

We recommend checking out our drill comparison page, where you can see the features of different models side by side and find the one that best fits your needs:
https://www.melodysusie.com/pages/compare?ref=naviMenu

If you have any questions about a specific model or need guidance on getting started, feel free to reply — we're happy to assist.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 固定引导文案 |

---

#### W-PRE-04｜物流配送可用性确认

`即刻可用`｜问题分类：PRE-04｜渠道：官网｜前置条件：无  
场景：客户询问是否发货到某国家。

```text
Hello,

Thank you for reaching out. Yes, we do ship to {客户询问的国家}. To make it easy, we offer reliable international shipping and you can shop directly from our website: https://www.melodysusie.com

If you need help choosing or want a recommendation for first-time use, just let us know — we're happy to assist.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {客户询问的国家} | 客户输入 | 客户询问是否发货的国家，如 Turkey |

> 修正：具体国家名标注为参数。

---

#### W-PRE-05｜物流费用查询

`即刻可用`｜问题分类：PRE-05｜渠道：官网｜前置条件：无  
场景：客户询问运费。

```text
Hello [Customer Name],

Thank you for reaching out. Please kindly refer to our shipping policy for detailed shipping fees:
https://www.melodysusie.com/pages/shipping-warranty

Shipping highlights:
- United States (except remote areas): $7.99, free shipping for orders over $129.99.
- Alaska, Guam, Hawaii and other US remote areas: from $12.99 for 1 product, $2.00 per additional product.
- Canada: from $16.99 for 1 product, $2.00 per additional product.
- UK, France and Germany: from $15.99 for 1 product, $2.00 per additional product.
- Free shipping for orders over $129.99 (US).

For the exact shipping fee to your location, the cost will be calculated automatically at checkout based on your order and destination.

Should you need any additional information or support, please feel free to reach out at any time.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {客户询问的国家} | 客户输入 | 客户询问运费的国家 |

> 修正：`Hello Martina`→`Hello [Customer Name]`；`Warmest Regards`→`Best regards`；原冗长逐国运费表精简为引用链接 + 要点说明。

---

#### W-PRE-06｜税费 / 关税说明

`即刻可用`｜问题分类：PRE-06｜渠道：官网｜前置条件：无  
场景：客户询问税费 / 关税。

```text
Hello,

Thank you for your inquiry. Taxes and import duties vary depending on your country's regulations. Customers are responsible for any customs fees or import taxes. We recommend checking with your local customs office to confirm any applicable charges.

For full details, please refer to our Shipping & Warranty Policy:
https://www.melodysusie.com/pages/shipping-warranty

For all international shipments (outside the contiguous United States), any taxes or duties are the responsibility of the buyer. Shipments are delivered duty unpaid, and the final cost does not include import duties or sales taxes. You may be required to pay additional charges by your local government or courier, including duties, taxes and other fees. We are not responsible for any extra charges once the package has been shipped.

We hope this helps clarify. If you have further questions, please feel free to reach out.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 固定政策说明 |

> 修正：原长段 policy 说明改为引用链接 + 精简说明。

---

#### W-PRE-07｜物流运输时效

`即刻可用`｜问题分类：PRE-07｜渠道：官网｜前置条件：无  
场景：客户问运输时间。

```text
Hello,

Thank you for reaching out.

For orders shipped to Canada, the estimated delivery time is 7–15 business days.

For your reference:
- United States: 6–12 business days
- Canada: 7–15 business days
- Germany, France, Italy, Spain, Australia, United Kingdom: 7–15 business days
- Other countries: 10–15 business days

You can find more details in our Shipping Policy here:
https://www.melodysusie.com/pages/shipping-warranty

We hope this information is helpful. Please feel free to let us know if you have any other questions.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 固定时效说明 |

> 修正：`Teameam`→`Team`。

---

## 三、售中话术（W-MID）

---

#### W-MID-01｜已发货无法改单 + 提供单号

`即刻可用`｜问题分类：MID-01｜渠道：官网｜前置条件：无  
场景：客户想取消 / 改单但订单已发货，告知无法取消并提供单号。

```text
Hello [Customer Name],

Thank you for shopping with MelodySusie. We sincerely apologize for any inconvenience caused.

We've checked your order and, unfortunately, it had already been processed and shipped before we received your cancellation request. As a result, we're unable to stop the shipment at this stage.

Please find your tracking details below for reference:
Item: {产品名}
Ship Date: {发货日期}
Estimated Delivery: {预计送达日期}
Tracking Number: {物流单号}
Carrier: {承运商}
Tracking Link: {追踪链接}
Current Status: {物流状态}

May we know if you can try to accept this item and wait for it? This is also our hot selling product and loved by many professionals and beginners alike. We truly hope you'll enjoy it as well.

However, if you still prefer to return it after delivery, please feel free to contact us and we will gladly assist you with the next steps.

Thank you for your understanding. Should you need any further assistance, please don't hesitate to reach out — we're always here to help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品名} | 订单数据 | 物流信息中的产品名 |
| {发货日期} | 物流数据 | 发出日期 |
| {预计送达日期} | 物流数据 | 预计送达 |
| {物流单号} | 物流数据 | 运单号 |
| {承运商} | 物流数据 | 物流商 |
| {追踪链接} | 物流数据 | 物流查询链接 |
| {物流状态} | 物流数据 | 当前状态 |

> 修正：`Hello[Customer Name],,`→`Hello [Customer Name],`；`andloved`→`and loved`；物流字段标注为参数；挽留话术保留。

---

#### W-MID-02｜未发货取消挽留（回复一）

`即刻可用`｜问题分类：MID-02｜渠道：官网｜前置条件：无  
场景：客户想取消未发货订单，先询问原因并挽留。

```text
Hello [Customer Name],

We've received your request to cancel order {订单号}.

Before processing the cancellation, we'd love to understand if there's anything we can do to help. If your decision is related to pricing, product question, or shipping concern, please feel free to let us know — we may be able to offer a better solution or adjust the order for you.

Your satisfaction truly matters to us, and we'd be happy to assist in any way possible.

Please let us know how you'd like to proceed.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {订单号} | 订单数据 | 官网订单号（通常 MS 开头） |

> 修正：`#[Order Number]`→`{订单号}`。

---

#### W-MID-03｜未发货确认取消（回复二）

`前置条件`｜问题分类：MID-03｜渠道：官网｜前置条件：人工确认取消操作已执行  
场景：客户坚持取消，确认取消并说明退款时效。

```text
Hello [Customer Name],

Thank you for your message, please don't worry, we will cancel your order {订单号} as you requested.

If you paid with your PayPal, please allow up to 48 hours for the transaction to appear on your PayPal account. If you paid with your card, please allow up to 7-14 business days for the bank to update the charge on your bank statement.

Sorry for the inconvenience caused and we appreciate your understanding.

Please feel free to contact us if you need further help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {订单号} | 订单数据 | 官网订单号（通常 MS 开头） |

> 修正：`#[Order Number]`→`{订单号}`；`Best Wishes`→`Best regards`；补全缺失的右括号。  
> 层级：前置条件（需人工确认取消操作已执行）。

---

#### W-MID-04｜部分取消退款

`前置条件`｜问题分类：MID-04｜渠道：官网｜前置条件：人工确认部分取消已执行  
场景：客户想取消订单中部分产品。

```text
Hello [Customer Name],

Thank you for your order!

As requested, we will cancel the item {产品名} and issue a refund of [CONFIRM:退款金额].

If you paid via PayPal, please allow up to 48 hours for the refund to appear in your PayPal account. If payment was made by credit or debit card, kindly allow 7–14 business days for your bank to process and reflect the refund on your statement.

The remaining items in your order will be shipped to your provided address as scheduled.

If you need any further assistance, please don't hesitate to reach out — we're always happy to help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品名} | 订单数据 | 取消的产品名 |
| [CONFIRM:退款金额] | 运营确认 | 退款金额（含币种）需运营确认 |

> 修正：`Hello Lisa`→`Hello [Customer Name]`；`Warm regards`→`Best regards`；产品名标注 `{产品名}`；退款金额标注 `[CONFIRM:退款金额]`；补全退款时效与结尾。  
> 层级：前置条件（需人工确认部分取消已执行）。

---

#### W-MID-05｜改地址索要信息

`即刻可用`｜问题分类：MID-05｜渠道：官网｜前置条件：无  
场景：客户想修改收货地址。

```text
Hello [Customer Name],

Thank you for shopping with MelodySusie.

To update your shipping address, could you please provide the correct details in the format below? Once received, we will manually update the information for you as soon as possible.

Name:
Address Line 1:
Address Line 2 (if applicable):
City:
State/Province:
Country:
Postal Code:
Mobile Phone Number:

We appreciate your prompt reply, as it will help us process and ship your order without delay.

If you have any questions, please feel free to let us know — we're happy to assist.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 客户按格式回填地址信息 |

> 修正：`Hello Jazmin`→`Hello [Customer Name]`；`Kind regards`→`Best regards`；补全结尾。

---

#### W-MID-06｜换产品 / 颜色确认

`即刻可用`｜问题分类：MID-06｜渠道：官网｜前置条件：无  
场景：客户想换产品或颜色。

```text
Hello,

Thank you for your order and for reaching out.

To proceed with your exchange request, please kindly let us know the item(s) you would like to receive instead. Once we have the details, we'll be happy to review the available options and follow up with you on the next steps.

If you need any recommendations or have questions about specific products, feel free to let us know — we're here to help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 客户回复想换的产品 / 颜色 |

> 修正：`arrange the exchange for you`（完成式承诺）降级为核实式 `review the available options and follow up with you on the next steps`。

---

#### W-MID-07｜加产品 Draft order

`即刻可用`｜问题分类：MID-07｜渠道：官网｜前置条件：无  
场景：客户想加产品到已有订单。

```text
Hello,

Thank you for reaching out.

We've prepared a new order for you. You can complete it using the following link:
{Draft Order链接}

Once completed, we will ship this new order along with your original order.

If you have any questions or need further assistance, please don't hesitate to contact us at any time.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {Draft Order链接} | 运营确认 | Draft order 完成下单链接 |

> 修正：`Complete Your Order` 链接标注为 `{Draft Order链接}`。

---

#### W-MID-08｜退折扣处理

`前置条件`｜问题分类：MID-08｜渠道：官网｜前置条件：人工确认折扣退款已执行  
场景：客户未使用折扣码。

```text
Hello,

Thank you for your order.

Good news — your order qualifies for a [CONFIRM:折扣额度] discount with code {折扣码}. We have processed a refund of [CONFIRM:退款金额] for you.

If you paid via PayPal, please allow up to 48 hours for the refund to appear in your account. If you paid with a card, it may take 7–14 business days for the refund to reflect on your bank statement.

If you have any questions or need assistance, please don't hesitate to reach out. We're always happy to help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| [CONFIRM:折扣额度] | 运营确认 | 折扣比例（如 10%）需运营确认 |
| {折扣码} | 运营确认 | 优惠码（如 NEW10） |
| [CONFIRM:退款金额] | 运营确认 | 退款金额需运营确认 |

> 修正：`10%`→`[CONFIRM:折扣额度]`；`$4.99`→`[CONFIRM:退款金额]`；`NEW10`→`{折扣码}`；`Yours sincerely`→`Best regards`；补全退款时效与结尾。  
> 层级：前置条件（需人工确认折扣退款已执行）。

---

#### W-MID-09｜整单物流信息回复

`即刻可用`｜问题分类：MID-09｜渠道：官网｜前置条件：无  
场景：客户询问整单物流单号（多包裹发货）。

```text
Hello,

Thank you for reaching out.

Please don't worry, your order is shipped out via 2 packages. Here is tracking info for your reference:

# PACKAGE 1: {产品名} × {数量}
Ship date: {发货日期}
Carrier Estimated Delivery Date: {预计送达日期}
Carrier: {承运商}
Carrier Tracking Number: {物流单号}
Tracking Link: {追踪链接}
Status: {物流状态}

# PACKAGE 2: {产品名} × {数量}
Ship date: {发货日期}
Carrier Estimated Delivery Date: {预计送达日期}
Carrier: {承运商}
Carrier Tracking Number: {物流单号}
Tracking Link: {追踪链接}
Status: {物流状态}

Should you need any additional information or support, please feel free to reach out at any time.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品名} | 订单数据 | 各包裹产品名（一包裹可含多产品，逐行列出） |
| {数量} | 订单数据 | 各产品数量 |
| {发货日期} | 物流数据 | 各包裹发出日期 |
| {预计送达日期} | 物流数据 | 各包裹预计送达 |
| {承运商} | 物流数据 | 各包裹物流商 |
| {物流单号} | 物流数据 | 各包裹运单号 |
| {追踪链接} | 物流数据 | 各包裹查询链接 |
| {物流状态} | 物流数据 | 各包裹当前状态 |

> 修正：所有物流字段标注为参数；`Best Regards`→`Best regards`；包裹 2 补全为同格式。

---

#### W-MID-10｜部分产品物流信息回复

`即刻可用`｜问题分类：MID-10｜渠道：官网｜前置条件：无  
场景：客户只收到部分包裹（少发 / 漏发 / 未收到）。

```text
Hello,

Thank you for reaching out.

Please don't worry, another package is still in transit:

# PACKAGE 2: {产品名} × {数量}
Tracking link: {追踪链接}
Status: {物流状态}

Should you have any questions or need assistance, feel free to reach out to us.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品名} | 订单数据 | 在途包裹产品名 |
| {数量} | 订单数据 | 产品数量 |
| {追踪链接} | 物流数据 | 在途包裹查询链接 |
| {物流状态} | 物流数据 | 在途包裹当前状态 |

> 修正：`Yours sincerely`→`Best regards`；物流字段标注为参数。

---

## 四、售后话术（W-POST）

---

#### W-POST-01｜产品售后问题

场景：客户反馈产品故障 / 损坏 / 保修。

##### 回复一（索证版）

`即刻可用`｜问题分类：POST-01｜渠道：官网｜前置条件：无

```text
Hello,

Thank you for shopping with MelodySusie. We're sorry to hear that you've experienced an issue with your order.

To better understand the situation and assist you as quickly as possible, could you please share your order number along with a short video showing the issue? This will help us evaluate the problem accurately and provide the most suitable solution for you.

We're committed to making sure you have a positive experience with our products, and we will review your case and confirm the next step.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 客户提供订单号与视频 |

> 降级：`we'll do our best to resolve this for you promptly`（含完成式承诺意味）降级为核实式 `we will review your case and confirm the next step`。

##### 回复二（确认后重发版）

`前置条件`｜问题分类：POST-01｜渠道：官网｜前置条件：人工已核实产品问题并确认重发方案  
场景：确认产品问题后，提供重发方案（配件 / 整机），并跟客户确认地址重发。

```text
Hello,

Thank you for getting in touch and for taking the time to send us a detailed video of the issue you experienced with our product.

After reviewing the video, we were able to identify that the problem is with the handpiece. We'll be arranging for a replacement to be sent your way. To make sure we send it to the correct address, could you please confirm the shipping details below?

{收件人姓名}
{地址}
{电话}

Thank you for your patience and understanding as we work to resolve this issue. We truly value your business and want to make sure you have a positive experience with our products and customer service.

If you have any further questions or concerns, please don't hesitate to reach out to us. We're always here to help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {收件人姓名} | 地址数据 | 重发收件人 |
| {地址} | 地址数据 | 重发收货地址 |
| {电话} | 地址数据 | 联系电话 |

> 说明：回复二中 `We'll be arranging for a replacement` 保留（人工已确认）；`{收件人姓名}``{地址}``{电话}` 标注为参数；补全结尾段。  
> 层级：前置条件（在保修期三个月内免费重发，超过三个月需收运费，需人工确认）。

---

#### W-POST-02｜破损 / 发错货 / 用过的

`前置条件`｜问题分类：POST-02｜渠道：官网｜前置条件：人工确认重发方案  
场景：客户反馈收到破损 / 发错 / 用过的产品。

```text
Hello,

We're very sorry to hear about your experience, and we sincerely apologize for the inconvenience and frustration this has caused you.

We take these matters seriously — receiving a used or defective item is absolutely not the standard we uphold at MelodySusie. Could you please kindly send us a photo of the items you have got, along with the packing list and shipping label? We are currently investigating this with our quality control and fulfillment team to determine how this occurred.

In the meantime, we'd like to resolve this for you as quickly as possible. We can offer you a new replacement of the item, shipped at no cost to you. Please kindly confirm the following shipping address before shipment:

{收件人姓名}
{地址}
{电话}

We truly value your trust and appreciate your patience as we work to make this right.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {收件人姓名} | 地址数据 | 重发收件人 |
| {地址} | 地址数据 | 重发收货地址 |
| {电话} | 地址数据 | 联系电话 |

> 说明：`We can offer you a new replacement` 保留（人工确认后）；参数标注；补全缺失空格。  
> 层级：前置条件（需人工确认重发方案）。

---

#### W-POST-03｜退货退款

场景：客户申请退货退款。

##### 回复一（询问原因）

`即刻可用`｜问题分类：POST-03｜渠道：官网｜前置条件：无

```text
Hello,

Thank you for contacting us regarding your request to return order {订单号}.

We respect your decision and are ready to assist you with the return process. However, before we proceed, we would appreciate the opportunity to understand the reason for your request. Your feedback is very important to us and allows us to review whether there may be a suitable solution, such as product support, an exchange, or another option that may better meet your expectations.

Please feel free to share any details you're comfortable providing. We will then handle your request promptly and in accordance with our return policy.

We look forward to your response.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {订单号} | 订单数据 | 官网订单号（通常 MS 开头） |

> 修正：`#MS136388`→`{订单号}`。

##### 回复二（退货政策 + 小礼品挽留）

`前置条件`｜问题分类：POST-03｜渠道：官网｜前置条件：人工确认挽留方案（小礼品 / 退货标签）  
场景：客户坚持退货，发退货政策并以小礼品挽留。

```text
Hello,

Thank you for shopping with MelodySusie. We sincerely apologize for any inconvenience this situation may have caused.

You are certainly welcome to return your item for a refund. However, please kindly note that for returns not related to product quality issues, the original shipping fee and return shipping costs are non-refundable. You may review our full Shipping & Warranty Policy here:
https://www.melodysusie.com/pages/shipping-warranty

To proceed, please ensure the item is in good condition and returned in its original packaging so that we can process your return smoothly. When you're ready, kindly send us photos of the product along with the packaging, and we will provide you with the return label and next steps.

That said, your satisfaction is very important to us. Before moving forward with the return, we'd like to offer an alternative solution: we can send you a gift at no additional cost, which would allow you to keep your order while avoiding the time and expense of a return. Please let us know if you would prefer this option.

We truly appreciate your understanding and look forward to your reply.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| 无 | | 固定退货政策 + 挽留文案 |

> 层级：前置条件（需人工确认挽留方案）。

---

#### W-POST-04｜妥投未收到（3 个变体）

场景：物流显示妥投但客户未收到。

##### 变体一（有妥投照片）

`前置条件`｜问题分类：POST-04｜渠道：官网｜前置条件：人工核实妥投照片与物流信息  
场景：物流有妥投照片，直接发送妥投照片与物流信息给客户。

```text
Hello [Customer Name],

Thank you for reaching out.

Please see the proof of delivery details below. Your order was shipped in one package:

Tracking link: {追踪链接}
Status: {物流状态}

Shipping Address:
{收件人姓名}
{地址}
{电话}

The proof of delivery confirms it was delivered to the same address listed above.

If you need any further assistance or have questions, please don't hesitate to contact us anytime.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {追踪链接} | 物流数据 | 妥投包裹查询链接 |
| {物流状态} | 物流数据 | 妥投状态描述（含照片） |
| {收件人姓名} | 地址数据 | 收件人 |
| {地址} | 地址数据 | 收货地址 |
| {电话} | 地址数据 | 联系电话 |

> 修正：`Hello Sonya`→`Hello [Customer Name]`；真实地址 / 物流数据参数化。  
> 层级：前置条件。

##### 变体二（无妥投照片）

`即刻可用`｜问题分类：POST-04｜渠道：官网｜前置条件：无  
场景：无妥投照片，引导客户先联系物流商 / 查看监控等方式寻找包裹。

```text
Hello,

Thank you for shopping with MelodySusie.

We understand your concern about not receiving your package, and we appreciate your patience while we look into this matter for you.

Here is the shipping information for your reference:
#1: {产品名} × {数量}
Ship date: {发货日期}
Tracking Number: {物流单号}
Carrier: {承运商}
Tracking Link: {追踪链接}
Status: {物流状态}

According to the tracking details, the package has been marked as delivered. We kindly suggest trying the following steps to help locate it:
1. Check your mailbox, porch, back door, behind plants, or with household members, neighbors, or your leasing/receiving office if applicable.
2. Contact your local post office or nearby delivery location to see if it was left there for safekeeping.
3. Review any available security or doorbell camera footage to confirm whether someone may have received it on your behalf.
4. We also recommend contacting the carrier directly with your tracking number so they can help investigate the delivery location.

We understand how important your order is to you, and we want to assure you that we are in frequent contact with our logistics partner to keep them updated about the parcel situation.

If you have not received your package, please do not hesitate to contact us for assistance.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品名} | 订单数据 | 产品名 |
| {数量} | 订单数据 | 产品数量 |
| {发货日期} | 物流数据 | 发出日期 |
| {物流单号} | 物流数据 | 运单号 |
| {承运商} | 物流数据 | 物流商 |
| {追踪链接} | 物流数据 | 查询链接 |
| {物流状态} | 物流数据 | 当前状态 |

> 修正：`Warmest regards`→`Best regards`；物流字段参数化。  
> 层级：即刻可用。

##### 变体三（三次确认未找到，带签名重发）

`前置条件`｜问题分类：POST-04｜渠道：官网｜前置条件：人工确认重发（订单 < $200 重发，> $200 需具体情况具体分析）  
场景：确认三次客户仍未找到包裹，带签名服务重发。

```text
Hello,

We hope you're doing well, and we sincerely appreciate your patience and understanding regarding your recent order.

We understand that you experienced an issue with the delivery, and we truly apologize for any inconvenience this may have caused. While lost packages are not covered under our warranty policy, we want to ensure you have a positive experience with us. As a courtesy, we have submitted a request to our shipping team to arrange a replacement shipment for you as soon as possible.

The replacement package will include:
#1: {产品名}

To ensure successful delivery, please kindly confirm that the shipping details below are correct:

Shipping Address
{收件人姓名}
{地址}
{电话}

Additionally, could you please confirm whether you will be available to sign for the package upon delivery?

We look forward to your confirmation so we can proceed promptly.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {产品名} | 订单数据 | 重发产品名 |
| {收件人姓名} | 地址数据 | 重发收件人 |
| {地址} | 地址数据 | 重发收货地址 |
| {电话} | 地址数据 | 联系电话 |

> 修正：`Warm regards`→`Best regards`；真实产品 / 地址参数化。  
> 层级：前置条件（需人工确认重发方案）。

---

#### W-POST-05｜物流延迟 / 被退回 / 无法投递

`即刻可用`｜问题分类：POST-05｜渠道：官网｜前置条件：无  
场景：物流异常（延迟 / 退回 / 无更新 / 无法投递）。

```text
Hello,

Thank you for reaching out, and we sincerely apologize for the delay in your delivery.

After checking, it appears your order was not successfully delivered. To ensure we can send a replacement promptly, could you please confirm that the shipping address below is correct:

{收件人姓名}
{地址}
{电话}

Once we have your confirmation, we'll arrange for a new replacement to be shipped right away.

If you need any further assistance, please don't hesitate to contact us — we're always happy to help.

Best regards,
MelodySusie Customer Service Team
```

| 参数 | 类型 | 说明 |
|---|---|---|
| {收件人姓名} | 地址数据 | 收件人 |
| {地址} | 地址数据 | 收货地址 |
| {电话} | 地址数据 | 联系电话 |

> 说明：`we'll arrange for a new replacement to be shipped right away` 保留（因这是确认地址后执行重发的场景）；真实地址参数化。  
> 层级：即刻可用（确认地址后由人工执行重发并索赔）。

---

## 五、附录：模板层级速查表

| 编码 | 名称 | 层级 | 关键参数 |
|---|---|---|---|
| W-PRE-01 | 延保注册引导 | 即刻可用 | 无 |
| W-PRE-02 | 产品参数查询回复 | 即刻可用 | {产品型号}{扭矩}{转速范围} |
| W-PRE-03 | 产品推荐引导对比页 | 即刻可用 | 无 |
| W-PRE-04 | 物流配送可用性确认 | 即刻可用 | {客户询问的国家} |
| W-PRE-05 | 物流费用查询 | 即刻可用 | {客户询问的国家} |
| W-PRE-06 | 税费 / 关税说明 | 即刻可用 | 无 |
| W-PRE-07 | 物流运输时效 | 即刻可用 | 无 |
| W-MID-01 | 已发货无法改单 + 提供单号 | 即刻可用 | {产品名}{发货日期}{预计送达日期}{物流单号}{承运商}{追踪链接}{物流状态} |
| W-MID-02 | 未发货取消挽留（回复一） | 即刻可用 | {订单号} |
| W-MID-03 | 未发货确认取消（回复二） | 前置条件 | {订单号} |
| W-MID-04 | 部分取消退款 | 前置条件 | {产品名}[CONFIRM:退款金额] |
| W-MID-05 | 改地址索要信息 | 即刻可用 | 无 |
| W-MID-06 | 换产品 / 颜色确认 | 即刻可用 | 无 |
| W-MID-07 | 加产品 Draft order | 即刻可用 | {Draft Order链接} |
| W-MID-08 | 退折扣处理 | 前置条件 | [CONFIRM:折扣额度]{折扣码}[CONFIRM:退款金额] |
| W-MID-09 | 整单物流信息回复 | 即刻可用 | 物流全套参数 |
| W-MID-10 | 部分产品物流信息回复 | 即刻可用 | {产品名}{数量}{追踪链接}{物流状态} |
| W-POST-01 回复一 | 产品售后问题（索证版） | 即刻可用 | 无 |
| W-POST-01 回复二 | 产品售后问题（重发版） | 前置条件 | {收件人姓名}{地址}{电话} |
| W-POST-02 | 破损 / 发错货 / 用过的 | 前置条件 | {收件人姓名}{地址}{电话} |
| W-POST-03 回复一 | 退货退款（询问原因） | 即刻可用 | {订单号} |
| W-POST-03 回复二 | 退货退款（政策 + 挽留） | 前置条件 | 无 |
| W-POST-04 变体一 | 妥投未收到（有照片） | 前置条件 | {追踪链接}{物流状态}{收件人姓名}{地址}{电话} |
| W-POST-04 变体二 | 妥投未收到（无照片） | 即刻可用 | 物流全套参数 |
| W-POST-04 变体三 | 妥投未收到（重发） | 前置条件 | {产品名}{收件人姓名}{地址}{电话} |
| W-POST-05 | 物流延迟 / 退回 / 无法投递 | 即刻可用 | {收件人姓名}{地址}{电话} |
