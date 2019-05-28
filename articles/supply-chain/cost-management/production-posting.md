---
title: Üretimin deftere nakli
description: Bu makale üretim sürecindeki farklı türdeki nakiller hakkında bilgi sağlar.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b44d57fe89ef7ae3def835865e4da80c260f907
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547757"
---
# <a name="production-posting"></a>Üretimin deftere nakli

[!include [banner](../includes/banner.md)]

Bu makale üretim sürecindeki farklı türdeki nakiller hakkında bilgi sağlar.

Üretim nakil işlemleri, aşağıdaki bölümlerde açıklanan üretim süreçlerini takip eder.

## <a name="material-consumption"></a>Malzeme tüketimi
Üretim malzeme çekme listesi defteri nakledildiğinde üretim sırasında malzemeler tüketildi olarak kaydedilir. Bu süreç, eldeki stoktan düşecek çıkış hareketleri oluşturulur. Üretim parametrelerinde, kullanılmaya devam eden (süren iş \[[WIP]\]) ham maddelerin değerinin deftere nakledilip nakledilmeyeceğini belirleyebilirsiniz. Kullanılmaya devam eden (WIP) hammaddelerin değeri özel bir Malzeme çekme listesi hesabına ve özel bir Malzeme çekme listesi mahsup hesabına aktarılır.

## <a name="time-consumption"></a>Zaman tüketimi
Üretim işlerinde çalışanların harcadıkları süre Rota kartı defterine veya İş kartı defterine kaydedilir. Bu defterler nakledildiğinde, kullanılmaya devam eden (WIP) kaynaklar için özel bir hesaba nakil yapan defter işleme alınır. Bu nakil işlemi, üretim emri için harcanan sürenin değerini temsil eder. Üretim emri sonlandırıldı olarak kaydedildiğinde WIP hesapları kapatılır.

## <a name="reporting-finished-goods-and-error-quantities"></a>Mamul malların ve hatalı miktarların raporlanması
Bir üretim emri tamamlandı olarak rapor edildiğinde tamamlanan niahi malların miktarı, Raporla Stok yönetiminde nihai olarak güncellenir. Üretim parametreleri altında ayarlanabilen WIP hesapları kullanıyorsanız, madde formundaki standart maliyet kullanılarak süren WIP hesaplarını düşürmek ve mamul madde stokunu yükseltmek için bir genel muhasebe günlüğü yapılır. Defter, ürün için tanımlanan standart maliyeti kullanır.

## <a name="ending-the-production-order"></a>Üretim emrinin sonlandırılması
Bir üretim emri sonlandırılmadan önce gerçek maliyetler, üretilen miktar için hesaplanır. Tüm tahmini malzeme, işgücü giderleri ve genel giderler tersine çevrilir ve bunların yerine gerçek maliyetler konur. Mamul ürünün toplam maliyeti, stok Giriş hesabından düşürür ve stok Çıkış hesabına alacak kaydedilir. Maliyet hesabı yürütürken **İşi sonlandır** seçim kutusunu işaretlerseniz üretim emrinin durumu **Sonlandırıldı** olarak değişir. Bu durum, tamamlanmış bir üretim emrine istemeden ek maliyetlerin nakledilmesini engeller. Raporlama sırasında bitti olarak rapor edilen hatalı miktarların değerinin bitti olarak rapor edilen doğru miktarlara tahsis edilmesi gerektiğini belirtebilirsiniz. Alternatif olarak, özel bir hurda hesabına nakledilmesi gereken hata miktarları değerini belirtebilirsiniz.

## <a name="controlling-the-level-of-ledger-posting"></a>Defter nakil düzeyinin kontrol edilmesi
**Üretim kontrol parametreleri** altında üretim prosesleri için defter nakil düzeyini ayarlamak üzere **Defter naklil** alanını kullanabilirsiniz. Aşağıdaki değerler kullanılabilir:

-   **Madde ve kaynak** – Ham maddeler ve nihai mallar için madde gruplarında tanımlanan defter hesaplarını kullanın. Harcanan süre için WIP, rota operasyonlarına ilişkin kaynaktan veya kaynak grubundan alınır.
-   **Madde ve kategori** – Ham maddeler ve niahi mallar için madde gruplarında ayarlanan defter hesaplarını kullanın. Harcanan süre için WIP, rota operasyonlarıyla ilişkilendirilen maliyet kategorilerinden alınır.
-   **Üretim grupları** – Hem harcanan malzeme hem harcanan süre için üretim gruplarında ayarlanan defter hesaplarını kullanın. Üretim grupları, serbest bırakılan ürünlerle ilişkilendirilir ve oluşturulduklarında üretim emirlerine kopyalanır. Üretim emirlerinde nakil, üretim emriyle ilişkilendirilen üretim gruplarını takip eder.

**Not:** Bitmiş maddenin maliyetini hesaplamak için standart yöntem kullanılmışsa, nihai hareketler bu gerçeği yansıtır. Gerçek maliyetler ve standart yöntemle hesaplanan maliyetler arasında fark oluşursa, bu fark kar ya da zararı gösteren hesaba nakledilir.



