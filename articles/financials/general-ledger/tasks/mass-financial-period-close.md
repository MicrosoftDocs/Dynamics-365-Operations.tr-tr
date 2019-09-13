---
title: Toplu mali dönem kapatma
description: Bu konuda, bir dönemin nasıl beklemeye alındığı veya bir kerede bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 398a62e575010501291af3016553fc72fbc891de
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914642"
---
# <a name="mass-financial-period-close"></a>Toplu mali dönem kapatma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konuda, bir dönemin nasıl beklemeye alındığı veya bir kerede bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir. Ayrıca görev, kullanıcı grubunun belirli modüllere naklinin nasıl sınırlandırılacağını gösterir.

1. Gezinti bölmesinde **Modüller > Genel muhasebe > Dönem kapanışı > Genel muhasebe takvimleri**'ne gidin. Görüntülenen tüzel kişilikler listesinin sayfada seçilen mali takvime bağlı olduğunu unutmayın. Yalnızca seçilen mali takvimi kullanan tüzel kişilikler görüntülenecektir.
2. **Düzenle** öğesini seçin.
3. Durumu değiştirmek istediğiniz dönemi seçin.
4. Durumu güncelleştirmek istediğiniz tüzel kişilikleri seçin. Kılavuzun sol üst kısmındaki onay işaretini seçerek tüm tüzel kişilikleri hızlı bir şekilde seçebilirsiniz.  
5. Seçilen modüle nakil erişimini tanımlamak için **Modül erişimini güncelleştir**'i seçin. Modül durumu da kılavuzdaki kayıtları düzenleyerek tek tek güncelleştirilebilir. Birden çok tüzel kişilik kaydını hızlı bir şekilde güncelleştirmek istediğinizde düğmeyi kullanabilirsiniz.  
6. **Uygulama** modülünde, durumunu güncelleştirmek istediğiniz modülü seçin. **Seç**'e tıklayın.
7. **Erişim** düzeyinde **Tümü**, **Hiçbiri** veya belirli bir kullanıcı grubunu seçin. **Seç**'e tıklayın. Tümü, dönem açıksa, deftere nakil yapabilecek modülü düzenleme erişimi olan tüm kullanıcıları gösterir. Dönem açıksa, hiçbiri modülde deftere nakil yapamayacak tüm kullanıcıları göstermez. Belirli bir kullanıcı grubu, dönem açıksa, yalnızca gruptaki modülde deftere nakil yapabilecek kullanıcıları gösterir.  
8. **Güncelleştir**'i seçin
9. Durumu güncelleştirmek için başka bir dönem seçin.
10. Durumunu güncelleştirmek istediğiniz tüzel kişilikleri seçin.
11. **Dönem durumunu güncelleştir**'i seçin ve durumu **Beklemede**, **Açık** veya **Kalıcı olarak kapatıldı** şeklinde ayarlayın. **Açık**, dönem içinde erişimi olan kullanıcılar tarafından deftere nakil yapılabileceğini gösterir. **Beklemede** dönemin nakledilemeyeceği ancak yeniden açılabileceği anlamına gelir. **Kalıcı olarak kapatıldı**, dönemin tamamen kapatıldığı ve bir daha açılamayacağı anlamına gelir. Ayarlamalar nakledilemezler. Tüm ayarlamalar ve denetimler tamamlanana kadar bir dönemin **Kalıcı olarak kapatıldı** şeklinde ayarlanması önerilmez.  
12. **Güncelleştir**'i seçin

