---
title: Satıcı KDV kayıt tarihi
description: Bu konu, satıcı KDV kaydının bitiş tarihini etkinleştirme özelliği hakkında bilgi sağlar
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 882d5a8718d819cff80bfa5b86e054a39e9db159
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7992071"
---
# <a name="date-of-vendor-vat-register"></a>Satıcı KDV kayıt tarihi

Microsoft Dynamics 365 Finance sürüm 10.0.24'te yeni **Satıcı KDV kayıt alanının tarihi**, satıcı faturaları için kullanılabilir. Bu alan, bir satınalmayla ilgili vergiye tabi tedarikin tarihini belirtir.

Yeni alanı etkinleştirmek için, **Özellik yönetimi** çalışma alanına gidin , **Satıcı faturaları üzerindeki satıcı KDV kaydının etkinleştirme tarihi** özelliğini bulun ve **Şimdi etkinleştir**'i seçin.

Tedarikçilerinizi gelen faturaların iki tarihi olabilir: satıcının faturayı verdiği tarih ve vergiye tabi tedarikin tarihi (diğer bir deyişle, satıcının katma değer vergisi [KDV] değerini aldığı tarih borcu). Bazı senaryolarda bu iki tarih farklılık gösterebilir.

Bir satınalma faturası için gelen KDV tutarını düşebilirsiniz ve bu faturayı daha sonra KDV raporlarına, daha önce sözü edilen tarihlerden farklı bir tarihe dahil edebilirsiniz. Bu tarih bazı senaryolarda ertelenen gelen KDV kesintisi ile ilgili yerel yasalarla kontrol edilir. Ülke veya bölgeye göre değişir.

Çek Cumhuriyeti'nde [KDV kontrol ekstre raporu](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) gibi bazı KDV raporları, bir satınalma belgesi için vergiye tabi tedarikin tarihinin bildirilmesine gerek duyar. Vergi dairesinin, ilgili kişilerin arasındaki KDV raporlamasını mutabık kılabilmesi için bu tarih raporlanmalıdır.

Finance'de, aşağıdaki alanlarda tarihleri tanımlayabilirsiniz:

- **Fatura tarihi** – Faturanın tedarikçi tarafından verildiği tarih.
- **KDV kaydı tarihi** – Satınalma faturası için KDV tutar kesintisi tarihi.
- **Satıcı KDV kaydının tarihi** – Satıcının vergiye tabi kaynağının tarihi.
- **Alınan belge tarihi** – Faturayı teslim aldığınız tarih.

Bu alanlar, aşağıdaki sayfalarda yer alır:

- Satıcı faturası
- Satıcı faturası kaydı
- Satıcı faturası onayı
- Satıcı fatura günlüğü

Satıcı faturası deftere nakledildikten sonra, tarihleri **Fatura günlüğü** ve **Satıcı hareketleri** sayfalarında inceleyebilirsiniz.
