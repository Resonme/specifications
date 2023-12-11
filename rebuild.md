## 微信H5、小程序重构内容
------------
#### 命名规范
  * 文件
  * javascript
  * 样式

#### 语言国际化 lang
  * en.json
  * zh.json

#### 枚举 enu
  * 用户性别、孕状、婚姻
  * 体检状态
  * 预约类型
  * 预约状态
  * 支付类型
  * 支付状态
  * 会员等级
  * ... 

#### 工具集
  * utils 工具集合
  * enc 加密解密
  * request 请求
  * storage 缓存
  * validate 校验
  * qrcode 二维码
  * pay 支付

#### icons 图片管理

#### icons 图标

#### style 样式
  * 全局样式
  * 样式变量

#### store 全局状态 + 缓存 localStorage
  * 系统参数 systemParams
    * 页面布局样式相关
    * 文本配置
    * 预约相关
    * 套餐相关
    * 加项相关
    * 订单相关
  * 系统环境信息 system
    * 系统版本信息
    * 系统主题
  * 系统运行环境
    * 系统时间
    * 上次发送验证码时间
  * 医院信息 hospitalInfo
    * 医院配置信息
  * 用户信息 userInfo
    * 个人信息
    * 登入、登出
    * 会员信息
  * 操作订单信息
    * 套餐信息
    * 项目列表
    * 预约用户
    * 预约时间

#### module 全局组件模块
  * components
    * 车牌号
    * 图表
    * 签名
    * PDF预览
    * form相关 下拉、省市区、图片/拍照、
    * dialog弹窗相关 toast、alert、confirm、dialog
    * 状态页面 成功、异常、无数据

  * mixins
    * lang 语言
    * 问卷相关
    * 项目相关 套餐、组合项目、推荐包
  * directive
  * filters

#### api 模块管理
  * 系统
    * 系统参数
    * 系统版本
  * 用户
    * 用户信息相关
    * 用户会员卡相关
  * 医院
    * 医院相关
  * 套餐
  * 项目
  * 订单

#### router 路由
  * 系统
  * 用户
  * 医院
  * 套餐
  * 项目
  * 订单

