---
title: <typename>' 형식이 CLS 규격이 아닙니다.
ms.date: 07/20/2015
f1_keywords:
- bc40041
- vbc40041
helpviewer_keywords:
- BC40041
ms.assetid: 634132c2-5646-44aa-98c6-f773e2e63882
ms.openlocfilehash: eacf5036ebc6fc31dfa0e8de39c4fb574c9072b3
ms.sourcegitcommit: f8c270376ed905f6a8896ce0fe25b4f4b38ff498
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2020
ms.locfileid: "84386960"
---
# <a name="type-typename-is-not-cls-compliant"></a>\<typename>' 형식이 CLS 규격이 아닙니다.
변수, 속성 또는 함수 return이 CLS 규격이 아닌 데이터 형식으로 선언 되었습니다.  
  
 응용 프로그램의 [언어 독립성 및 언어 독립적 구성 요소](../../../standard/language-independence-and-language-independent-components.md) (cls)를 준수 하려면 cls 규격 형식만 사용 해야 합니다.  
  
 다음 Visual Basic 데이터 형식은 CLS 규격이 아닙니다.  
  
- [SByte 데이터 형식](../data-types/sbyte-data-type.md)  
  
- [UInteger 데이터 형식](../data-types/uinteger-data-type.md)  
  
- [ULong 데이터 형식](../data-types/ulong-data-type.md)  
  
- [UShort 데이터 형식](../data-types/ushort-data-type.md)  
  
 **오류 ID:** BC40041  
  
## <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
- 응용 프로그램에서 CLS 규격을 준수 해야 하는 경우이 요소의 데이터 형식을 가장 가까운 CLS 규격 형식으로 변경 합니다. 예를 들어 2,147,483,647을 초과하는 값 범위가 필요하지 않은 경우 `UInteger` 대신 `Integer` 을 사용할 수 있습니다. 확장된 범위가 필요한 경우 `UInteger` 를 `Long`으로 바꿀 수 있습니다.  
  
- 응용 프로그램에서 CLS 규격이 필요 하지 않은 경우에는 아무것도 변경할 필요가 없습니다. 그러나 비준수를 알고 있어야 합니다.
