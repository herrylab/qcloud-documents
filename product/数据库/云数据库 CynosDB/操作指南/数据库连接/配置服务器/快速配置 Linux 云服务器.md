云服务器（Cloud Virtual Machine，CVM）是腾讯云提供的可扩展的计算服务。使用云服务器避免了使用传统服务器时需要预估资源用量及前期投入，帮助您在短时间内快速启动任意数量的云服务器并即时部署应用程序。

本文为您介绍如何从零开始，以最简单的方式搭建一个 Linux 云服务器。您可按照以下文档，购买和配置您的第一台云服务器。若想了解搭建 Windows 云服务器的入门教程，可以参考 [快速配置 Windows 云服务器](https://cloud.tencent.com/document/product/1003/79662)。

## 前提条件
已注册腾讯云账号，详细方法请参见 [注册腾讯云账号](https://cloud.tencent.com/document/product/378/17985)。

## 配置 Linux 云服务器
>!为确保成功连接到 TDSQL-C MySQL 版，建议购买的云服务器 CVM 与 TDSQL-C MySQL 版满足以下几点：
>- CVM 和 TDSQL-C MySQL 版属于同一个腾讯云主账号。
>- CVM 和 TDSQL-C MySQL 版位于同一地域。
>- CVM 和 TDSQL-C MySQL 版的网络类型都是 VPC 且处于同一个 VPC 内。
>

### 步骤一：购买 Linux 云服务器
1. 进入 [快速购买页面](https://buy.cloud.tencent.com/cvm?tab=lite&ltCreateMode=createLt)。
2. 在购买页 > **快速配置**分页，完成云服务器配置后，单击**立即购买**。
![](https://qcloudimg.tencent-cloud.cn/raw/a58a744f2aad1103cd09263b6efbf573.png)
配置说明如下：
<table>
<thead><tr><th>配置项</th><th>说明</th></tr></thead>
<tr>
<td>地域</td>
<td>选择与您的 TDSQL-C MySQL 版集群所在同一个地域。</td></tr>
<tr>
<td>实例</td>
<td>选择您需要的云服务器机型配置。这里我们选择 “普及配置（2核4GB）”。 </td></tr>
<tr>
<td>操作系统</td>
<td>选择您需要的云服务器操作系统。这里我们选择 “CentOS 8.2 64位”。</td></tr>
<tr>
<td>公网 IP</td>
<td>勾选后会为您分配公网 IP，默认公网带宽为 “1Mbps”，您可以根据需求调整。</td></tr>
<tr>
<td>登录方式</td>
<td>自动生成的密码将在服务器创建完成后通过 <a href="https://console.cloud.tencent.com/message">站内信</a> 发送。</td></tr>
<tr>
<td>默认配置</td>
<td>可展开查看可用区、安全组等6项默认配置。</td></tr>
<tr>
<td>自动续费</td>
<td>勾选后，若账户余额足够，则将在云服务器到期时按月自动续费。</td></tr>
<tr>
<td>协议</td>
<td>查阅并了解相关协议后勾选。</td></tr>
<tr>
<td>时长</td>
<td>购买时长，默认为 “1个月”。</td></tr>
<tr>
<td>数量</td>
<td>购买数量，默认为 “1台”。</td></tr>
</table>


当您付费完成后，即完成了云服务器的购买。云服务器可以作为个人虚拟机或者您建站的服务器。接下来，您可以登录您购买的这台服务器。

### 步骤二：登录云服务器
>!通过快速配置购买的云服务器，系统将为您自动分配云服务器登录密码并发送到您的站内信中。此密码为登录云服务器的凭据。您可至 [站内信](https://console.cloud.tencent.com/message) 查收您的密码。

1. 登录 [云服务器控制台](https://console.cloud.tencent.com/cvm/instance/index)，在上方选择地域。
2. 在实例列表中找到您刚购买的云服务器，在右侧操作栏中单击**登录**。
![](https://qcloudimg.tencent-cloud.cn/raw/c8f41067fb79d5b3f1d7e1c28f05e4f0.png)
3. 在“标准登录 | Linux 实例”窗口中，输入**云服务器**的用户名（默认为 root）和密码，并单击登录即可正常登录。如下图所示：
![](https://qcloudimg.tencent-cloud.cn/raw/4570580bc15ccd130a191e134301f562.png)
4. 登录成功后，界面如下图所示：
![](https://qcloudimg.tencent-cloud.cn/raw/bbbfc31304bcea7389f86577f65b4b0e.png)
