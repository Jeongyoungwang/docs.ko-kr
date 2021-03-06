---
title: '방법: Freezable을 읽기 전용으로 설정'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: 4185966d864be425bc631953461f6f27ab983bee
ms.sourcegitcommit: 944ddc52b7f2632f30c668815f92b378efd38eea
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/03/2019
ms.locfileid: "73460076"
---
# <a name="how-to-make-a-freezable-read-only"></a>방법: Freezable을 읽기 전용으로 설정
이 예제에서는 <xref:System.Windows.Freezable.Freeze%2A> 메서드를 호출 하 여 <xref:System.Windows.Freezable> 읽기 전용으로 설정 하는 방법을 보여 줍니다.  
  
 다음 조건 중 하나에 개체에 대 한 `true` 있는 경우 <xref:System.Windows.Freezable> 개체를 고정할 수 없습니다.  
  
- 애니메이션 또는 데이터 바인딩된 속성이 있습니다.  
  
- 동적 리소스에 의해 설정 되는 속성이 있습니다. 동적 리소스에 대 한 자세한 내용은 [XAML 리소스](../../../desktop-wpf/fundamentals/xaml-resources-define.md)를 참조 하세요.  
  
- 고정할 수 없는 <xref:System.Windows.Freezable> 하위 개체가 포함 되어 있습니다.  
  
 이러한 조건이 <xref:System.Windows.Freezable> 개체에 대해 `false` 되 고 수정 하지 않으려는 경우 성능 향상을 위해 고정 하는 것이 좋습니다.  
  
## <a name="example"></a>예제  
 다음 예에서는 <xref:System.Windows.Freezable> 개체의 형식인 <xref:System.Windows.Media.SolidColorBrush>를 고정 합니다.  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 <xref:System.Windows.Freezable> 개체에 대 한 자세한 내용은 [Freezable 개체 개요](freezable-objects-overview.md)를 참조 하세요.  
  
## <a name="see-also"></a>참조

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [Freezable 개체 개요](freezable-objects-overview.md)
- [방법 항목](base-elements-how-to-topics.md)
