---
ms.openlocfilehash: 23ba6064a283b47312a66f3636c2834a7d58106e
ms.sourcegitcommit: e02d17b2cf9c1258dadda4810a5e6072a0089aee
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/01/2020
ms.locfileid: "85620186"
---
### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET가 이제 끊어진 SQL 연결을 자동으로 다시 연결 시도

#### <a name="details"></a>설명

.NET Framework 4.5.1부터는 .NET Framework가 끊어진 SQL 연결을 자동으로 다시 연결하려고 시도합니다. 이것은 일반적으로 응용 프로그램을 보다 안정적으로 만들지만, 연결이 끊어져서 다시 연결될 때 어떤 조치를 취할 수 있다는 것을 앱이 알아야 할 경우가 있습니다.

#### <a name="suggestion"></a>제안 해결 방법

이 기능이 호환성 문제로 인해 사용하지 않을 경우, 연결 문자열(또는 <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=fullName>)의 <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=fullName> 속성을 0으로 설정하여 비활성화할 수 있습니다.

| 이름    | 값       |
|:--------|:------------|
| Scope   |Microsoft Edge|
|버전|4.5.1|
|형식|런타임

#### <a name="affected-apis"></a>영향을 받는 API

-<xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)></li></ul>|
