---
title: 使用命令行参数安装 Visual Studio |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-install
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- command-line parameters
- switches
- command prompt
ms.assetid: 480f3cb4-d873-434e-a8bf-82cff7401cf2
caps.latest.revision: 10
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 6266626d2eb60b64f1923a0c3f54d39c9b20072a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/12/2018
ms.locfileid: "49268601"
---
# <a name="use-command-line-parameters-to-install-visual-studio"></a>使用命令行参数安装 Visual Studio
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio 2017 的最新文档，请参阅[使用命令行参数安装 Visual Studio 2017](https://docs.microsoft.com/visualstudio/install/use-command-line-parameters-to-install-visual-studio)。

当从命令提示符安装 Visual Studio 2015 时，可以使用以下命令行参数 （也称为开关）。  
  
> [!NOTE]
>  请确保使用实际的安装程序而不是引导程序文件。 例如，请确保你使用**`vs_enterprise.exe`** 而不是 vs_enterprise_*GUID*.exe。 您可以下载的安装程序从[My.VisualStudio.com](https://my.visualstudio.com/downloads?q=visual%20studio%20enterprise%202015)。  
  
## <a name="list-of-command-line-parameters"></a>命令行参数列表  
 Visual Studio 命令行参数不区分大小写。  
  
|参数|描述|  
|---------------|-----------------|  
|**/?**<br /><br /> **/help**<br /><br /> **/h**|显示命令行参数。|  
|**/ AddRemoveFeatures**|指定要在安装的产品中添加或移除的功能。|  
|**/ AdminFile** *AdminDeployment.xml*|使用你为管理安装指定的数据文件安装 Visual Studio。|  
|**/ ChainingPackage** *BundleName*|指定此捆绑包链接到的捆绑包。 还可用于指定客户改善体验队列。|  
|**/ CreateAdminFile\<文件名 >**|指定用于创建可与 /AdminFile 一起使用的控制文件的位置|  
|**/ CustomInstallPath** *InstallationDirectory*|在你指定的目录中安装所有可重定目标的包。|  
|**/ ForceRestart**|安装完成后始终重新启动计算机。|  
|**/ 完整**|安装所有产品功能。|  
|**/Installselectableitems\<项名称 > [;\<项名称 2 >]**|要在安装程序向导选择屏幕上检查的选择树项列表。|  
|**/l**<br /><br /> **/ 日志***文件名*|指定日志文件的位置。|  
|**/layout** *目录*|将安装媒体上的文件复制到你指定的目录。|  
|**/ NoCacheOnlyMode**|阻止包缓存的预填充。|  
|**/ NoRefresh**|禁止检查此产品的较新版本是否存在必需或推荐的更新版本。|  
|**/norestart**|在安装期间或安装完成后，阻止安装应用程序重新启动计算机。 请参阅的返回代码部分[Visual Studio 管理员指南](../install/visual-studio-administrator-guide.md)要查找的返回代码。|  
|**/noweb**|阻止从 Internet 中安装。|  
|**/ OverrideFeedUri\<馈送文件的路径 >**|本地外部源的路径，它描述软件项|  
|**/ ProductKey**<br /><br /> *ProductKey*|设置不包含短划线且不超过 25 个字符的自定义产品密钥。|  
|**/ Promptrestart 一起使用**|在重新启动计算机之前提示用户。|  
|**/q**<br /><br /> **/quiet**<br /><br /> **/s**<br /><br /> **/Silent**|取消安装应用程序的用户界面 (UI)。 如果已安装 Visual Studio，并且你除了这个参数之外未指定任何参数，则在维护模式下运行安装应用程序。|  
|**/qb**<br /><br /> **/passive**|显示进度，但不等待用户输入。|  
|**/repair**|修复 Visual Studio。|  
|**/ SuppressRefreshPrompt**|禁止在安装向导中显示更新可用对话框，因此安装向导将自动接受任意必需或推荐更新版本。|  
|**/u**<br /><br /> **/ 卸载**|卸载 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]。|  
|**/Uninstall /Force**<br /><br /> **/u /force**|卸载 Visual Studio 以及与其他产品共享的所有功能。 **警告：** 使用此参数，如果同一台计算机安装其他产品可能会停止正常运行。|  
  
## <a name="see-also"></a>请参阅  
 [Visual Studio 管理员指南](../install/visual-studio-administrator-guide.md)