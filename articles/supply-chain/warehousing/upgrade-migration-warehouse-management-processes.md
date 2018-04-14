---
title: "Ürün ve ambar yönetimi AX 2012'den Finance and Operations'a geçirme"
description: "Bu konu, ürün ve ambar yönetimi geçiş seçenekleri hakkında bilgi sağlar."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 92d0b4dd9611de4d717f30dc8736c673835bea29
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>Ürün ve ambar yönetimi AX 2012'den Finance and Operations'a geçirme

[!INCLUDE [banner](../includes/banner.md)]

Bu konu Microsoft Dynamics 365 for Finance and Operations içindeki ürün ve ambar yönetimi taşıma seçeneklerine genel bir bakış sağlar.

<a name="introduction"></a>Giriş
------------

Finance and Operations'a yükseltme sırasında, ayarları Finance and Operations'daki depolama boyutu grubu ayarlarıyla eşleşmeyen bir depolama boyutu grubuyla ilişkilendirilmiş olması durumunda ürünler bloke edilir. Ancak, yükseltmenin ardından, yükseltmek sırasında engellenen ürünlerin engelini kaldırmak için **Maddeler için depolama boyutu grubunu değiştir** işlemindeki geçiş seçenekleri kümesini kullanabilirsiniz. Bu ürünler için hareketleri daha sonra işleyebilirsiniz. Maddelerinizin bazıları zaten Tesis, Ambar ve Yerleşim stok boyutlarının etkin olduğu ve fiziksel olarak takip edildiği depolama boyutu gruplarıyla ilişkilendirilmiş olabilir. Bu durumda, **Maddeler için depolama boyutu grubunu değiştir** işlemini kullanarak bu maddeleri ambar yönetimi işlemlerinde kullanılmak üzere etkinleştirebilirsiniz. Mevcut maddeler için ambar yönetimi işlevlerini kullanmak istiyorsanız, bu özellik yararlıdır.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>AX 2012 R3 WMSII kullanıldığında, Finance and Operations'a yükseltme
Finance and Operations, artık Microsoft Dynamics AX 2012'deki eski **WMSII** modülünü desteklememektedir. Bunun yerine, yeni **Ambar yönetimi** modülünü kullanabilirsiniz. Önceki sürümlerde, mali stok için Yerleşim ve Palet kodu stok boyutları seçilebilirdi. Bununla birlikte, yükseltme işleminin bir parçası olarak, Paket kodu stok boyutu artık mali stok için etkinleştirilemez. Palet Kodu stok boyutunu kullanan depolama boyut grubuyla ilişkilendirilmiş tüm ürünleri engellenir ve işlenmez.

### <a name="enabling-items-in-finance-and-operations"></a>Finance and Operations'da maddeleri etkinleştirme

Finance and Operations'da, ambar yönetimi işlemlerinin parçası olarak kullanılacak maddelerin **Ambar yönetimi işlemlerini kullan** parametresinin seçili olduğu bir depolama boyutu grubuyla ilişkilendirilmiş olması gerekir. Bu ayar seçildiğinde Tesis, Ambar, Stok durumunu, Yerleşim ve Plaka stok boyutları etkinleşir. Bu tür depolama boyutu grubunu yalnızca zaten Yerleşim stok boyutu etkinleştirilmiş olan depolama boyutu gruplarıyla ilişkilendirilmiş olan maddeler için kullanabilirsiniz.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Stok güncelleştirmeleri için engellenen maddeler

Yükseltme sırasında engellenen ve işlenemeyen serbest bırakılan ürünlerin listesini görüntülemek için **Stok Yönetimi** &gt; **Kurulum** &gt; **Stok** &gt; **Stok güncelleştirmeleri için engellenen maddeler**'e tıklayın.

### <a name="reapplying-blocked-products"></a>Engellenen ürünleri yeniden uygulama

Yükseltme sırasında engellenen ürünlerin engelini kaldırmak üzere ürünler için yeni bir depolama boyut grubunu seçmeniz gerekir. Açık stok hareketleri olsa bile depolama boyutu grubunu değiştirebilirsiniz. Yükseltme sırasında engellenen öğeleri kullanmak için iki seçeneğiniz vardır:

-   Madde için depolama boyut grubunu yalnızca Tesis, Ambar ve Yerleşim stok boyutlarını kullanan bir depolama boyutu grubuyla değiştirin. Bu değişikliğin bir sonucu olarak Palet Kodu stok boyutu artık kullanılmamaktadır.
-   Madde için depolama boyut grubunu ambar yönetimi işlemlerini kullanan bir depolama boyutu grubuyla değiştirin. Bu değişikliğin bir sonucu olarak artık Plaka stok boyutu kullanılmaktadır.

### <a name="migration-processes"></a>Taşıma işlemleri

Finance and Operations'da madde izleme ambar yönetimi işlemlerinin bir parçasıdır. Bu işlemler için tüm ambarların ve yerleşimlerinin bir yerleşim profiliyle eşleştirilmesi gerekir. Ambar yönetimi işlemlerini kullanmak istiyorsanız, kavramsal olarak, iki işlemin ele alınması gerekir:

-   Mevcut ambarlar ambar yönetimi süreçlerini kullanmak üzere etkinleştirilmelidir.
-   Mevcut serbest bırakılan ürünler, ambar yönetimi işlemlerini kullanan yeni bir depolama boyutu grubu ile ilişkilendirilmelidir.

Kaynak depolama boyut grupları Palet Kodu stok boyutunu kullanıyorsa, Palet Kodu stok boyutunu kullanan mevcut eldeki stokların konumları **Plaka izlemeyi kullan** parametresinin seçili olduğu bir yerleşim profiliyle ilişkilendirilmelidir. Mevcut ambarların ambar yönetimi işlemlerini kullanmak üzere etkinleştirilmemesi gerekiyorsa, mevcut eldeki stok depolama boyutu gruplarını yalnızca Tesis, Ambar ve Yerleşim stok boyutlarını işleyen gruplarla değiştirebilirsiniz.

### <a name="using-the-warehouse-management-processes"></a>Ambar yönetimi süreçlerini kullanma

**Ambar yönetimi** modülünde serbest bırakılan ürünleri kullanabilmeniz için ürünlerin **Ambar yönetimi işlemlerini kullan** parametresinin seçili olduğu bir depolama boyutu kullanması gerekir.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Ambarları ambar yönetimi süreçlerini kullanmak üzere etkinleştirme

1.  En az bir yeni konum profili oluşturun.
2.  **Ambar yönetimi** &gt; **Kurulum** &gt; **Ambar yönetimi işlemlerini etkinleştir** &gt; **Ambar kurulumunu etkinleştir**'i tıklayın.
3.  **Ambar kurulumunu etkinleştir** sayfasında, etkinleştirilmesi gereken ambarları ekleyin. Bu adımı doğrudan sayfadan veya Microsoft Office tümleştirme kullanarak gerçekleştirebilirsiniz.
4.  Tüm yerleşimlere yerleşim profili atayın. Bu adımı kolaylıkla Microsoft Office tümleştirmeyi doğrudan sayfadan kullanarak gerçekleştirebilirsiniz. Verileri dışa veya içe aktarabilir veya [Veri yönetimi](../../dev-itpro/data-entities/data-entities.md) içindeki veri varlığı işlemeyi kullanabilirsiniz.
5.  Değişiklikleri doğrulayın. Doğrulama işleminin bir parçası olarak çeşitli veri bütünlüğünü doğrulamaları oluşur. Daha büyük bir yükseltme işleminin bir parçası olarak, oluşan sorunların kaynak uygulamasında düzeltilmesi gerekebilir. Bu durumda, ek veri yükseltme gerekir.
6.  Değişiklikleri işleyin.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Maddeler için depolama boyutu grubunu, ambar yönetimi işlemlerini kullanacak şekilde değiştirin.

1.  Yeni **Stok durumu** değeri oluşturun ve değeri **Ambar yönetimi parametreleri** ayarlarında **Varsayılan stok durum kodu** değeri olarak atayın.
2.  **Ambar yönetimi işlemleri kullan** parametresinin seçili olduğu yeni depolama boyut grubu oluşturun.
3.  **Rezervasyon hiyerarşisi** sayfasında, maddenin depolama ve izleme boyut gruplarına göre yeni bir ayırma hiyerarşisi tanımlayın.
4.  En azından maddenin stok birimleri için kullanılanlarla aynı birimleri içeren bir veya daha fazla birim sırası grupları oluşturun.
5.  **Ambar yönetimi** &gt; **Kurulum** &gt; **Ambar yönetimi işlemlerini etkinleştir** &gt; **Maddeler için depolama boyutu grubunu değiştir**'i tıklayın.
6.  **Maddeler için depolama boyutu grubunu değiştir** sayfasında madde numaraları, depolama boyut grupları ve birim sıra grupları ekleyin. Bu adımı Microsoft Office tümleştirmesi kullanarak doğrudan sayfa üzerinde veya [Veri yönetimi](../../dev-itpro/data-entities/data-entities.md) içindeki veri varlığı işlemini kullanarak tamamlayabilirsiniz.
7.  Değişiklikleri doğrulayın. Doğrulama işleminin bir parçası olarak çeşitli veri bütünlüğünü doğrulamaları oluşur. Daha büyük bir yükseltme işleminin bir parçası olarak, oluşan sorunların kaynak uygulamasında düzeltilmesi gerekebilir. Bu durumda, ek veri yükseltme gerekir.
8.  Değişiklikleri işleyin. Stok boyutlarının güncelleştirilmesi biraz zaman alabilir. İlerlemeyi toplu iş görevlerini kullanarak izleyebilirsiniz.



