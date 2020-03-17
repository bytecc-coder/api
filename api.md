
 <h1 class="curproject-name"> tps_web </h1> 
 


# 公共分类

## login
<a id=login> </a>
### 基本信息

**Path：** /login

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| username | 是  |  admin |   |
| password | 是  |  admin12345 |   |
| captcha | 是  |  abc |   |

### 返回数据

<table>
  <thead class="ant-table-thead">
    <tr>
      <th key=name>名称</th><th key=type>类型</th><th key=required>是否必须</th><th key=default>默认值</th><th key=desc>备注</th><th key=sub>其他信息</th>
    </tr>
  </thead><tbody className="ant-table-tbody"><tr key=0-0><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> code</span></td><td key=1><span>number</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5><p key=5><span style="font-weight: '700'">undefined: </span><span>200</span></p></td></tr><tr key=0-1><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> result</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-1-0><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> token</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5><p key=5><span style="font-weight: '700'">undefined: </span><span>asdasdadadadadadadadsad</span></p></td></tr><tr key=0-1-1><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> username</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5><p key=5><span style="font-weight: '700'">undefined: </span><span>admin</span></p></td></tr><tr key=0-1-2><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> role</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5><p key=5><span style="font-weight: '700'">undefined: </span><span>admin</span></p></td></tr>
               </tbody>
              </table>
            
# admin

## 学院方向添加
<a id=学院方向添加> </a>
### 基本信息

**Path：** /major/add

**Method：** POST

**接口描述：**


### 请求参数
**Headers**

| 参数名称  | 参数值  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ | ------------ |
| Content-Type  |  application/x-www-form-urlencoded | 是  |   |   |
**Body**

| 参数名称  | 参数类型  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ | ------------ |
| collegeDirectionName | text  |  是 |  软件开发与测试  |   |



### 返回数据

```javascript
{"code":200}
```
## 按讲座汇总
<a id=按讲座汇总> </a>
### 基本信息

**Path：** /auth/getLectureSelectedData

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| companyId | 否  |   |  企业id |
| lectureName | 否  |   |  讲座名称 |
| from | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

```javascript
{"type":"object","title":"empty object","properties":{"code":{"type":"string"},"result":{"type":"object","properties":{"records":{"type":"object","properties":{"lectureId":{"type":"string","description":"讲座Id"},"companyName":{"type":"string","description":"企业名称"},"lectureName":{"type":"string","description":"讲座名称"},"selectedNum":{"type":"number","description":"选择人数"},"lectureAddress":{"type":"string","description":"讲座地址（可以为空）"},"lectureStatus":{"type":"number","description":"0：未开始；1：进行中；2：已完成"},"startedAt":{"type":"string","description":"讲座开始时间"},"endedAt":{"type":"string","description":"讲座结束时间"}},"required":["lectureId","companyName","lectureName","selectedNum","lectureAddress","lectureStatus","startedAt","endedAt"]}},"required":["records"]}},"required":["code","result"]}
```
## 获取学院方向
<a id=获取学院方向> </a>
### 基本信息

**Path：** /auth/getCollegeDirection

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| form | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

<table>
  <thead class="ant-table-thead">
    <tr>
      <th key=name>名称</th><th key=type>类型</th><th key=required>是否必须</th><th key=default>默认值</th><th key=desc>备注</th><th key=sub>其他信息</th>
    </tr>
  </thead><tbody className="ant-table-tbody"><tr key=0-0><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> result</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-0-0><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> records</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-0-0-0><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> collegeDirectionId</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-0-0-1><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> collegeDirectionName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr>
               </tbody>
              </table>
            
## 获取学院班级
<a id=获取学院班级> </a>
### 基本信息

**Path：** /auth/getCollegeClass

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| from | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

```javascript
{ "code": 200,"result": {"records": [{"collegeClassId":"001","collegeClassName":"16140A02","collegeDirectionId": "001","collegeDirectionName": "软件开发与测试" }]}}
```
## 获取实训方向
<a id=获取实训方向> </a>
### 基本信息

**Path：** /auth/getTrainingDirection

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| from | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

```javascript
{"code":200,"result":{"records":[{"trainingDirectionId": "001","trainingDirectionName": "全栈开发"}]}}
```
## 获取方向选择控制
<a id=获取方向选择控制> </a>
### 基本信息

**Path：** /auth/getControls

**Method：** GET

**接口描述：**


### 请求参数

### 返回数据

<table>
  <thead class="ant-table-thead">
    <tr>
      <th key=name>名称</th><th key=type>类型</th><th key=required>是否必须</th><th key=default>默认值</th><th key=desc>备注</th><th key=sub>其他信息</th>
    </tr>
  </thead><tbody className="ant-table-tbody"><tr key=0-0><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> result</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-0-0><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> records</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-0-0-0><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> controlValue</span></td><td key=1><span>number</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">0:关闭；1：开启</span></td><td key=5></td></tr><tr key=0-0-0-1><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> controlId</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-0-0-2><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> controlName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">（讲座选择，方向选择，方向确认）</span></td><td key=5></td></tr>
               </tbody>
              </table>
            
## 获取未来计划
<a id=获取未来计划> </a>
### 基本信息

**Path：** /auth/getPlan

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| from | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

```javascript
{"code":200,"result":{"records":[{"planId": "001","planName": "考研"}]}}
```
## 讲座选择已完成
<a id=讲座选择已完成> </a>
### 基本信息

**Path：** /auth/getFinishedLecture

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| studentName | 否  |   |  学生姓名 |
| collegeClassId | 否  |   |  学院班级id |
| from | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

<table>
  <thead class="ant-table-thead">
    <tr>
      <th key=name>名称</th><th key=type>类型</th><th key=required>是否必须</th><th key=default>默认值</th><th key=desc>备注</th><th key=sub>其他信息</th>
    </tr>
  </thead><tbody className="ant-table-tbody"><tr key=0-0><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> code</span></td><td key=1><span>number</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">200</span></td><td key=5></td></tr><tr key=0-1><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> result</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-1-0><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> records</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-1-0-0><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> collegeClassName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">班级</span></td><td key=5></td></tr><tr key=0-1-0-1><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> sno</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">学号</span></td><td key=5></td></tr><tr key=0-1-0-2><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> studentName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">姓名</span></td><td key=5></td></tr><tr key=0-1-0-3><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> selectedLectureName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">已选讲座</span></td><td key=5></td></tr>
               </tbody>
              </table>
            
## 讲座选择未完成
<a id=讲座选择未完成> </a>
### 基本信息

**Path：** /auth/getNoFinishedLecture

**Method：** GET

**接口描述：**


### 请求参数
**Query**

| 参数名称  |  是否必须 | 示例  | 备注  |
| ------------ | ------------ | ------------ | ------------ |
| studentName | 否  |   |  学生姓名 |
| collegeClassId | 否  |   |  学院班级ID |
| from | 是  |   |   |
| limit | 是  |   |   |

### 返回数据

<table>
  <thead class="ant-table-thead">
    <tr>
      <th key=name>名称</th><th key=type>类型</th><th key=required>是否必须</th><th key=default>默认值</th><th key=desc>备注</th><th key=sub>其他信息</th>
    </tr>
  </thead><tbody className="ant-table-tbody"><tr key=0-0><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> code</span></td><td key=1><span>number</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">200</span></td><td key=5></td></tr><tr key=0-1><td key=0><span style="padding-left: 0px"><span style="color: #8c8a8a"></span> result</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-1-0><td key=0><span style="padding-left: 20px"><span style="color: #8c8a8a">├─</span> records</span></td><td key=1><span>object</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap"></span></td><td key=5></td></tr><tr key=0-1-0-0><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> collegeClassName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">班级</span></td><td key=5></td></tr><tr key=0-1-0-1><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> sno</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">学号</span></td><td key=5></td></tr><tr key=0-1-0-2><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> studentName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">学生姓名</span></td><td key=5></td></tr><tr key=0-1-0-3><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> selectedLectureName</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">已选讲座</span></td><td key=5></td></tr><tr key=0-1-0-4><td key=0><span style="padding-left: 40px"><span style="color: #8c8a8a">├─</span> noSelectSum</span></td><td key=1><span>string</span></td><td key=2>必须</td><td key=3></td><td key=4><span style="white-space: pre-wrap">未选数量</span></td><td key=5></td></tr>
               </tbody>
              </table>
            