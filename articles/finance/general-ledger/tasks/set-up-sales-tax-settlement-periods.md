---
title: Satış vergisi kapatma dönemlerini ayarlama
description: Bu konuda, Dynamics 365 Finance'da satış vergisi kapatma dönemlerini nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e5340150623057e233ed0acf487c42c61deba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222131"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Satış vergisi kapatma dönemlerini ayarlama

[!include [banner](../../includes/banner.md)]

Bu konuda, satış vergisi kapatma dönemlerinin nasıl ayarlanacağı açıklanmaktadır. Satış vergisi kapatma dönemleri, satış vergisinin bildirilip ödenmesi gereken dönem aralıkları hakkında bilgiler içerir. Belirli bir tarih aralığında bir kapatma dönemi için bir kapatma işlemi yapılabilir. Kapatma dönemiyle ilişkili tüm vergi kodları kapatılır. İlgili satış vergisi dairesinin ayarlarına bağlı olarak, vergi borcu ya bir satıcıya veya bir Genel muhasebe hesabına nakledilir.

Bu görevde USMF demo şirketi kullanılmaktadır.

1. Gezinti bölmesinde **Modüller > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kapatma dönemleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Kapatma dönemi** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Makam** alanında kapatma dönemi için oluşturulan bildirimleri ve ödemeleri alan satış vergisi makamını seçin.
6. Listede, istenen kaydı bulun ve seçin.
7. **Ödeme koşulları** alanında, açılır menüden istediğiniz kaydı seçin. İlgili Satış vergi dairesi, bir satıcı olarak kurulabilir ve Satış vergisi kapatma işlemi bir açık satıcı faturası oluşturur. Ödeme koşulları, açık satıcı faturası için Vade tarihi oluşturur.  
8. Kapatma dönemi aralıkları için tür seçin.
9. Dönem başına dönem aralığı birim sayısını girin. Örneğin üç aylık dönemde 3 ay vardır.
10. **Satış vergisi kapatma için toplu iş kullan** onay kutusunu işaretleyin veya kutuda işaret varsa kaldırın. Kapatma dönemi için kapatma işlemi arka planda toplu iş olarak sürdürülebilir. Bu bir dönem aralığında çok sayıda vergi hareketi olması durumunda önerilir.  
    > [!NOTE]
    > Şu anda bu İspanya, İtalya, Japonya ve Hollanda'da desteklenmez.
11. **Mahsup vergi hareketleri oluşturmayı engelle** onay kutusunu seçin veya temizleyin. Varsayılan olarak, sistem kapatma işlemi sırasında mahsup vergi hareketleri oluşturur; bu da bir dönem aralığında çok sayıda vergi hareketi varsa performans sorununa neden olur. Mahsup vergi hareketleri oluşturmayı engellemek için bu onay kutusunu seçin.
12. **Dönem aralıkları sekmesi**'ni genişletin.
13. **Ekle**'yi seçin.
14. **Başlangıç tarihi** alanında yeni sekmede bir tarih girin.
15. **Bitiş tarihi** alanına bir tarih girin.
16. **Yeni dönem aralığı**'nı seçin. İlk dönem aralığı girildikten sonra yeni dönemler otomatik olarak oluşturulabilir. Gerektiğinde geri dönüp yeni dönem aralıkları ekleyebilirsiniz.  
17. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]