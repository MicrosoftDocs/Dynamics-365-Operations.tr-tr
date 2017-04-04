---
title: "Kişiselleştirilmiş ürün önerileri genel bakış"
description: "İşlemler için Dynamics 365 içinde ürün önerileri on the point of satış (POS) aygıtı görüntülenebilir. Öneriler müşteri kendi satın alma geçmişi, onların istek listesindeki öğeleri ve diğer müşterilerin çevrimiçi satın alınan maddeleri ve Tuğla Dibek depolarında göre ilgilenebileceğiniz maddelerdir. Büyük kataloglar ile Perakendeciler için öneriler müşteri ile ürün bulma yardımı. Bir müşterinin ilgi ve satın alma alışkanlıkları hedeflenen ürünleri vitrini, ürün önerileri Perakendeciler satışını ve çapraz satış ile yardımcı olabilir ve müşteri tutma geliştirebilirsiniz. İşlemler için Dynamics 365 içinde ürün önerileri kavrama Hizmetleri ve Microsoft Azure makine öğrenme tarafından güç sağlar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Kişiselleştirilmiş ürün önerileri genel bakış

İşlemler için Dynamics 365 içinde ürün önerileri on the point of satış (POS) aygıtı görüntülenebilir. Öneriler müşteri kendi satın alma geçmişi, onların istek listesindeki öğeleri ve diğer müşterilerin çevrimiçi satın alınan maddeleri ve Tuğla Dibek depolarında göre ilgilenebileceğiniz maddelerdir. Büyük kataloglar ile Perakendeciler için öneriler müşteri ile ürün bulma yardımı. Bir müşterinin ilgi ve satın alma alışkanlıkları hedeflenen ürünleri vitrini, ürün önerileri Perakendeciler satışını ve çapraz satış ile yardımcı olabilir ve müşteri tutma geliştirebilirsiniz. İşlemler için Dynamics 365 içinde ürün önerileri kavrama Hizmetleri ve Microsoft Azure makine öğrenme tarafından güç sağlar.

<a name="scenarios"></a>Senaryolar
---------

Ürün önerileri POS aşağıdaki senaryolar için etkinleştirilir. Bunlar, bulut POS veya Modern POS (MPOS) kullanılabilir.

1.  Üzerinde **ürün ayrıntıları** sayfa:

-   Mağaza ziyaret ilişkilendirirseniz bir **ürün ayrıntıları** önceki hareketleri sırasında farklı kanallar arasında öneri motoru önerdiği ek bakarak bu öğeler, sayfa büyük olasılıkla birlikte satın alınması.
-   Mağaza ilişkilendirirseniz müşteri harekete ekler ve daha sonra ziyaret bir **ürün ayrıntıları** sayfa, öneri motoru müşteri hareket geçmişini kullanarak kişiselleştirilmiş öneriler sağlar.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

1.  Üzerinde **hareket** sayfa:

-   Öneri motoru sepetindeki öğeleri tüm listeyi temel alan öğeleri önerir.
-   Mağaza ilişkilendirirseniz harekete bir müşteri ekler, öneri motoru sepette müşteri hareket geçmişini ve öğelerin listesini kullanarak kişisel öneriler sağlar.

**Not** önerilerini görüntülemek için **hareket** sayfa, satıcıya gereken işlemleri için Dynamics 365 ekran düzende güncelleştirmek. **Önerileri** denetimi atlanıyor, üzerinde **hareket** sayfa. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  Üzerinde **Müşteri ayrıntıları** sayfa:
    -   Kullanıcı kimliği ve müşterinin istek listesindeki öğeleri temel alarak madde öneri motoru önerir.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Dynamics 365 POS önerileri etkinleştirme işlemleri için yapılandırma
Ürün önerileri ayarlamak için aşağıdakileri yapmanız gerekir.

1.  Doğru seçtiğinizden emin olun **tüzel kişilik**.
2.  Gidin **varlık deposu**seçin **perakende satış**ı **yenileme**. ** ** Bu demo verileri (veya veri) operasyonel veritabanınızdan kullanın ve varlık deposuna taşıyın.
3.  İsteğe bağlı: öneriler hareket ekranda görüntülemek için Git ** ekran düzeni, **ekran Mizanpaj, başlatma **ekran düzeni tasarımcısı**,** ** ve sonra bırak ** öneriler denetim ** gereken yerde.
4.  Git **perakende parametreleri**seçin **makine öğrenme**, select ** Evet ** altında **POS etkinleştirmek önerileri**.
5.  POS üzerinde önerileri görmek için genel yapılandırma işlemi çalıştırmak **1110**. POS ekran düzeni tasarımcısı için yapılan değişiklikleri yansıtacak şekilde kanalı yapılandırma işlemi çalıştırmak **1070**.

## <a name="how-does-it-work"></a>[]()Nasıl çalışır?
Yenilediğinizde **varlık deposu** varlığı, aşağıdaki eylemleri yer.

-   Algılama hizmetleri tarafından gerekli biçiminde veri işlemsel veritabanı işlemleri için Dynamics 365 ayıklanacağı ve varlık depoya gönderilen.
-   Veri ADF etkinlikleri kapsamında kovanı komut dosyaları kullanarak veri temizlemeyi Azure veri fabrikası (ADF) tarafından kullanılır. Cleansed veri blob deposunda saklanır.
-   Blob depolama biriminden verileri bir öneri modeli eğitmek için API algılama hizmetleri tarafından kullanılır.

Açmak ne zaman **önerileri etkinleştirme** ve yapılandırma işlemlerini çalıştıracak, aşağıdaki eylemler gerçekleşir.

-   Model kimlik ve kimlik API'dan toplanma ve işlemsel veritabanı işlemleri için Dynamics 365, AOS için Web.config dosyasında ve ayrıca perakende sunucusunda depolanır.
-   Çevrimiçi modda bulut POS ve MPOS ürün önerileri aramaları kabul edilir böylece model kimlik ve kimlik CRT için kullanılabilir yapılır.


<a name="see-also"></a>Ayrıca bkz.
--------

[POS aygıt hareket sayfasında önerileri denetimi ekleyin](add-recommendations-control-pos-screen.md)


