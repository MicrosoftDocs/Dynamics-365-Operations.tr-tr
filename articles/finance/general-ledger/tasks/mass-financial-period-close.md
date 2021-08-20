---
title: Toplu mali dönem kapatma
description: Bu konuda, bir dönemin nasıl beklemeye alındığı veya bir kerede bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir.
author: aprilolson
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7dac267d2d4ce0824bc47b63b8d07913a8dd7f02bcccc025880701cb4d0bdd3d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751289"
---
# <a name="mass-financial-period-close"></a>Toplu mali dönem kapatma

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]