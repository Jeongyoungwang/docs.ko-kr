---
title: ICorDebugManagedCallback 인터페이스
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback
helpviewer_keywords:
- ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: b47f1d61-c7dc-4196-b926-0b08c94f7041
topic_type:
- apiref
ms.openlocfilehash: cb2b69c5e6dfed4e0cb4e4e324c4ec6ad664f3e7
ms.sourcegitcommit: 488aced39b5f374bc0a139a4993616a54d15baf0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83212752"
---
# <a name="icordebugmanagedcallback-interface"></a>ICorDebugManagedCallback 인터페이스
디버거 콜백을 처리하는 메서드를 제공합니다.  
  
## <a name="methods"></a>메서드  
  
|메서드|설명|  
|------------|-----------------|  
|[Break 메서드](icordebugmanagedcallback-break-method.md)|<xref:System.Reflection.Emit.OpCodes.Break>코드 스트림의 명령이 실행 될 때 디버거에 알립니다.|  
|[Breakpoint 메서드](icordebugmanagedcallback-breakpoint-method.md)|중단점에 도달 하면 디버거에 알립니다.|  
|[BreakpointSetError 메서드](icordebugmanagedcallback-breakpointseterror-method.md)|CLR (공용 언어 런타임)이 함수가 JIT (just-in-time) 컴파일 전에 설정 된 중단점을 정확 하 게 바인딩하지 못했음을 디버거에 알립니다.|  
|[ControlCTrap 메서드](icordebugmanagedcallback-controlctrap-method.md)|디버깅 중인 프로세스에서 CTRL + C가 트랩 되었음을 디버거에 알립니다.|  
|[CreateAppDomain 메서드](icordebugmanagedcallback-createappdomain-method.md)|응용 프로그램 도메인이 생성 되었음을 디버거에 알립니다.|  
|[CreateProcess 메서드](icordebugmanagedcallback-createprocess-method.md)|프로세스가 처음으로 연결 되거나 시작 된 경우 디버거에 알립니다.|  
|[CreateThread 메서드](icordebugmanagedcallback-createthread-method.md)|스레드가 관리 코드 실행을 시작 했음을 디버거에 알립니다.|  
|[DebuggerError 메서드](icordebugmanagedcallback-debuggererror-method.md)|CLR에서 이벤트를 처리 하려고 시도 하는 동안 오류가 발생 했음을 디버거에 알립니다.|  
|[EditAndContinueRemap 메서드](icordebugmanagedcallback-editandcontinueremap-method.md)|사용되지 않습니다. 다시 매핑 이벤트가 IDE에 전송 되었음을 디버거에 알립니다.|  
|[EvalComplete 메서드](icordebugmanagedcallback-evalcomplete-method.md)|평가가 완료 되었음을 디버거에 알립니다.|  
|[EvalException 메서드](icordebugmanagedcallback-evalexception-method.md)|처리 되지 않은 예외를 사용 하 여 평가가 종료 되었음을 디버거에 알립니다.|  
|[Exception 메서드](icordebugmanagedcallback-exception-method.md)|관리 코드에서 예외가 throw 되었음을 디버거에 알립니다.|  
|[ExitAppDomain 메서드](icordebugmanagedcallback-exitappdomain-method.md)|응용 프로그램 도메인이 종료 되었음을 디버거에 알립니다.|  
|[ExitProcess 메서드](icordebugmanagedcallback-exitprocess-method.md)|프로세스가 종료 되었음을 디버거에 알립니다.|  
|[ExitThread 메서드](icordebugmanagedcallback-exitthread-method.md)|관리 코드를 실행 하는 스레드가 종료 되었음을 디버거에 알립니다.|  
|[LoadAssembly 메서드](icordebugmanagedcallback-loadassembly-method.md)|CLR 어셈블리가 성공적으로 로드 되었음을 디버거에 알립니다.|  
|[LoadClass 메서드](icordebugmanagedcallback-loadclass-method.md)|클래스가 로드 되었음을 디버거에 알립니다.|  
|[LoadModule 메서드](icordebugmanagedcallback-loadmodule-method.md)|CLR 모듈이 성공적으로 로드 되었음을 디버거에 알립니다.|  
|[LogMessage 메서드](icordebugmanagedcallback-logmessage-method.md)|CLR 관리 스레드가 클래스의 메서드를 호출 하 여 이벤트를 기록 했음을 디버거에 알립니다 <xref:System.Diagnostics.EventLog> .|  
|[LogSwitch 메서드](icordebugmanagedcallback-logswitch-method.md)|<xref:System.Diagnostics.Switch>디버깅/추적 스위치를 만들거나 수정 하거나 삭제 하기 위해 CLR 관리 스레드에서 클래스의 메서드를 호출 했음을 디버거에 알립니다.|  
|[NameChange 메서드](icordebugmanagedcallback-namechange-method.md)|응용 프로그램 도메인 또는 스레드의 이름이 변경 되었음을 디버거에 알립니다.|  
|[StepComplete 메서드](icordebugmanagedcallback-stepcomplete-method.md)|단계가 완료 되었음을 디버거에 알립니다.|  
|[UnloadAssembly 메서드](icordebugmanagedcallback-unloadassembly-method.md)|CLR 어셈블리가 언로드 되었음을 디버거에 알립니다.|  
|[UnloadClass 메서드](icordebugmanagedcallback-unloadclass-method.md)|클래스가 언로드되고 있음을 디버거에 알립니다.|  
|[UnloadModule 메서드](icordebugmanagedcallback-unloadmodule-method.md)|CLR 모듈 (DLL)이 언로드 되었음을 디버거에 알립니다.|  
|[UpdateModuleSymbols 메서드](icordebugmanagedcallback-updatemodulesymbols-method.md)|CLR 모듈의 기호가 변경 되었음을 디버거에 알립니다.|  
  
## <a name="remarks"></a>설명  
 모든 콜백은 동일한 스레드에서 호출 되며 동기화 된 상태의 프로세스와 함께 호출 됩니다.  
  
 각 콜백 구현에서는 [ICorDebugController:: Continue](icordebugcontroller-continue-method.md) 를 호출 하 여 실행을 다시 시작 해야 합니다. `ICorDebugController::Continue`콜백이 반환 되기 전에가 호출 되지 않으면 프로세스가 중지 된 상태로 유지 되 고가 호출 될 때까지 이벤트 콜백이 더 이상 발생 하지 않습니다 `ICorDebugController::Continue` .  
  
 디버거는 .NET Framework 버전 2.0 응용 프로그램을 디버깅 하는 경우 [ICorDebugManagedCallback2](icordebugmanagedcallback2-interface.md) 을 구현 해야 합니다. 또는의 인스턴스 `ICorDebugManagedCallback` 는 `ICorDebugManagedCallback2` [ICorDebug:: setmanagedhandler](icordebug-setmanagedhandler-method.md)에 콜백 개체로 전달 됩니다.  
  
> [!NOTE]
> 이 인터페이스는 크로스 시스템 또는 크로스 프로세스 원격 호출을 지원하지 않습니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:**[시스템 요구 사항](../../get-started/system-requirements.md)을 참조하세요.  
  
 **헤더:** CorDebug.idl, CorDebug.h  
  
 **라이브러리:** CorGuids.lib  
  
 **.NET Framework 버전:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>참고 항목

- [ICorDebug 인터페이스](icordebug-interface.md)
- [ICorDebugManagedCallback2 인터페이스](icordebugmanagedcallback2-interface.md)
- [디버깅 인터페이스](debugging-interfaces.md)
