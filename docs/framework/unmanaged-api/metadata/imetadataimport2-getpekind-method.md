---
title: IMetaDataImport2::GetPEKind 메서드
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetPEKind
helpviewer_keywords:
- GetPEKind method [.NET Framework metadata]
- IMetaDataImport2::GetPEKind method [.NET Framework metadata]
ms.assetid: d91c3d89-8022-4a4c-a2a2-a8af2c387507
topic_type:
- apiref
ms.openlocfilehash: 3626998c456e23fb922ae45a68bedb0e45a7ccba
ms.sourcegitcommit: da21fc5a8cce1e028575acf31974681a1bc5aeed
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/08/2020
ms.locfileid: "84490434"
---
# <a name="imetadataimport2getpekind-method"></a>IMetaDataImport2::GetPEKind 메서드
현재 메타 데이터 범위에 정의 된 PE (이식 가능한 실행) 파일 (일반적으로 DLL 또는 EXE 파일)에 있는 코드의 특성을 식별 하는 값을 가져옵니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
HRESULT GetPEKind (  
   [out] DWORD *pdwPEKind,  
   [out] DWORD *pdwMachine  
);  
```  
  
## <a name="parameters"></a>매개 변수  
 `pdwPEKind`  
 제한이 PE 파일을 설명 하는 [CorPEKind](corpekind-enumeration.md) 열거형의 값에 대 한 포인터입니다.  
  
 `pdwMachine`  
 제한이 컴퓨터의 아키텍처를 식별 하는 값에 대 한 포인터입니다. 가능한 값에 대해서는 다음 섹션을 참조 하십시오.  
  
## <a name="remarks"></a>설명  
 매개 변수에서 참조 하는 값은 `pdwMachine` 다음 중 하나일 수 있습니다.  
  
|값|컴퓨터 아키텍처|  
|-----------|--------------------------|  
|IMAGE_FILE_MACHINE_I386<br /><br /> 0x014C|x86|  
|IMAGE_FILE_MACHINE_IA64<br /><br /> 0x0200|Intel IPF|  
|IMAGE_FILE_MACHINE_AMD64<br /><br /> 0x8664|X64|  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:**[시스템 요구 사항](../../get-started/system-requirements.md)을 참조하세요.  
  
 **헤더:** Cor  
  
 **라이브러리:** Mscoree.dll에서 리소스로 사용 됩니다.  
  
 **.NET Framework 버전:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고 항목

- [IMetaDataImport2 인터페이스](imetadataimport2-interface.md)
- [IMetaDataImport 인터페이스](imetadataimport-interface.md)
- [CorPEKind 열거형](corpekind-enumeration.md)
