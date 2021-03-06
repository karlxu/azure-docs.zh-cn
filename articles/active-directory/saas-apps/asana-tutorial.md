---
title: 教程：Azure Active Directory 与 Asana 集成 | Microsoft Docs
description: 了解如何在 Azure Active Directory 和 Asana 之间配置单一登录。
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.reviewer: joflore
ms.assetid: 837e38fe-8f55-475c-87f4-6394dc1fee2b
ms.service: active-directory
ms.component: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 05/10/2018
ms.author: jeedes
ms.openlocfilehash: b60f80353a6c2a67c5c1602987ba06aad8bd38e1
ms.sourcegitcommit: 16ddc345abd6e10a7a3714f12780958f60d339b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36224821"
---
# <a name="tutorial-azure-active-directory-integration-with-asana"></a>教程：Azure Active Directory 与 Asana 集成

在本教程中，了解如何将 Asana 与 Azure Active Directory (Azure AD) 集成。

将 Asana 与 Azure AD 集成提供以下优势：

- 可在 Azure AD 中控制谁有权访问 Asana
- 可使用户通过其 Azure AD 帐户自动登录 Asana（单一登录）
- 可以在一个中心位置（即 Azure 门户）管理帐户

如需了解有关 SaaS 应用与 Azure AD 集成的详细信息，请参阅 [Azure Active Directory 的应用程序访问与单一登录是什么](../manage-apps/what-is-single-sign-on.md)。

## <a name="prerequisites"></a>先决条件

若要配置 Azure AD 与 Asana 的集成，需要以下项目：

- Azure AD 订阅
- 已启用 Asana 单一登录的订阅

> [!NOTE]
> 为了测试本教程中的步骤，我们不建议使用生产环境。

测试本教程中的步骤应遵循以下建议：

- 除非必要，请勿使用生产环境。
- 如果没有 Azure AD 试用环境，可以[获取一个月的试用版](https://azure.microsoft.com/pricing/free-trial/)。

## <a name="scenario-description"></a>方案描述
在本教程中，将在测试环境中测试 Azure AD 单一登录。
本教程中概述的方案包括两个主要构建基块：

1. 从库中添加 Asana
2. 配置和测试 Azure AD 单一登录

## <a name="adding-asana-from-the-gallery"></a>从库中添加 Asana
要配置 Asana 与 Azure AD 的集成，需要将库中的 Asana 添加到托管的 SaaS 应用列表。

**若要从库中添加 Asana，请执行以下步骤：**

1. 在 **[Azure 门户](https://portal.azure.com)** 的左侧导航面板中，单击“Azure Active Directory”图标。 

    ![“Azure Active Directory”按钮][1]

2. 导航到“企业应用程序”。 然后转到“所有应用程序”。

    ![“企业应用程序”边栏选项卡][2]

3. 若要添加新应用程序，请单击对话框顶部的“新建应用程序”按钮。

    ![“新增应用程序”按钮][3]

4. 在搜索框中，键入“Asana”，在结果面板中选择“Asana”，然后单击“添加”按钮添加该应用程序。

    ![创建 Azure AD 测试用户](./media/asana-tutorial/tutorial_asana_addfromgallery.png)

## <a name="configure-and-test-azure-ad-single-sign-on"></a>配置和测试 Azure AD 单一登录

在本部分中，基于名为“Britta Simon”的测试用户配置和测试 Asana 的 Azure AD 单一登录。

为了成功实现单一登录，Azure AD 需要知道 Azure AD 用户在 Asana 中的对应用户。 换句话说，需要建立 Azure AD 用户与 Asana 中相关用户之间的链接关系。

可通过将 Azure AD 中“用户名”的值指定为 Asana 中“用户名”的值来建立此关联关系。

若要通过 Asana 配置和测试 Azure AD 单一登录，需要完成以下构建基块：

1. **[配置 Azure AD 单一登录](#configure-azure-ad-single-sign-on)** - 使用户能够使用此功能。
2. **[创建 Azure AD 测试用户](#create-an-azure-ad-test-user)** - 使用 Britta Simon 测试 Azure AD 单一登录。
3. [创建 Asana 测试用户](#create-an-asana-test-user) - 在 Asana 中创建 Britta Simon 的对应用户，并将其链接到用户的 Azure AD 表示形式。
4. **[分配 Azure AD 测试用户](#assign-the-azure-ad-test-user)** - 使 Britta Simon 能够使用 Azure AD 单一登录。
5. **[测试单一登录](#test-single-sign-on)** - 验证配置是否正常工作。

### <a name="configure-azure-ad-single-sign-on"></a>配置 Azure AD 单一登录

在本部分中，将在 Azure 门户中启用 Azure AD 单一登录并在 Asana 应用程序中配置单一登录。

**若要配置 Asana 的 Azure AD 单一登录，请执行以下步骤：**

1. 在 Azure 门户中的 Asana 应用程序集成页上，单击“单一登录”。

    ![配置单一登录][4]

2. 在“单一登录”对话框中，选择“基于 SAML 的单一登录”作为“模式”以启用单一登录。

    ![“单一登录”对话框](./media/asana-tutorial/tutorial_asana_samlbase.png)

3. 在“Asana 域和 URL”部分中，执行以下步骤：

    ![Asana 域和 URL 单一登录信息](./media/asana-tutorial/tutorial_asana_url.png)

    a. 在“登录 URL”文本框中，键入 URL：`https://app.asana.com/`

    b. 在“标识符”文本框中，键入值：`https://app.asana.com/`

4. 在“SAML 签名证书”部分中，单击“证书(base64)”，并在计算机上保存证书文件。

    ![证书下载链接](./media/asana-tutorial/tutorial_asana_certificate.png)

5. 单击“保存”按钮。

    ![配置单一登录“保存”按钮](./media/asana-tutorial/tutorial_general_400.png)

6. 在“Asana 配置”部分，单击“配置 Asana”打开“配置登录”窗口。 从“快速参考”部分中复制“SAML 单一登录服务 URL”

    ![Asana 配置](./media/asana-tutorial/tutorial_asana_configure.png)

7. 在其他浏览器窗口中，登录 Asana 应用程序。 若要在 Asana 中配置 SSO，请单击屏幕右上角的工作区名称，访问工作区设置。 然后，单击“\<工作区名称\> 设置”。

    ![Asana SSO 设置](./media/asana-tutorial/tutorial_asana_09.png)

8. 在“组织设置”窗口中，单击“管理”。 然后，单击“成员必须通过 SAML 登录”，启用 SSO 配置。 然后执行以下步骤：

    ![配置单一登录组织设置](./media/asana-tutorial/tutorial_asana_10.png)  

     a. 在“登录页 URL”文本框中，粘贴“SAML 单一登录服务 URL”。

     b. 右键单击从 Azure 门户下载的证书，然后使用记事本或首选文本编辑器打开证书文件。 复制证书开始和结束标题之间的内容，并将其粘贴在“X.509 证书”文本框中。

9. 单击“ **保存**”。 如果需要进一步的协助，请转到 [“设置 SSO 的 Asana 指南”](https://asana.com/guide/help/premium/authentication#gl-saml)。

### <a name="create-an-azure-ad-test-user"></a>创建 Azure AD 测试用户

本部分的目的是在 Azure 门户中创建名为 Britta Simon 的测试用户。

![创建 Azure AD 测试用户][100]

**若要在 Azure AD 中创建测试用户，请执行以下步骤：**

1. 在 **Azure 门户**的左侧导航窗格中，单击“Azure Active Directory”图标。

    ![“Azure Active Directory”按钮](./media/asana-tutorial/create_aaduser_01.png) 

2. 若要显示用户列表，请转到“用户和组”，单击“所有用户”。

    ![“用户和组”以及“所有用户”链接](./media/asana-tutorial/create_aaduser_02.png)

3. 若要打开“用户”对话框，请在对话框顶部单击“添加”。

    ![创建 Azure AD 测试用户](./media/asana-tutorial/create_aaduser_03.png)

4. 在“用户”对话框页上，执行以下步骤：

    ![“添加”按钮](./media/asana-tutorial/create_aaduser_04.png)

    a. 在“名称”文本框中，键入 **BrittaSimon**。

    b. 在“用户名”文本框中，键入 BrittaSimon 的“电子邮件地址”。

    c. 选择“显示密码”并记下“密码”的值。

    d. 单击“创建”。

### <a name="create-an-asana-test-user"></a>创建 Asana 测试用户

本部分的目的是在 Asana 中创建名为“Britta Simon”的用户。 Asana 支持在默认情况下启用的自动用户预配。 有关如何配置自动用户预配的更多详细信息，请参见[此处](asana-provisioning-tutorial.md)。

如果需要手动创建用户，请执行以下步骤：

在本部分中，创建 Asana 中名为“Britta Simon”的用户。

1. 在“Asana”上，转到左侧窗格上的“团队”部分。 单击加号按钮。

    ![创建 Azure AD 测试用户](./media/asana-tutorial/tutorial_asana_12.png)

2. 在文本框中键入电子邮件 britta.simon@contoso.com，并选择“邀请”。

3. 单击“发送邀请”。 新用户会在电子邮件帐户中收到电子邮件。 她需要创建并验证该帐户。

### <a name="assign-the-azure-ad-test-user"></a>分配 Azure AD 测试用户

在本部分中，通过向 Britta Simon 授予 Asana 的访问权限支持她使用 Azure 单一登录。

![分配用户角色][200]

**要将 Britta Simon 分配到 Asana，请执行以下步骤：**

1. 在 Azure 门户中打开应用程序视图，导航到目录视图，接着转到“企业应用程序”，并单击“所有应用程序”。

    ![分配用户][201]

2. 在应用程序列表中选择“Asana”。

    ![应用程序列表中的 Asana 链接](./media/asana-tutorial/tutorial_asana_app.png)

3. 在左侧菜单中，单击“用户和组”。

    ![“用户和组”链接][202]

4. 单击“添加”按钮。 然后在“添加分配”对话框中选择“用户和组”。

    ![“添加分配”窗格][203]

5. 在“用户和组”对话框的“用户”列表中，选择“Britta Simon”。

6. 在“用户和组”对话框中单击“选择”按钮。

7. 在“添加分配”对话框中单击“分配”按钮。

### <a name="test-single-sign-on"></a>测试单一登录

本部分旨在测试 Azure AD 单一登录。

请转到 Asana 登录页。 在电子邮件地址文本框中，插入电子邮件地址 britta.simon@contoso.com。 将密码文本框留空，然后单击“登录”。 系统会你将重定向至 Azure AD 登录页。 完成 Azure AD 凭据。 此时已登录 Asana。

## <a name="additional-resources"></a>其他资源

* [有关如何将 SaaS 应用与 Azure Active Directory 集成的教程列表](tutorial-list.md)
* [什么是使用 Azure Active Directory 的应用程序访问和单一登录？](../manage-apps/what-is-single-sign-on.md)
* [配置用户预配](asana-provisioning-tutorial.md)

<!--Image references-->

[1]: ./media/asana-tutorial/tutorial_general_01.png
[2]: ./media/asana-tutorial/tutorial_general_02.png
[3]: ./media/asana-tutorial/tutorial_general_03.png
[4]: ./media/asana-tutorial/tutorial_general_04.png

[100]: ./media/asana-tutorial/tutorial_general_100.png

[200]: ./media/asana-tutorial/tutorial_general_200.png
[201]: ./media/asana-tutorial/tutorial_general_201.png
[202]: ./media/asana-tutorial/tutorial_general_202.png
[203]: ./media/asana-tutorial/tutorial_general_203.png
[10]: ./media/asana-tutorial/tutorial_general_060.png
[11]: ./media/asana-tutorial/tutorial_general_070.png