---
title: XPath를 사용하여 LINQ to XML을 쿼리하는 방법(C#)
ms.date: 07/20/2015
ms.assetid: ee5af263-4ab1-45e5-b792-33a3221b426d
ms.openlocfilehash: 61878febd9b4880872b7bc58e4de04b37cff96f8
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/14/2020
ms.locfileid: "75344804"
---
# <a name="how-to-query-linq-to-xml-using-xpath-c"></a>XPath를 사용하여 LINQ to XML을 쿼리하는 방법(C#)
이 항목에서는 XPath를 사용하여 XML 트리를 쿼리할 수 있도록 하는 확장명 메서드에 대해 소개합니다. 이러한 확장 메서드 사용에 대한 자세한 내용은 <xref:System.Xml.XPath.Extensions?displayProperty=nameWithType>를 참조하세요.  
  
 레거시 코드의 광범위한 사용과 같이 XPath를 사용하여 쿼리할 매우 구체적인 이유가 없는 한 LINQ to XML과 함께 XPath를 사용하지 않는 것이 좋습니다. XPath 쿼리의 성능은 [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] 쿼리의 성능보다 좋지 않습니다.  
  
## <a name="example"></a>예제  
 다음 예제에서는 작은 XML 트리를 만들고 <xref:System.Xml.XPath.Extensions.XPathSelectElements%2A>를 사용하여 요소 집합을 선택합니다.  
  
```csharp  
XElement root = new XElement("Root",  
    new XElement("Child1", 1),  
    new XElement("Child1", 2),  
    new XElement("Child1", 3),  
    new XElement("Child2", 4),  
    new XElement("Child2", 5),  
    new XElement("Child2", 6)  
);  
IEnumerable<XElement> list = root.XPathSelectElements("./Child2");  
foreach (XElement el in list)  
    Console.WriteLine(el);  
```  
  
 이 예제는 다음과 같은 출력을 생성합니다.  
  
```xml  
<Child2>4</Child2>  
<Child2>5</Child2>  
<Child2>6</Child2>  
```  
  