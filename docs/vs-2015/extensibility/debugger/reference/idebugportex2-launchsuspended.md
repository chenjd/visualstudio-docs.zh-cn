---
title: IDebugPortEx2::LaunchSuspended |Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugPortEx2::LaunchSuspended
helpviewer_keywords:
- IDebugPortEx2::LaunchSuspended
ms.assetid: 34b2cf99-2e52-4757-8969-1d12ac517ec0
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 652dca7c8d17a2572119146af57663cfa22fb730
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/23/2018
ms.locfileid: "49937000"
---
# <a name="idebugportex2launchsuspended"></a>IDebugPortEx2::LaunchSuspended
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

启动可执行文件。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT LaunchSuspended(   
   LPCOLESTR        pszExe,  
   LPCOLESTR        pszArgs,  
   LPCOLESTR        pszDir,  
   BSTR             bstrEnv,  
   DWORD            hStdInput,  
   DWORD            hStdOutput,  
   DWORD            hStdError,  
   IDebugProcess2** ppPortProcess  
);  
```  
  
```csharp  
int LaunchSuspended(   
   string             pszExe,  
   string             pszArgs,  
   string             pszDir,  
   string             bstrEnv,  
   uint               hStdInput,  
   uint               hStdOutput,  
   uint               hStdError,  
   out IDebugProcess2 ppPortProcess  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pszExe`  
 [in]若要启动的可执行文件的名称。 这可以是完整路径或相对于工作目录中指定`pszDir`参数。  
  
 `pszArgs`  
 [in]要传递给可执行文件的参数。 如果没有任何自变量可能为 null 值。  
  
 `pszDir`  
 [in]使用的可执行文件的工作目录的名称。 如果没有工作目录是必需的可能为 null 值。  
  
 `bstrEnv`  
 [in]以 null 结尾的字符串后, 跟其他的 NULL 结束符的环境块。  
  
 `hStdInput`  
 [in]其他输入流的句柄。 如果不需要重定向，则可能为 0。  
  
 `hStdOutput`  
 [in]备用输出流的句柄。 如果不需要重定向，则可能为 0。  
  
 `hStdError`  
 [in]备用错误输出流的句柄。 如果不需要重定向，则可能为 0。  
  
 `ppPortProcess`  
 [out]返回[IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)对象，表示启动的进程。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 此方法应启动的过程，以便它处于挂起状态和未运行任何代码。 [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)调用方法来继续执行过程。  
  
 此外可以从调试引擎启动程序。 有关详细信息，请参阅[启动程序](../../../extensibility/debugger/launching-a-program.md)。  
  
## <a name="see-also"></a>请参阅  
 [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)   
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)   
 [启动程序](../../../extensibility/debugger/launching-a-program.md)

