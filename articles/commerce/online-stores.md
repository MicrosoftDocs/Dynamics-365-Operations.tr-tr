---
title: Çevrimiçi mağaza kanalı ayarlama
description: Bu makalede çevrimiçi mağaza kanalları ve Dynamics 365 Commerce'te bunların nasıl kurulacağı hakkında bilgi sağlanmaktadır.
author: kfend
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c427b0eba2120123a47f52029d70896be88b9ec0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024388"
---
# <a name="set-up-an-online-store-channel"></a>Çevrimiçi mağaza kanalı ayarlama

[!include [banner](includes/banner.md)]

Bu makalede çevrimiçi mağaza kanalları ve Dynamics 365 Commerce'te bunların nasıl kurulacağı hakkında bilgi sağlanmaktadır.

Commerce, birden fazla perakende kanalını destekler. Bu kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir. Çevrimiçi mağazalar, bir perakendeciye çevrimiçi mevcudiyet sağlarlar, böylelikle müşteriler ürünleri perakendeci'nin perakende mağazalarının yanı sıra çevrimiçi mağazasından da alabilirler. Müşteriler ürünleri çevrimiçi mağazadan satın alırlarsa, bu ürünler onlara sevk edilebilir veya müşteriler ürünleri yerel mağazasından alabilirler. 

Commerce istemcisinde bir çevrimiçi mağaza oluşturursunuz. Daha sonra bu çevrimiçi mağaza, Commerce ile entegre bir üçüncü taraf çevrimiçi mağazaya yayımlanır. Üçüncü taraf çevrimiçi mağaza, çevrimiçi mağaza için bir mağaza ön tarafı (UI) işlevi görür ve size müşteri yönetim sistemi (CMS) ve UI özellikleri seçeneğini verir. Bu tür sayısız entegrasyon mevcuttur. 

Çevrimiçi mağaza için tanımladığınız özellikler, çevrimiçi mağazanın davranışını kontrol eder. Örneğin, gezinme kategori hiyerarşisi tanımlar ve bunu çevrimiçi mağazaya atarsınız. Çevrimiçi mağazayı bir üçüncü taraf çevrimiçi mağazaya yayınlarsanız, gezinme kategori hiyerarşisi mağazanın çevrimiçi sürümünde belirir. Ardından alışveriş yapanlar gezinme kategori hiyerarşisini kullanarak çevrimiçi mağazada gezinebilir ve ürün arayabilirler. 

Bir çevrimiçi mağaza oluşturmak için, mağaza için hareketlerin işlenmesine imkan tanıyacak bileşenler ayarlamanız gerekir. Örneğin çeşit eklemeniz, öznitelik uygulamanız ve ödeme yöntemleri ve sevkıyat yöntemleri ayarlamanız gerekir. Öte yandan çevrimiçi mağazaya özel fiyatlar, promosyonlar, iskontolar, ticari anlaşmalar ve sevkıyat şartları da tanımlayabilirsiniz. 

Çevrimiçi mağazayı üçüncü taraf çevrimiçi mağazaya yayımladıktan sonra, çevrimiçi mağaza için ürün katalogları oluşturabilirsiniz. Katalogdaki ürünler, çevrimiçi mağaza ürün listeleri haline gelir. Alışveriş yapan biri çevrimiçi mağazadan ürün satın aldığında, mevcut stok güncellenir ve istemcide eşitlenir. Ayrıca, satınalmalar için satış emirleri de üretilir ve siparişin yerine getirilmesi ve işlenmesi için istemciye gönderilir.

## <a name="set-up-an-online-store"></a>Bir çevrimiçi mağaza ayarlama

Bir çevrimiçi mağaza ayarlamak için, aşağıdaki görevleri tamamlamanız gerekir.

1. Çevrimiçi mağazayı oluşturun.
2. Çevrimiçi mağazayı uygun organizasyon hiyerarşilerine ekleyin.
3. Çevrimiçi mağazada bulunan ürünleri içeren çeşitler ekleyin.
4. Çevrimiçi mağaza için fiyat grupları atayın veya oluşturun.
5. Çevrimiçi mağazada sunulan teslimat şekillerini ayarlayın.
6. Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.
7. Alışveriş yapanların ürünleri çevrimiçi sipariş etmesine ve ardından bunları yerel bir mağazadan almasına izin veriyorsanız, çevrimiçi mağazaya mağaza bulucu grupları atayın.
8. Çevrimiçi mağazaya kanallar, ürünler ve satış emirleri için öznitelikler atayın. Kanal öznitelikleri tüm çevrimiçi mağaza için geçerlidir, ürün öznitelikleri çevrimiçi mağazada sunulan ürünler için geçerlidir ve satış siparişi öznitelikleri, çevrimiçi mağazadan üretilen satış emirleri için geçerlidir.
9. Bu özniteliklerin çevrimiçi mağazada nasıl davranacağını belirleyen özellikler tanımlamak için öznitelikleri eşleyin. Örneğin, öznitelikler gerekli ya da aranabilir şeklinde tanımlanabilir.
10. Çevrimiçi mağazayı yayınlayarak üçüncü taraf çevrimiçi mağaza tercihinizin mağaza yapısını üretin.

    > [!IMPORTANT]
    > Çevrimiçi mağazayı yayımlamadan önce, ona bir dağıtım konumu ayarlamanız gerekir.

## <a name="commerce-channel-navigation-hierarchies"></a>Ticaret kanalı gezinme hiyerarşileri

Bir çevrimiçi mağaza oluşturmadan önce, onu kullanmak istediğiniz ticaret kanalı gezinme hiyerarşisini tanımlamanız gerekir. Kanal gezinme hiyerarşisi, mağaza yayımlandıktan sonra çevrimiçi mağazada görüntülenen kategori hiyerarşisini temsil eder. Çevrimiçi mağazaya ürün katalogları yayımladığınızda, katalogdaki ürünler kanalı gezinme hiyerarşisindeki kategorilerle eşlenir. Ardından, alışveriş yapanlar hiyerarşiyi kullanarak çevrimiçi mağazada gezinirler.

## <a name="organization-hierarchies"></a>Kuruluş hiyerarşileri

Kurum hiyerarşileri, ticaret kanalları oluşturmak ve işletmenizi oluşturan organizasyonlar arasındaki ilişkileri temsil etmesi için kullanılır. Çevrimiçi mağazalar ayarladığınızda, bunlara bir organizasyon hiyerarşisi ekleyebilirsiniz. Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır. 

Bir organizasyon hiyerarşisini oluşturduğunuzda, buna bir amaç atarsınız. Amaç, hiyerarşinin işletme yapısı içinde nasıl kullanıldığını gösterir. Mağaza operasyonlarınız için bir organizasyon hiyerarşisi oluşturabilir ve bu hiyerarşiyi ürün çeşitleri, stok yenilemeleri ve raporlama için kullanabilirsiniz. 

Alternatif olarak, her amaç için ayrı bir organizasyon hiyerarşisi de oluşturabilirsiniz. Öte yandan, aynı amaca sahip birden fazla hiyerarşi oluşturabilir ve her birine ayrı bir kanal atayabilirsiniz. Çevrimiçi mağazaya ürün katalogları yayımlamayı planlıyorsanız, en azından, çevrimiçi mağazayı ürün çeşitlerine yönelik bir organizasyon hiyerarşisine ekleyin. Katalogdaki ürünler, çevrimiçi mağazaya atanan ürün çeşitleri arasından seçilir. Katalog yayınlandığında, yayınlama işlemi, çevrimiçi mağazaya atanan ürün çeşidinin geçerlilik tarihlerini kataloga dahil ürünlerle karşılaştırarak hangi ürünlerin çevrimiçi mağazada sunulacağını belirler.
