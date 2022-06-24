---
title: Toplu mali dönem kapatma
description: Bu makalede, bir dönemin nasıl beklemeye alındığı veya tek seferde bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir.
author: aprilolson
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18e2418777e4f8a5f10b946d7cdc217e5e264318
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872455"
---
# <a name="mass-financial-period-close"></a>Toplu mali dönem kapatma

[!include [banner](../../includes/banner.md)]

Bu makalede, bir dönemin nasıl beklemeye alındığı veya tek seferde bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir. Ayrıca görev, kullanıcı grubunun belirli modüllere naklinin nasıl sınırlandırılacağını gösterir.

1. Gezinti bölmesinde **Genel muhasebe > Dönem kapanışı > Genel muhasebe takvimleri**'ne gidin. Görüntülenen tüzel kişilikler listesinin sayfada seçilen mali takvime bağlı olduğunu unutmayın. Yalnızca seçilen mali takvimi kullanan tüzel kişilikler görüntülenecektir.
2. **Düzenle** öğesini seçin.
3. Durumu değiştirmek istediğiniz dönemi seçin.
4. Durumu güncelleştirmek istediğiniz tüzel kişilikleri seçin. Kılavuzun sol üst kısmındaki onay işaretini seçerek tüm tüzel kişilikleri hızlı bir şekilde seçebilirsiniz.  
5. Seçilen modüle nakil erişimini tanımlamak için **Modül erişimini güncelleştir**'i seçin. Modül durumu da kılavuzdaki kayıtları düzenleyerek tek tek güncelleştirilebilir. Birden çok tüzel kişilik kaydını hızlı bir şekilde güncelleştirmek istediğinizde düğmeyi kullanabilirsiniz.  
6. **Uygulama** modülünde, durumunu güncelleştirmek istediğiniz modülü seçin. **Seç**'e tıklayın.
7. **Erişim** düzeyinde **Tümü**, **Hiçbiri** veya belirli bir kullanıcı grubunu seçin. **Seç**'e tıklayın.  
- **Tümü** - Dönem açıksa, modülü düzenleme erişimi olan tüm kullanıcılar deftere nakil yapabilir. 
- **Hiçbiri** - Dönem açıksa, kullanıcılar modüle nakil yapamaz. Belirli bir kullanıcı grubu, dönem açıksa, yalnızca gruptaki modülde deftere nakil yapabilecek kullanıcıları gösterir.  
8. **Güncelleştir**'i seçin. 
9. Durumu güncelleştirmek için başka bir dönem seçin.
10. Durumunu güncelleştirmek istediğiniz tüzel kişilikleri seçin.
11. **Dönem durumunu güncelleştir**'i seçin ve durumu **Beklemede**, **Açık** veya **Kalıcı olarak kapatıldı** şeklinde ayarlayın. **Açık**, dönem içinde erişimi olan kullanıcılar tarafından deftere nakil yapılabileceğini gösterir. **Beklemede** dönemin nakledilemeyeceği ancak yeniden açılabileceği anlamına gelir. **Kalıcı olarak kapatıldı**, dönemin tamamen kapatıldığı ve bir daha açılamayacağı anlamına gelir. Ayarlamalar nakledilemezler. Tüm ayarlamalar ve denetimler tamamlanana kadar bir dönemin **Kalıcı olarak kapatıldı** şeklinde ayarlanması önerilmez.  
12. **Güncelleştir**'i seçin



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
