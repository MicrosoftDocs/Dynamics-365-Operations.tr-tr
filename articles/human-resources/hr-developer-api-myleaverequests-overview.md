---
title: MyLeaveRequests genel bakış
description: Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115548"
---
# <a name="myleaverequests-overview"></a>MyLeaveRequests genel bakış

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