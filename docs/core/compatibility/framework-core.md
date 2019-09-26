---
title: 호환성이 손상되는 변경 사항, .NET Framework에서 .NET Core 3.0으로 - .NET Core
description: .NET Framework에서 .NET Core 3.0으로 Windows Forms 및 Windows Presentation Foundation에 대한 호환성이 손상되는 주요 변경을 나열합니다.
ms.date: 09/10/2019
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c658c5bce7a2554bba83f2779a73d9d6af01a342
ms.sourcegitcommit: 3ac05b2c386c8cc5e73f4c7665f6c0a7ed3da1bd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/20/2019
ms.locfileid: "71151527"
---
# <a name="breaking-changes-for-migration-from-net-framework-to-net-core-30"></a><span data-ttu-id="eba09-103">.NET Framework에서 .NET Core 3.0으로 마이그레이션 시 호환성이 손상되는 주요 변경</span><span class="sxs-lookup"><span data-stu-id="eba09-103">Breaking changes for migration from .NET Framework to .NET Core 3.0</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eba09-104">이 문서는 작성 중입니다.</span><span class="sxs-lookup"><span data-stu-id="eba09-104">This article is under construction.</span></span> <span data-ttu-id="eba09-105">이것은 .NET Core 호환성이 손상되는 변경 사항의 완전한 목록이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="eba09-105">This is not a complete list of .NET Core breaking changes.</span></span> <span data-ttu-id="eba09-106">.NET Core 호환성이 손상되는 변경 사항에 대한 자세한 내용은 GitHub의 dotnet/docs 리포지토리에 있는 개별 [호환성이 손상되는 변경 문제](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3Abreaking-change)에서 검토할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eba09-106">For more information on .NET Core breaking changes, you can examine individual [breaking changes issues](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3Abreaking-change) in the dotnet/docs repository on GitHub.</span></span> 

<span data-ttu-id="eba09-107">Windows Forms 또는 Windows Presentation Foundation 애플리케이션을 .NET Framework에서 .NET Core 3.0으로 마이그레이션하는 경우 다음 항목에서 앱에 영향을 줄 수 있는 주요 변경 내용을 검토하세요.</span><span class="sxs-lookup"><span data-stu-id="eba09-107">If you are migrating a Windows Forms or Windows Presentation Foundation application from .NET Framework to .NET Core 3.0, review the following topics for breaking changes that may affect your app:</span></span>

## <a name="windows-forms"></a><span data-ttu-id="eba09-108">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eba09-108">Windows Forms</span></span>

[!INCLUDE[Control.DefaultFont changed to Segoe UI 9pt](~/includes/core-changes/windowsforms/control-defaultfont-changed.md)]

***

[!INCLUDE[Modernization of the FolderBrowserDialog](~/includes/core-changes/windowsforms/modernized-folderbrowserdialog.md)]

***

[!INCLUDE[Switch.System.Windows.Forms.AllowUpdateChildControlIndexForTabControls compatibility switch not supported](~/includes/core-changes/windowsforms/deprecate-allowupdatechildcontrolindexfortabcontrols.md)]

***

[!INCLUDE[Switch.System.Windows.Forms.EnableVisualStyleValidation compatibility switch not supported](~/includes/core-changes/windowsforms/deprecate-enablevisualstylevalidation.md)]

***

[!INCLUDE[Switch.System.Windows.Forms.UseLegacyImages compatibility switch not supported](~/includes/core-changes/windowsforms/deprecate-uselegacyimages.md)]