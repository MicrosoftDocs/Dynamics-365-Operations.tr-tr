---
title: "Kişiselleştirilmiş ürün önerilerine genel bakış"
description: "Bu konuda satış noktası (POS) cihazında görüntülenebilecek Dynamics 365 for Retail ürün önerileri hakkında bilgiler yer almaktadır."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 942d6225a46b108ea39d3b8e4376b644c128ae6d
ms.contentlocale: tr-tr
ms.lasthandoff: 11/15/2017

---

# <a name="personalized-product-recommendations-overview"></a>Kişiselleştirilmiş ürün önerilerine genel bakış

[!include[banner](includes/banner.md)]


> [!NOTE]
> Bu özellik şu anda yalnızca korumalı alan ve üretim (yüksek kullanılabilirlik) dağıtım topolojilerinde kullanılabilir. 

Dynamics 365 for Retail'da, ürün önerileri satış noktası cihazında (POS) görüntülenebilir. Öneriler satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerin ilgi duyabilecekleri maddelerdir. Büyük kataloglara sahip perakendeciler için öneriler müşterinin ürün bulmasına yardımcı olur. Müşterinin ilgi alanlarını ve satın alma alışkanlıklarını hedefleyen ürünleri sunarak , ürün önerileri perakendecilere çapraz satış ve yukarı satış konusunda yardımı olabilir ve müşteri tutmayı geliştirebilir. Dynamics 365 for Retail'de ürün önerileri bilişsel hizmetler ve Microsoft Azure makine öğrenimiyle desteklenir.


<a name="scenarios"></a>Senaryolar
---------

Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir. Bulut POS veya Modern POS'da (MPOS) kullanılabilir.

1.  **Ürün ayrıntıları** sayfasında:

-   Bir mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı birlikte satın alınabilecek ek maddeleri önerir.
-   Mağaza çalışanı müşteriyi harekete ekler ve **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı müşteri hareket geçmişini kullanarak kişiselleştirilmiş öneriler sağlar.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  **Hareket** sayfasında:

-   Öneri altyapısı sepetteki maddelerin tam listesini temel olarak maddeler önerir.
-   Mağaza çalışanı müşteriyi harekete eklerse, öneri altyapısı müşteri hareket geçmişini ve sepetteki maddelerin listesini kullanarak kişiselleştirilmiş öneriler sağlar.

> [!NOTE]
> **Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 for Retail'da ekran düzenini güncelleştirmesi gerekir. **Öneriler** denetimi, **Hareket** sayfasında atlanmalıdır. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  **Müşteri ayrıntıları** sayfasında:
    -   Öneri altyapısı Kullanıcı kimliğini ve müşteri istek listesindeki maddeleri temel olarak maddeler önerir.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Dynamics 365 for Retail'ı POS önerileri etkinleştirme işlemleri için yapılandırma
Ürün önerilerini ayarlamak için aşağıdakileri yapmanız gerekir:

1.  Doğru **Tüzel kişilik** seçimi yaptığınızdan emin olun.
2.  **Varlık deposu**'na gidin, **Perakende satış**'ı seçin ve ardından **Yenile**'ye tıklayın. Bu, işlem veritabanınızdan alınan demo verileri (veya sizin verilerinizi) kullanır ve bunu Varlık deposuna taşır.
3.  İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.

4.  **Perakende parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.
5.  Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın. Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.

## <a name="how-does-it-work"></a>[]()Nasıl çalışır?
**Varlık deposu** varlığını yenilediğinizde, aşağıdaki eylemleri gerçekleşir.

-   Bilişsel hizmetler tarafından istenen biçimdeki veriler Dynamics 365 for Retail işlem veritabanından çıkarılır ve Varlık deposuna gönderilir.
-   Veriler, Azure Data Factory (ADF) tarafından ADF etkinliklerinin bir parçası olarak Hive betiği kullanan verileri temizlemek için kullanılır. Temizlenen veriler blob depolamada saklanır.
-   Blob depolamadaki veriler öneri modelini eğitmek amacıyla Bilişsel hizmetler API'sı tarafından kullanılır.

**Önerileri etkinleştir**'i açıp yapılandırma işlerini çalıştırdığınızda, aşağıdaki eylemler gerçekleşir.

-   Model kimlik bilgileri ve kimliği API'dan toplanır ve Dynamics 365 for Retail işlem veritabanında, AOS için web.config'de ve ayrıca perakende sunucusunda depolanır.
-   Model kimlik bilgileri ve kimliği CRT'nin kullanımına sunulur, böylece Bulut POS ve MPOS'tan çevrimiçi modda gelen ürün önerileri çağrıları değerlendirilir.


<a name="see-also"></a>Ayrıca bkz.
--------

[POS cihazındaki hareket sayfasına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md)




