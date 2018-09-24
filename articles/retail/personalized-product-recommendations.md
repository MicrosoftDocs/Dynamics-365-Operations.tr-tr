---
title: "Kişiselleştirilmiş ürün önerileri"
description: "Bu konuda satış noktası (POS) cihazında görüntülenebilecek Dynamics 365 for Retail ürün önerileri hakkında bilgiler yer almaktadır."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 7925a37c595f5ffa040747462d3ea60a3da41858
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2018

---

# <a name="personalized-product-recommendations"></a>Kişiselleştirilmiş ürün önerileri

[!include [banner](includes/banner.md)]

> [!NOTE]
> Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz. Daha fazla bilgi için bkz. [Kaldırılan veya artık kullanılmayan özellikler](../dev-itpro/migration-upgrade/deprecated-features.md). 

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

## <a name="how-does-it-work"></a>Nasıl çalışır?
**Varlık deposu** varlığını yenilediğinizde, aşağıdaki eylemleri gerçekleşir.

-   Bilişsel hizmetler tarafından istenen biçimdeki veriler Dynamics 365 for Retail işlem veritabanından çıkarılır ve Varlık deposuna gönderilir.
-   Veriler, Azure Data Factory (ADF) tarafından ADF etkinliklerinin bir parçası olarak Hive betiği kullanan verileri temizlemek için kullanılır. Temizlenen veriler blob depolamada saklanır.
-   Blob depolamadaki veriler öneri modelini eğitmek amacıyla Bilişsel hizmetler API'sı tarafından kullanılır.

**Önerileri etkinleştir**'i açıp yapılandırma işlerini çalıştırdığınızda, aşağıdaki eylemler gerçekleşir.

-   Model kimlik bilgileri ve kimliği API'dan toplanır ve Dynamics 365 for Retail işlem veritabanında, AOS için web.config'de ve ayrıca perakende sunucusunda depolanır.
-   Model kimlik bilgileri ve kimliği CRT'nin kullanımına sunulur, böylece Bulut POS ve MPOS'tan çevrimiçi modda gelen ürün önerileri çağrıları değerlendirilir.

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Zaten etkinleştirilmiş ürün önerileriyle ilgili sorunları giderme 
> - **Perakende Parametreleri** > **Makine öğrenimi** > **Ürün önerilerini devre dışı bırak**'a gidin ve **Ürün yapılandırma işini [1110]** çalıştırın. **Makine öğrenimi** sekmesini bulamıyorsanız, lütfen Dynamics Destek birimine başvurun. 
> 
> - **Öneriler denetimini** hareket ekranınıza **Ekran düzeni tasarımcısını** kullanarak eklediyseniz bunu da kaldırın. 



<a name="additional-resources"></a>Ek kaynaklar
--------

[POS cihazındaki hareket sayfasına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md)




