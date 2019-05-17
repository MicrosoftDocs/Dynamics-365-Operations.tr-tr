---
title: Perakende işlem tutarlılık denetleyicisi
description: Bu konuda Microsoft Dynamics 365 for Retail ürününde bulunan perakende işlem tutarlılık denetleyicisi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517189"
---
# <a name="retail-transaction-consistency-checker"></a>Perakende işlem tutarlılık denetleyicisi


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Bu konuda Microsoft Dynamics 365 for Finance and Operations sürüm 8.1.3'te sunulan perakende işlem tutarlılık denetleyicisi açıklanmaktadır. Tutarlılık denetleyicisi, tutarsız işlemleri ekstre deftere nakil işlemiyle seçilmeden önce tanımlayıp ayırır.

Bir ekstre Retail departmanında deftere nakledildiğinde deftere nakil işlemi, perakende işlem tablolarında tutarsız verilerin bulunması nedeniyle başarısız olabilir. Veri sorunu, satış noktası (POS) uygulamasında öngörülemeyen aksaklıklardan veya işlemlerin üçüncü taraf POS sistemleri tarafından yanlış aktarılmasından kaynaklanabilir. Bu tutarsızlıkların nasıl görünebileceğine ilişkin örnekler şunlardır: 

  - Üstbilgi tablosundaki işlem toplamı, satırlardaki işlem toplamıyla eşleşmiyordur.
  - Üstbilgi tablosundaki satır sayısı, işlem tablosundaki satır sayısıyla eşleşmiyordur.
  - Üstbilgi tablosundaki vergiler, satırlardaki vergi tutarıyla eşleşmiyordur. 
  
Ekstre deftere nakil işlemi tarafından tutarsız işlemler seçildiğinde tutarsız satış faturaları ve ödeme günlükleri oluşturulur ve bunun sonucunda tüm ekstre deftere nakil işlemi başarısız olur. Ekstrelerin bu durumdan kurtarılması, birden fazla işlem tablosu arasında karmaşık veri düzeltmelerini içerir. Perakende işlem tutarlılık denetleyicisi, bu tür sorunları önler.

Aşağıdaki çizelgede işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi gösterilmektedir.

![Perakende işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi](./media/validchecker.png "Perakende işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi")

**Mağaza işlemlerini doğrulama** toplu işlemi, aşağıdaki senaryolar için perakende işlem tablolarının tutarlılığını denetler.

- Müşteri hesabı: Perakende işlem tablolarındaki müşteri hesabının Genel Merkez müşteri yöneticisinde de bulunduğunu doğrular.
- Satır sayısı: İşlem üstbilgi tablosundan alındığı şekilde satır sayısının satış işlem tablolarındaki satır sayısıyla eşleştiğini doğrular.

## <a name="set-up-the-consistency-checker"></a>Tutarlılık denetleyicisini ayarlama
**Perakende \> Perakende BT \> POS deftere nakil** bölümünde "Mağaza işlemlerini doğrulama" toplu işlemini düzenli aralıklarla yapılandırın. Toplu iş, "Ekstreyi toplu olarak hesaplama" ve "Ekstreyi toplu olarak deftere nakletme" işlemlerinin ayarlanmasına benzer şekilde, mağaza organizasyon hiyerarşisine göre zamanlanabilir. Bu toplu işlemi günde birden fazla kez yürütülecek şekilde yapılandırmanızı ve her P işi uygulamasının sonunda çalıştırılacak şekilde zamanlamanızı öneririz.

## <a name="results-of-validation-process"></a>Doğrulama işleminin sonuçları
Toplu işlem tarafından gerçekleştirilen doğrulama denetlemesinin sonuçları, uygun perakende işlemde işaretlenir. Perakende işlem kaydındaki **Doğrulama durumu** alanı, ya **Başarılı** ya da **Hata** olarak ayarlanır ve son doğrulama çalıştırma tarihi, **Son doğrulama saati** alanında görünür.

Doğrulama hatası ile ilgili daha fazla hata açıklaması görmek için ilgili perakende mağaza işlem kaydını seçip **Doğrulama hataları** düğmesine tıklayın.

Doğrulama denetlemesinden geçemeyen işlemler ve henüz doğrulanmamış olan işlemler ekstrelere eklenmez. "Ekstre hesaplama" işlemi sırasında ekstreye eklenebilecek, ancak eklenmemiş olan işlemlerin olması durumunda kullanıcılar bilgilendirilir.

Bir doğrulama hatası bulunursa hatayı düzeltmenin tek yolu, Microsoft Desteği ile iletişime geçmektir. Bir sonraki sürümde kullanıcıların kullanıcı arabiriminde başarısız olan kayıtları düzeltmelerine olanak tanıyan özellik eklenecektir. Değişiklik geçmişini takip etmek için günlüğe kaydetme ve denetleme özellikleri de kullanıma sunulacaktır.

> [!NOTE]
> Bir sonraki sürümde daha fazla senaryoyu desteklemek için ek doğrulama kuralları da eklenecektir.
