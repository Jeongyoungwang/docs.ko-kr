---
ms.openlocfilehash: c3e39e49747be709977d7fba3c39b59f5575c40d
ms.sourcegitcommit: e02d17b2cf9c1258dadda4810a5e6072a0089aee
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/01/2020
ms.locfileid: "85620504"
---
### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException이 줄 위치를 제대로 설정

#### <a name="details"></a>설명

<xref:System.Xml.Linq.LoadOptions.SetLineInfo> 값을 Load 메서드에 전달하고 유효성 검사 오류가 발생한 경우 <xref:System.Xml.Schema.XmlSchemaException.LineNumber> 및 <xref:System.Xml.Schema.XmlSchemaException.LinePosition> 속성은 이제 줄 정보를 포함합니다.

#### <a name="suggestion"></a>제안 해결 방법

XML을 로드하는 동안 SetLineInfo를 사용할 때 이러한 속성이 이제 제대로 설정되므로 <xref:System.Xml.Schema.XmlSchemaException.LineNumber> 및 <xref:System.Xml.Schema.XmlSchemaException.LinePosition>이 설정되지 않는다고 가정하는 예외 처리 코드를 업데이트해야 합니다.

| 이름    | 값       |
|:--------|:------------|
| Scope   |Microsoft Edge|
|버전|4.5|
|형식|런타임

#### <a name="affected-apis"></a>영향을 받는 API

-<xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|
