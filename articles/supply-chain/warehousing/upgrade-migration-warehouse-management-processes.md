---
title: Ambar yönetimini Microsoft Dynamics AX 2012'den Supply Chain Management'a yükseltme
description: Bu konu, ürün ve ambar yönetimi geçiş seçenekleri hakkında bilgi sağlar.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac8c0d8781e5146186fbf71ce619f90ca3556ccefefe7e974efded7e0eb86dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775447"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Ambar yönetimini Microsoft Dynamics AX 2012'den Supply Chain Management'a yükseltme 


[!include [banner](../includes/banner.md)]

Bu konu, WMSII modülünü çalıştıran Microsoft Dynamics AX 2012 R3'ten Supply Chain Management'a yükseltme işlemi hakkında genel bakış sağlar.

Supply Chain Management artık Microsoft Dynamics AX 2012'den gelen eski **WMSII** modülünü desteklemiyor. Bunun yerine, **Ambar yönetimi** modülünü kullanabilirsiniz. WMSII modülünde mali stok için Yerleşim ve Palet Kodu stok boyutları seçilebilir ancak Palet kodu stok boyutu Supply Chain Management'ta mali stok için kullanılamaz.

Yükseltme sırasında, Palet kodu stok boyutu kullanan depolama boyutu grubuyla ilişkilendirilmiş tüm ürünler tanımlanır, engellenmiş olarak işaretlenir ve yükseltme için işlenmez.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>AX 2012 R3 WMSII kullanılırken Supply Chain Management'a yükseltme
Yükseltmenin ardından, yükseltme sırasında engellenen ürünlerin engelini kaldırmak için **Maddeler için depolama boyutu grubunu değiştir** formundaki seçenek kümesini kullanabilir ve bu ürünler için hareketleri işleyebilirsiniz.

### <a name="enabling-items-in-supply-chain-management"></a>Supply Chain Management'ta maddeleri etkinleştirme 
Supply Chain Management'ta madde izleme ambar yönetimi işlemlerinin bir parçası olduğundan bu değişikliğin yapılması gerekmiştir. Bu işlemler için tüm ambarların ve yerleşimlerinin bir yerleşim profiliyle eşleştirilmesi gerekir. Ambar yönetimi işlemlerini kullanmak istiyorsanız, aşağıdakilerin yapılandırılması gerekir:
-   Mevcut ambarlar ambar yönetimi işlemlerini kullanmak üzere etkinleştirilmelidir. 
-   Mevcut serbest bırakılan ürünler, ambar yönetimi işlemlerini kullanan bir depolama boyutu grubu ile ilişkilendirilmelidir. 

Kaynak depolama boyut grupları Palet Kodu stok boyutunu kullanıyorsa, Palet Kodu stok boyutunu kullanan mevcut eldeki stokların konumları **Plaka izlemeyi kullan** parametresinin seçili olduğu bir yerleşim profiliyle ilişkilendirilmelidir. Mevcut ambarların ambar yönetimi işlemlerini kullanmak üzere etkinleştirilmemesi gerekiyorsa, mevcut eldeki stok depolama boyutu gruplarını yalnızca Tesis, Ambar ve Yerleşim stok boyutlarını işleyen gruplarla değiştirebilirsiniz. 

> [!NOTE] 
>  Açık stok hareketleri olsa bile maddeler için depolama boyutu grubunu değiştirebilirsiniz.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Palet Kodu nedeniyle engellenen ürünleri bulma
Yükseltme sırasında engellenen ve işlenemeyen serbest bırakılan ürünlerin listesini görüntülemek için **Stok Yönetimi** &gt; **Kurulum** &gt; **Stok** &gt; **Stok güncelleştirmeleri için engellenen maddeler**'e tıklayın.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Engellenen ürünler için depolama boyutu grubunu değiştirme 
 
Ambar yönetimi işlemlerinin parçası olarak kullanılacak bir maddenin Yerleşim stok boyutunun etkin olduğu ve **Ambar yönetimi işlemlerini kullan** parametresinin seçili olduğu bir depolama boyutu grubuyla ilişkilendirilmiş olması gerekir. Bu ayar seçildiğinde Tesis, Ambar, Stok durumunu, Yerleşim ve Plaka stok boyutları etkinleşir.

Yükseltme sırasında engellenen ürünlerin engelini kaldırmak üzere ürünler için yeni bir depolama boyut grubunu seçmeniz gerekir. Açık stok hareketleri olsa bile depolama boyutu grubunu değiştirebilirsiniz. Yükseltme sırasında engellenen öğeleri kullanmak için iki seçeneğiniz vardır:

-   Madde için depolama boyut grubunu yalnızca Tesis, Ambar ve Yerleşim stok boyutlarını kullanan bir depolama boyutu grubuyla değiştirin. Bu değişikliğin bir sonucu olarak Palet Kodu stok boyutu artık kullanılmamaktadır.
-   Madde için depolama boyut grubunu ambar yönetimi işlemlerini kullanan bir depolama boyutu grubuyla değiştirin. Bu değişikliğin bir sonucu olarak artık Plaka stok boyutu kullanılmaktadır.

## <a name="configure-warehouse-management-processes"></a>Ambar yönetimi işlemlerini yapılandırma
**Ambar yönetimi** modülünde serbest bırakılan ürünleri kullanabilmeniz için ürünlerin **Ambar yönetimi işlemlerini kullan** parametresinin seçili olduğu bir depolama boyutu kullanması gerekir.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Ambarları ambar yönetimi süreçlerini kullanmak üzere etkinleştirme

1.  En az bir yeni konum profili oluşturun.
2.  **Ambar yönetimi** &gt; **Kurulum** &gt; **Ambar yönetimi işlemlerini etkinleştir** &gt; **Ambar kurulumunu etkinleştir**'i tıklayın.
3.  **Ambar kurulumunu etkinleştir** sayfasında, etkinleştirilmesi gereken ambarları ekleyin. Bu adımı doğrudan sayfadan veya Microsoft Office tümleştirme kullanarak gerçekleştirebilirsiniz.
4.  Tüm yerleşimlere yerleşim profili atayın. Bu adımı kolaylıkla Microsoft Office tümleştirmeyi doğrudan sayfadan kullanarak gerçekleştirebilirsiniz. Verileri dışa veya içe aktarabilir veya [Veri yönetimi](../../fin-ops-core/dev-itpro/data-entities/data-entities.md) içindeki veri varlığı işlemeyi kullanabilirsiniz.
5.  Değişiklikleri doğrulayın. Doğrulama işleminin bir parçası olarak çeşitli veri bütünlüğünü doğrulamaları oluşur. Daha büyük bir yükseltme işleminin bir parçası olarak, oluşan sorunların kaynak uygulamasında düzeltilmesi gerekebilir. Bu durumda, ek veri yükseltme gerekir.
6.  Değişiklikleri işleyin.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Maddeler için depolama boyutu grubunu, ambar yönetimi işlemlerini kullanacak şekilde değiştirin.

1.  Yeni **Stok durumu** değeri oluşturun ve değeri **Ambar yönetimi parametreleri** ayarlarında **Varsayılan stok durum kodu** değeri olarak atayın.
2.  **Ambar yönetimi işlemleri kullan** parametresinin seçili olduğu yeni depolama boyut grubu oluşturun.
3.  **Rezervasyon hiyerarşisi** sayfasında, maddenin depolama ve izleme boyut gruplarına göre yeni bir ayırma hiyerarşisi tanımlayın.
4.  En azından maddenin stok birimleri için kullanılanlarla aynı birimleri içeren bir veya daha fazla birim sırası grupları oluşturun.
5.  **Ambar yönetimi** &gt; **Kurulum** &gt; **Ambar yönetimi işlemlerini etkinleştir** &gt; **Maddeler için depolama boyutu grubunu değiştir**'i tıklayın.
6.  **Maddeler için depolama boyutu grubunu değiştir** sayfasında madde numaraları, depolama boyut grupları ve birim sıra grupları ekleyin. Bu adımı Microsoft Officetümleştirmesi kullanarak doğrudan sayfa üzerinde veya [Veri yönetimi](../../fin-ops-core/dev-itpro/data-entities/data-entities.md) içindeki veri varlığı işlemini kullanarak tamamlayabilirsiniz.
7.  Değişiklikleri doğrulayın. Doğrulama işleminin bir parçası olarak çeşitli veri bütünlüğünü doğrulamaları oluşur. Daha büyük bir yükseltme işleminin bir parçası olarak, oluşan sorunların kaynak uygulamasında düzeltilmesi gerekebilir. Bu durumda, ek veri yükseltme gerekir.
8.  Değişiklikleri işleyin. Stok boyutlarının güncelleştirilmesi biraz zaman alabilir. İlerlemeyi toplu iş görevlerini kullanarak izleyebilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]