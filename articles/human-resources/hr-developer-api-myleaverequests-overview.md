---
title: MyLeaveRequests genel bakış
description: Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054968"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests genel bakış

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.

## <a name="key"></a>Anahtar

  | Özellik adı | Veri Türü |
  |---------------|-----------|
  | dataAreaId    | Dize    |
  | RequestId     | Dize    |
  | LeaveType     | Dize    |
  | LeaveDate     | Tarih      |
  
## <a name="properties"></a>Özellikler

  | Özellik adı     | Veri Türü | Gerekli |
  |-------------------|-----------|----------|
  | dataAreaId        | Dize    | X        |
  | RequestId         | Dize    | X        |
  | LeaveType         | Dize    | X        |
  | LeaveDate         | Tarih      | X        |
  | ReasonCodeId      | Dize    |          |
  | PersonnelNumber   | Dize    | X        |
  | RequestDate       | Tarih      | X        |
  | Açıklama           | Dize    |          |
  | Durum            | Numaralandırma      | X        |
  | Tutar            | Gerçek      |          |
  | HalfDayDefinition | Numaralandırma      |          |

## <a name="actions"></a>Eylemler

 | Eylem adı                               | Tanım                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [gönder](hr-developer-api-myleaverequests-submit.md)   | İsteği iş akışı tarafından işlenecek şekilde gönder. |

## <a name="see-also"></a>Ayrıca bkz.

- [Bir izin isteğini iş akışına gönderme](hr-developer-api-myleaverequests-submit.md)
- [Kimlik doğrulama](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]