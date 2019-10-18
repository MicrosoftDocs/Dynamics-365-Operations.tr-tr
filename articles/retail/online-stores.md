---
title: Çevrimiçi mağazaları ayarlama
description: Bu makalede Retail çevrimiçi mağazalar ve Dynamics 365 Retail'te bunların nasıl kurulacağı hakkında bilgiler verilmiştir.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 02402269a6976ff856e703cc8e94fbf0758ea771
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017978"
---
# <a name="set-up-online-stores"></a>Çevrimiçi mağazalar ayarlama

[!include [banner](includes/banner.md)]

Bu makalede Retail çevrimiçi mağazalar ve Dynamics 365 Retail'te bunların nasıl kurulacağı hakkında bilgiler verilmiştir.

Retail, birden fazla perakende kanalını destekler. Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir. Çevrimiçi mağazalar, bir perakendeciye çevrimiçi mevcudiyet sağlarlar, böylelikle müşteriler ürünleri perakendeci'nin perakende mağazalarının yanı sıra çevrimiçi mağazasından da alabilirler. Müşteriler ürünleri çevrimiçi mağazadan satın alırlarsa, bu ürünler onlara sevk edilebilir veya müşteriler ürünleri yerel perakende mağazasından alabilirler. Retail istemcisinde bir çevrimiçi mağaza oluşturursunuz. Daha sonra bu çevrimiçi mağaza, Retail ile entegre bir üçüncü taraf çevrimiçi mağazaya yayımlanır. Üçüncü taraf çevrimiçi mağaza, çevrimiçi mağaza için bir mağaza ön tarafı (UI) işlevi görür ve size müşteri yönetim sistemi (CMS) ve UI özellikleri seçeneğini verir. Bu tür sayısız entegrasyon mevcuttur. Çevrimiçi mağaza için tanımladığınız özellikler, çevrimiçi mağazanın davranışını kontrol eder. Örneğin, Retail'da gezinme kategori hiyerarşisi tanımlar ve bunu çevrimiçi mağazaya atarsınız. Çevrimiçi mağazayı bir üçüncü taraf çevrimiçi mağazaya yayınlarsanız, gezinme kategori hiyerarşisi mağazanın çevrimiçi sürümünde belirir. Ardından alışveriş yapanlar gezinme kategori hiyerarşisini kullanarak çevrimiçi mağazada gezinebilir ve ürün arayabilirler. Bir çevrimiçi mağaza oluşturmak için, mağaza için hareketlerin işlenmesine imkan tanıyacak bileşenler ayarlamanız gerekir. Örneğin çeşit eklemeniz, öznitelik uygulamanız ve ödeme yöntemleri ve sevkıyat yöntemleri ayarlamanız gerekir. Öte yandan çevrimiçi mağazaya özel fiyatlar, promosyonlar, iskontolar, ticari anlaşmalar ve sevkıyat şartları da tanımlayabilirsiniz. Çevrimiçi mağazayı üçüncü taraf çevrimiçi mağazaya yayımladıktan sonra, çevrimiçi mağaza için perakende ürün katalogları oluşturabilirsiniz. Katalogdaki ürünler, çevrimiçi mağaza ürün listeleri haline gelir. Alışveriş yapan biri çevrimiçi mağazadan ürün satın aldığında, mevcut stok güncellenir ve istemcide eşitlenir. Ayrıca, satınalmalar için satış emirleri de üretilir ve siparişin yerine getirilmesi ve işlenmesi için istemciye gönderilir.

## <a name="set-up-an-online-store"></a>Bir çevrimiçi mağaza ayarlama

Bir çevrimiçi mağaza ayarlamak için, aşağıdaki görevleri tamamlamanız gerekir.

1. Çevrimiçi mağazayı oluşturun.
2. Çevrimiçi mağazayı uygun organizasyon hiyerarşilerine ekleyin.
3. Çevrimiçi mağazada bulunan ürünleri içeren çeşitler ekleyin.
4. Çevrimiçi mağaza için fiyat grupları atayın veya oluşturun.
5. Çevrimiçi mağazada sunulan teslimat şekillerini ayarlayın.
6. Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.
7. Alışveriş yapanların ürünleri çevrimiçi sipariş etmesine ve ardından bunları yerel bir mağazadan almasına izin veriyorsanız, çevrimiçi mağazaya mağaza bulucu grupları atayın.
8. Çevrimiçi mağazaya kanallar, ürünler ve satış emirleri için öznitelikler atayın. Kanal öznitelikleri tüm çevrimiçi mağaza için geçerlidir, ürün öznitelikleri çevrimiçi mağazada sunulan ürünler için geçerlidir ve satış emri öznitelikleri, çevrimiçi mağazadan üretilen satış emirleri için geçerlidir.
9. Bu özniteliklerin çevrimiçi mağazada nasıl davranacağını belirleyen özellikler tanımlamak için öznitelikleri eşleyin. Örneğin, öznitelikler gerekli ya da aranabilir şeklinde tanımlanabilir.
10. Çevrimiçi mağazayı yayınlayarak üçüncü taraf çevrimiçi mağaza tercihinizin mağaza yapısını üretin.

    > [!IMPORTANT]
    > Çevrimiçi mağazayı yayımlamadan önce, ona bir dağıtım konumu ayarlamanız gerekir.

## <a name="retail-channel-navigation-hierarchies"></a>Perakende kanalı gezinme hiyerarşileri

Bir çevrimiçi mağaza oluşturmadan önce, onu kullanmak istediğiniz perakende kanalı gezinme hiyerarşisini tanımlamanız gerekir. Perakende kanalı gezinme hiyerarşisi, mağaza yayımlandıktan sonra çevrimiçi mağazada görüntülenen kategori hiyerarşisini temsil eder. Çevrimiçi mağazaya perakende ürün katalogları yayımladığınızda, katalogdaki ürünler perakende kanalı gezinme hiyerarşisindeki kategorilerle eşlenir. Ardından, alışveriş yapanlar hiyerarşiyi kullanarak çevrimiçi mağazada gezinirler.

## <a name="organization-hierarchies"></a>Kuruluş hiyerarşileri

Organizasyon hiyerarşileri, perakende kanallarını yapılandırmak için kullanılır. Organizasyon hiyerarşileri, organizasyonlar arasındaki işinizi meydana getiren ilişkileri temsil eder. Çevrimiçi mağazalar ayarladığınızda, bunlara bir organizasyon hiyerarşisi ekleyebilirsiniz. Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır. Bir organizasyon hiyerarşisini oluşturduğunuzda, buna bir amaç atarsınız. Amaç, hiyerarşinin işletme yapısı içinde nasıl kullanıldığını gösterir. Mağaza operasyonlarınız için bir organizasyon hiyerarşisi oluşturabilir ve bu hiyerarşiyi ürün çeşitleri, stok yenilemeleri ve raporlama için kullanabilirsiniz. Alternatif olarak, her amaç için ayrı bir organizasyon hiyerarşisi de oluşturabilirsiniz. Öte yandan, aynı amaca sahip birden fazla hiyerarşi oluşturabilir ve her birine ayrı bir kanal atayabilirsiniz. Çevrimiçi mağazaya perakende ürün katalogları yayımlamayı planlıyorsanız, en azından, çevrimiçi mağazayı ürün çeşitlerine yönelik bir organizasyon hiyerarşisine ekleyin. Katalogdaki ürünler, çevrimiçi mağazaya atanan ürün çeşitleri arasından seçilir. Katalog yayınlandığında, yayınlama işlemi, çevrimiçi mağazaya atanan ürün çeşidinin geçerlilik tarihlerini kataloga dahil ürünlerle karşılaştırarak hangi ürünlerin çevrimiçi mağazada sunulacağını belirler.
