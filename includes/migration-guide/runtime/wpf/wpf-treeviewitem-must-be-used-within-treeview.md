---
ms.openlocfilehash: af8cb9435be078351e3430dc8ded3f7cac377948
ms.sourcegitcommit: e02d17b2cf9c1258dadda4810a5e6072a0089aee
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/01/2020
ms.locfileid: "85620499"
---
### <a name="wpf-treeviewitem-must-be-used-within-a-treeview"></a>TreeView 내에서 WPF TreeViewItem을 사용해야 합니다.

#### <a name="details"></a>설명

변경 내용은 <xref:System.Windows.Controls.TreeView?displayProperty=fullName>의 외부에서 <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName> 요소의 사용을 제한하는 4.5에서 도입되었습니다. 이것은 다음과 같은 경우에 매니페스트할 수 있습니다.<ul><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>의 시각적 부모는 패널이 아닙니다. (<xref:System.Windows.Controls.TreeView?displayProperty=fullName>에 대해 생성된 <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>은 패널을 부모로 가집니다.)</li><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>은 목록 컨트롤(ListBox, DataGrid, ListView 등)에 대해 &quot;항목 호스트&quot; 역할을 하는 <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=fullName>의 하위 항목입니다. 가상화를 사용할 필요가 없습니다.</li><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=fullName>은 항목 스크롤(<code>ScrollUnit=&quot;Item&quot;</code>)입니다.</li><li>누군가 <code>VirtualizingStackPanel.MakeVisible(v)</code>을 호출하여 요소 <code>v</code>를 보기로 스크롤합니다. 이것은 명시적으로 또는 암시적인 몇 가지 방법으로 실행될 수 있습니다. 아마도 가장 일반적인 방법은 간단히 <code>v</code>를 클릭하여 키보드 포커스를 부여하는 것입니다.</li><li><code>v</code>에서 <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=fullName>로의 시각적 부모 체인은 <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>을 통과합니다.</li></ul>즉, 이것은 <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>이 <xref:System.Windows.Controls.TreeView?displayProperty=fullName> 외부에서 사용되고 사용자가 <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>의 하위 항목을 클릭하여 보기로 가져올 때 보입니다. <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>에 포커스 가능한 하위 항목이 없는 경우 이 문제는 발생하지 않습니다. 이것이 적중되는 상황의 예는 <xref:System.Windows.Controls.TreeViewItem?displayProperty=fullName>이 DateTemplate의 루트일 때입니다. 이 문제가 적중하면 WPF 프레임워크 내에 InvalidCastException가 발생합니다.

#### <a name="suggestion"></a>제안 해결 방법

이것을 위해 사용 가능한 핫픽스가 생성됩니다.

| 이름    | 값       |
|:--------|:------------|
| Scope   |부|
|버전|4.5|
|형식|런타임|
