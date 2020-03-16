---
title: Ambalaj malzemeleri ve ücretleri
description: Bu konu, belirli aralıklarda geri dönüşüm şirketleri için ödenen ambalaj malzemesi masrafları hakkında bilgi sağlar.
author: MarkusFogelberg
manager: AnnBe
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2351cce9dc6e1a554800817f75591c4a4e24d43
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076259"
---
# <a name="packing-materials-and-fees"></a>Ambalaj malzemeleri ve ücretleri

[!include [banner](../includes/banner.md)]

Ambalaj malzemesi masrafları, belirli aralıklarla bir geri dönüştürme şirketine ödenmektedir. Bir ambalaj birimini meydana getiren her malzeme için ağırlık birimi başına bir tutar ödenir. Ambalaj malzemesi masrafları hesaplanır ve raporlanır, fakat masraflar bir kuruma ödenecek vergiler olarak görülmediğinden, genel muhasebeye hareket nakledilmez.

Ambalaj malzemesi ağırlıkları ve masrafları satış sipariş satırları ve satınalma siparişi satırları için hesaplanır.

Tek madde, madde grubu (ambalaj grubu) veya tüm maddeler bazında bir veya birden fazla ambalaj birimi tanımlayabilirsiniz. Bir ambalaj birimi, ambalaj biriminde bulunan madde sayısı ve , ambalaj malzemeleri ve ağırlıklarını da içerir. Tanımlanan her tür ambalaj malzemesi için ambalaj malzemesi kodu atanır. Ambalaj malzemesi koduna göre belirli bir dönem için bir fiyat belirleyebilirsiniz. Ambalaj malzemesi masrafını bu bilgiler temel alınarak hesaplanır.

> [!NOTE]
> Şirketiniz ambalaj malzemesi masrafı ödemiyorsa dahi, bu işlevi ambalaj malzemesi ağırlıkları istatistiklerini hesaplamak amacıyla kullanabilirsiniz.

## <a name="allocations"></a>Ambalaj malzemesi tahsisatı ayarlama

Ambalaj malzemesi ağırlıklarını, ambalaj malzemesi masraflarını veya her ikisini birden hesaplayabilmeniz için, hesaplamayı etkinleştirmeniz ve hangi malzeme ve ücretlerin hangi maddelere uygulanacağını tanımlamanız gerekir.

1. **Stok yönetimi \> Kurulum \> Stok ve ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde **ambalaj malzemesi** bölümünde, **ambalaj malzemesi masraflarını hesapla** seçeneğini **Evet** olarak ayarlayın.
1. **Stok Yönetimi \> kurulum \> ambalaj malzemesi \> Ambalaj grupları**'na gidin ve kullandığınız tüm sevk gruplarını oluşturun. Bir ambalaj grubundaki tüm maddeler aynı ambalaj malzemesi tahsisatını kullanır. Ambalaj gruplarını kullanmıyorsanız, bu adımı atlayabilirsiniz.

    > [!TIP]
    > Ambalaj gruplarınızı oluşturduktan sonra, her ürüne gereksinim duyduğunuz gibi bir grup atayabilirsiniz. **Ürün bilgileri yönetimi \> ürünler \> Yayınlanan Ürünler**'e gidin, bir ürün seçin ve sonra **stok yönet** hızlı sekmesinde, **Ambalaj grubu** alanında uygun ambalaj grubunu seçin.

1. **Stok Yönetimi \> kurulum \>ambalaj malzemesi \> ambalaj malzemesi kodları** kullandığınız her ambalaj malzemesi tipini tanımlayın ve sevkiyatları hazırlarken ambalaj malzemesinin tüketilen birimi belirtin.
1. **Stok Yönetimi \> kurulum \>ambalaj malzemesi \> ambalaj malzemesi ücretlerine**gidin ve yeni tanımladığınız her ambalaj malzemesi türü için ücret ayarlayın. Ücretler, tüketilen birim başına düşen fiyata göre hesaplanır.
1. Maddelere ambalaj malzemesi tahsis etmek için **Stok yönetimi \> kurulum \> ambalaj malzemesi \> ambalaj malzemesi tahsisatı**'na gidin ve Tahsisatlar oluşturun. İhtiyaç duyduğunuz sayıda tahsisat oluşturabilirsiniz. Tahsisatlarınızın ne kadar ayrıntılı olmasını istediğinize bağlı olarak, belirli maddeler, madde grupları (Ambalaj grupları) veya tüm maddeler için ambalaj malzemeleri tahsis edebilirsiniz.

    Oluşturduğunuz her tahsisat için aşağıdaki adımları izleyin.

    1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

        - **Madde kodu** - Tahsisatın kapsamını seçin:

            - **Tablo** – Tek bir özel madde için tahsisat oluşturur.
            - **Grup** – **Ambalaj grupları** sayfasında tanımlanan bir ambalaj grubuna ait olan tüm maddeler için bir tahsisat oluşturur.
            - **Tümü** – Tüm maddeler için bir tahsisat oluşturur.

            > [!NOTE]
            > Genellikle tüm ayırmaların aynıdüzeyde (**tablo**, **grup** veya **tümü**) olması gerekir. Birden fazla düzey kullanırsanız her madde için en belirgin eşleşen tahsisat kullanılır. (**Tablo** düzeyi **grup** düzeyinden önceliklidir ve bu düzeylerin her ikisi de **tüm** düzeyden önceliklidir.)

        - **Madde ilişkisi** – Tek bir madde için tahsisat yapıyorsanız, maddeyi seçin. Bir madde grubu için tahsisat yapıyorsanız, ambalaj grubunu seçin. Tüm maddeler için tahsisat yapıyorsanız bu alanı boş bırakın.
        - **Konfigürasyon**, **Boyut**, **Renk**ve **Stil** – Tahsis ettiğiniz maddeyi daha ayrıntılı bir şekilde tanımlamak için bu boyutların gereksinim duyduğunuz değerleri girin.
        - **Ambalaj birimi** - Ambalaj malzemesi kullanıldığında maddenin paketlendiği birimi seçin. Bu birim, maddenin satın alındığı ve depolandığı birime göre farklılık gösterebilir.
        - **Ambalaj birimi faktörü** – Stok biriminden ambalaj birimine dönüştürmek için kullanılan dönüştürme faktörünü girin. (Dönüştürme *ambalaj birimleri* = *madde birimleri* × *ambalaj birimi faktörü* formülünü kullanır.)

    1. **Ambalaj malzemesi** hızlı sekmesinde, geçerli tahsisat için gerekli her ambalaj malzemesi parçasına bir satır ekleyin. Her satırda malzeme türünü ( **ambalaj malzemesi kodları** sayfasında tanımlandığı şekilde) ve geçerli maddenin her sevk edilen birimi için tüketilen tutarını belirtin.

## <a name="packing-units-on-sales-order-lines"></a>Satış siparişi satırlarındaki ambalaj birimleri

[Ambalaj malzemesi masraflarına yönelik hesaplamayı açtıktan ve tahsisatlarınızı ayarladıktan](#allocations) sonra, sistem bir satış siparişine eklenen her madde için ambalaj birimlerinin belirtilmiş olduğunu doğrular. Daha sonra, gerekli tüm ücretleri hesaplar. Bir madde satış siparişine eklendiğinde, aşağıdaki adımlardan biri gerçekleşir:

- **Eğer ambalaj tahsisatı ürün için geçerliyse:** Satış sipariş satırı, belirtilen ambalaj birimi ve ambalaj birim miktarı ile sistem tarafından güncelleştirilir. (Ambalaj birim miktarı, *Ambalaj birimi miktarı* = *Sipariş edilen miktar* ÷ *seçili ambalaj birimindeki madde sayısı* formülü kullanılarak hesaplanır.)
- **Maddeye hiçbir ambalaj tahsisatı uygulanmazsa**: Satış sipariş satırına el ile bir ambalaj birimi ve bir ambalaj birim miktarı girebilirsiniz.

Ayrıca, satış sipariş satırını naklettiğinizde ambalaj biriminin ve ambalaj birim miktarının değiştirebilirsiniz. Bu özellik sadece satış sipariş satırı kısmen teslim edilmiş veya kısmen faturalanmışsa mantıklı olur.

Satış siparişini faturaladığınızda, sistem ambalaj malzemesi hareketleri oluşturur. Ambalaj malzemesi hareketleri, satış satırı için ambalaj malzemelerinin ağırlıklarını içerir. Hareketleri faturaladıktan sonra değiştirebilirsiniz. Daha sonra yeni hareketler oluşturabilirsiniz.

## <a name="packing-units-on-purchase-order-lines"></a>Satınalma siparişi satırlarındaki ambalaj birimleri

Sistem, bir satınalma siparişi satırları için ambalaj malzemesi hareketleri oluşturmaz. Bunun yerine, Faturalanmış sipariş satırları için hareketleri **Ambalaj malzemesi hareketleri** sayfasında el ile oluşturabilirsiniz.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Ücretlendirilen ambalaj malzemesi ücretleri olan müşteriler için lisans numaraları ayarla

Belirli bir müşterinin satış siparişleri her sipariş için kullanılan ambalaj malzemeleriyle ilgili masrafları dahil etmelidir, aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Ambalaj malzemesi için faturalanması gereken müşteriyi seçin.
1. **Fatura ve teslimat** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Satış vergisi** bölümünde, **Ambalaj harcı lisans numarası** alanına şirketin lisans numarasını girin.
    - **Ambalaj malzeme ücreti** bölümünde, **Lisans numarası** alanına şirketin lisans numarasını girin.

Şimdi ambalaj malzemelerini kullanan bir veya daha fazla madde içeren bir satış siparişi oluşturup faturaladığınızda, fatura ambalaj malzemesi masraflarını gösterir.

Ambalaj malzemesi masraflarını ödemeyecek müşteriler için aynı adımları uygulayın, ancak **Ambalaj harcı lisans numarası** ve **lisans numarası** alanlarındaki Lisans numaralarını silin. Ambalaj malzemesi ücretlerini ödemeyecek müşterilerin faturaları ambalaj malzemelerinin ağırlıklarını gösterir, ancak bunlar ücretleri göstermez.

Şirketinizin belirli bir dönem için borçlu olduğu tüm ambalaj malzemesi masraflarını gösteren bir rapor oluşturmak için **stok yönetimi \> sorguları ve raporlar \> ambalaj malzemesi raporları \> ambalaj malzemesi ücreti hesaplamasına**gidin, bir tarih aralığı belirtin ve **Tamam**'ı seçin.

## <a name="print-packing-material-weights-on-invoices"></a>Ambalaj malzemesi ağırlıklarını faturalarda yazdırma

Ambalaj malzemesi ağırlıklarını yazdırmayı ve faturadaki ilgili ücretlerini kimin ödeyeceğini belirtebilirsiniz. Ambalaj koduna göre ağırlıklar özetlenmiştir.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
1. **Güncelleştirmeler** sekmesinde, **fatura** hızlı sekmesinde **ambalaj malzemesi ağırlığını Yazdır** seçeneğini **Evet** olarak ayarlayın.
