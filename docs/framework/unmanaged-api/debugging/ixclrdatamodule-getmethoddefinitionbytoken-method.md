---
title: 'IXCLRDataModule:: GetMethodDefinitionByToken 메서드'
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetMethodDefinitionByToken Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method
helpviewer.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 074949145be588fc34266a9f2ee501caeeffb9d3
ms.sourcegitcommit: 9a4488a3625866335e83a20da5e9c5286b1f034c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/15/2020
ms.locfileid: "83420879"
---
# <a name="ixclrdatamodulegetmethoddefinitionbytoken-method"></a>IXCLRDataModule:: GetMethodDefinitionByToken 메서드

지정 된 메타 데이터 토큰에 해당 하는 메서드 정의를 가져옵니다.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>구문

```cpp
HRESULT GetMethodDefinitionByToken(
    [in] mdMethodDef token,
    [out] IXCLRDataMethodDefinition** methodDefinition
);
```

## <a name="parameters"></a>매개 변수

`token`\
진행 메서드 토큰입니다.

`methodDefinition`\
제한이 메서드 정의입니다.

## <a name="remarks"></a>설명

제공 된 메서드는 인터페이스의 일부 이며 `IXCLRDataModule` 가상 메서드 테이블의 26 일 슬롯에 해당 합니다.

## <a name="requirements"></a>요구 사항

**플랫폼:**[시스템 요구 사항](../../get-started/system-requirements.md)을 참조하세요.  
**헤더:** 없음을  
**라이브러리:** 없음을  
**.NET Framework 버전:**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>참고 항목

- [디버깅](index.md)
- [IXCLRDataModule 인터페이스](ixclrdatamodule-interface.md)
