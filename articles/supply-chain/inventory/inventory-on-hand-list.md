---
title: Eldeki stok listesi
description: Bu konu, eldeki stok ayrıntılarını incelemek için Eldeki stok listesi sayfasının nasıl kullanılacağını açıklar. Çeşitli filtreleme ve sıralama seçeneklerinin birlikte çalışması ve bu seçeneklerin kimi zaman birleştirildiklerinde beklenmedik sonuçlar üretebileceği birçok yolu gösterir.
author: sherry-zheng
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 275a37cd76715ab9909e057ec759c66c4f9c617b
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829861"
---
# <a name="inventory-on-hand-list"></a>Eldeki stok listesi

[!include [banner](../includes/banner.md)]

Bu konu, eldeki stok ayrıntılarını incelemek için **Eldeki stok listesi** sayfasının nasıl kullanılacağını açıklar. Çeşitli filtreleme ve sıralama seçeneklerinin birlikte çalışması ve bu seçeneklerin kimi zaman birleştirildiklerinde beklenmedik sonuçlar üretebileceği birçok yolu gösterir.

## <a name="query-your-on-hand-inventory"></a>Eldeki stokunuza sorgu gönderme

Stok bulunabilirliğini denetlemek için **Stok Yönetimi \> Sorguları ve raporlar \> Eldeki liste**'ye gidin.

Stokta hareketler yapıldığında **Eldeki liste** sayfası otomatik olarak güncelleştirilir. Bu hareketler tahmin edilen, fiziksel veya mali hareketler olabilir.

Aradığınız ürünleri bulmak için aşağıdaki araçları kullanın:

- Eylem bölmesinde, **Eldeki** kılavuzunda gösterilen sütunları ekleyebileceğiniz veya kaldırabileceğiniz bir iletişim kutusu açmak için [**Boyutlar**](#dimensions)'ı seçin.
- [**Filtreler** bölmesine](#filters-pane), yalnızca bu değerlere uyan kayıtları göstermek için belirli alanların değerlerini girin. Burada tanımladığınız filtrelerin, göstermeyi seçtiğiniz boyutlara göre daha sonra toplanabilir kaynak tablolar için geçerli olduğunu unutmayın. Bu davranışın sonuçlarınızı nasıl etkileyeceği hakkında bilgi için bu konunun devamındaki [örnekler](#examples) bölümüne bakın.
- **Filtreler** bölmesinde, **Eldeki stok** kılavuzunda eşleştirilen eldeki stok listesini oluşturmak için **Uygula**'yı seçin.
- **Eldeki** kılavuzunda, ilgili sütundaki değerlere göre sıralama veya filtreleme için herhangi bir sütun başlığı seçin. Kılavuzun üst kısmındaki hızlı filtre ek filtre uygulama seçenekleri sağlar. Bu filtreler kaynak tablolar değil, sonuçlar için geçerlidir. Bu davranışın sonuçlarınızı nasıl etkileyeceği hakkında bilgi için bu konunun devamındaki [örnekler](#examples) bölümüne bakın.

Her eşleşen kalem için **Eldeki** kılavuzu aşağıdaki stok bilgileri sütunlarını sağlar.

| Sütun | Tanım |
|---|---|
| Fiziksel stok | Stokta bulunan kullanılabilecek fiili miktar. |
| Fiziksel rezerve miktar | Fiziksel olarak rezerve edilen toplam miktar. |
| Kullanılabilir fiziksel miktar | Fiziksel stokta bulunan mevcut (rezerve edilmemiş) miktar.<p>**Kullanılabilir fiziksel**, hesaplanan bir alandır. Değer **Fiziksel stok** değeri eksi **Fiziksel rezerve edilen** değer şeklinde hesaplanır.</p> |
| Ek boyutlarda kullanılabilir fiziksel miktar | Kılavuzda gösterilen tüm boyutlar için kullanılabilir fiziksel miktar. |
| Toplam sipariş edilen | Gelen siparişlere dahil edilen veya çeşitli stok günlüklerinde pozitif miktarı olan toplam miktar. |
| Siparişte | Giden siparişlere dahil edilen veya çeşitli stok günlüklerinde negatif miktarı olan toplam miktar. |
| Siparişli rezerve miktar | Sipariş edilen girişlerde rezerve edilen toplam miktar. Bu alandaki değer, _Siparişli rezerve_ durumuna sahip giden hareketlerdeki toplam kalem miktarını gösterir. Sipariş edilen olarak rezerve edilen kalemler stokta fiziksel olarak yoktur. Bu nedenle, bunlar doğrudan çekilemez ve teslim edilemez. |
| Rezerve edilebilir | Eldeki stokun rezerve edilebilecek toplam miktarı.<p>**Not:** **Stok ve ambar yönetimi parametreleri** sayfasında **Sipariş edilen kalemleri rezerve et** onay kutusu işaretlenmişse, bu alandaki değer beklenen girişleri içerir. Onay kutusu işaretli değilse değer beklenen girişleri hariç tutar.</p> |
| Toplam kullanılabilir miktar | Toplam kullanılabilir miktar.<p>**Kullanılabilir toplam**, hesaplanan bir alandır. Değer, **Kullanılabilir fiziksel** değeri artı **Sipariş edilen toplam** değeri eksi **Siparişte** değerine eşittir.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Aradığınız kayıtları bulmak için filtre uygulama

Eldeki stok listesini yalnızca alan değerlerinin filtre ölçütüne uyan kayıtları içerecek şekilde filtrelemek için **Filtreler** bölmesini kullanın. Filtre tanımlamak için şu adımları izleyin.

1. **Filtreler** bölmesinde, filtrelemek istediğiniz alanı bulun.
2. Hedef alanın adının altındaki alanda bir mantıksal işleç (örneğin, *şununla başlar*, *eşittir* veya *büyüktür*) seçin.
3. Arayacağınız değeri girin veya seçin.

> [!IMPORTANT]
> **Eldeki liste** sayfası, kullanılabilir tüm boyutları içeren ayrıntılı bir eldeki stok tablosundan toplanır. Ancak bu sayfadaki liste bir özettir. Bu nedenle, gösterilen boyutlara göre değerleri toplayarak kaynak tablodaki satırları birleştirebilir.
>
> **Filtreler** bölmesinde tanımladığınız filtreler, toplanan listeye değil, kaynak tabloya uygulanır. Bu davranış bazen beklenmeyen sonuçlara neden olabilir. Bu davranışın sonuçlarınızı nasıl etkileyeceği hakkında bilgi için bu konunun devamındaki [örnekler](#examples) bölümüne bakın.
> 
> Ancak, [kılavuzda sağlanan filtreler](#grid-filters) toplanan liste için *geçerlidir*. Bu filtreler kılavuzun üst kısmındaki hızlı filtreyi ve her sütun başlığının filtresini içerir.

**Filtreler** bölmesinde bulunan filtre kümesini aşağıdaki adımları izleyerek değiştirebilirsiniz.

- Bir filtreyi bölmeden kaldırmak için **Kapat** düğmesini (**X**) seçin.
- Filtre eklemek için **Filtreler** bölmesinin en üstündeki **Ekle**'yi seçin. Beliren **Filtre ekleme alanları** iletişim kutusunda kullanılabilir alanların listesi gösterilir. Ayrıca, her bir alan için veri türü ve tablo ile ilgili bilgileri gösterir. Listeyi gerektiği gibi filtrelemek ve sıralamak için sütun başlıklarını kullanın ve sonra **Filtre** bölmesine eklemek istediğiniz her alanın onay kutusunu seçin. İşlemi bitirdiğinizde değişikliklerinizi uygulamak için **Ekle**'yi seçin.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Gösterilecek boyutları seçme

Boyutlar, eldeki stok listesindeki her kalem hakkında daha fazla bilgi verir ve listeyi sıralamak ve filtre uygulamak için size daha fazla yol sağlar. Göstermek için seçtiğiniz boyutlar, **Eldeki liste** sayfasında satırların nasıl toplanmakta olduğunu da etkiler. Bu toplama da gördüğünüz sonuçlarda kaynak tablolardaki satırların nasıl birleştirileceğini etkileyebilir. Bu davranışın sonuçlarınızı nasıl etkileyeceği hakkında bilgi için bu konunun devamındaki [örnekler](#examples) bölümüne bakın.

Gösterilen stok boyutlarının seçimini özelleştirmek için aşağıdaki adımları izleyin.

1. Eylem Bölmesinde **Boyutlar** öğesini seçin.

    Görünen **Boyut görünümü** iletişim kutusu her boyutu gösterir.

2. Kılavuza dahil etmek istediğiniz her boyut için onay kutusunu işaretleyin.
3. **Eldeki liste** sayfasını bir sonraki açışınızda seçiminizin varsayılan olarak kullanılmasını istiyorsanız, **Kurulumu kaydet** seçeneğini **Evet** olarak ayarlayın. Bu seçeneği **Hayır** olarak ayarlarsanız, seçiminiz yalnızca geçerli oturum sırasında kullanılacaktır. Bu nedenle, sayfayı bir sonraki açışınızda, geçerli varsayılan seçim kullanılacaktır.
4. Değişikliklerinizi uygulayıp iletişim kutusunu kapatmak için **Tamam**'ı seçin.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Eldeki stok listesi çıktısına filtre uygulama

İlgili sütundaki değerlere göre sıralama veya filtreleme için **Eldeki** kılavuzunda dilediğiniz sütun başlığı seçebilirsiniz. Kılavuzun üst kısmındaki hızlı filtre ek filtre uygulama seçenekleri sağlar. Bu filtreler kaynak tablolar değil, sonuçlar için geçerlidir. Bu davranışın sonuçlarınızı nasıl etkileyeceği hakkında bilgi için bu konunun devamındaki [örnekler](#examples) bölümüne bakın.

> [!NOTE]
> Tüm sütunlara göre filtre veya sıralama yapamazsınız. Hesaplanmış alanlar olduklarından, miktar sütunlarının çoğu sıralama ve filtreleme denetimlerini içermez. **Siparişte** sütunu bir özel durumdur.

## <a name="examples"></a><a name="examples"></a>Örnekler

Sisteminiz, aşağıdaki eldeki stoku gösteren ayrıntılı (toplanmayan) bir stok tablosu içerir.

| Kalem Numarası | Tesis | Ambar | Fiziksel Stok | Kullanılabilir Fiziksel Miktar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Senaryo 1

**Eldeki liste** sayfası, aşağıdaki son boyutları gösterecek şekilde ayarlanır:

- Madde kodu
- Tesis
- Ambar

**Filtreler** bölmesinde aşağıdaki filtre ölçütleri ayarlanır:

- **Kalem Numarası** \| **tam olarak** \| _IA0001_
- **Kullanılabilir Fiziksel Miktar** \| **küçüktür veya eşittir** \| _1_

Elde edilen çıktı aşağıdaki gibidir.

| Kalem Numarası | Tesis | Ambar | Fiziksel Stok | Kullanılabilir Fiziksel Miktar |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Senaryo 2

**Eldeki liste** sayfası, aşağıdaki son boyutları gösterecek şekilde ayarlanır:

- Madde kodu
- Tesis

**Filtreler** bölmesinde aşağıdaki filtre ölçütleri ayarlanır:

- **Kalem Numarası** \| **tam olarak** \| _IA0001_
- **Kullanılabilir Fiziksel Miktar** \| **küçüktür veya eşittir** \| _1_

Elde edilen çıktı aşağıdaki gibidir.

| Kalem Numarası | Tesis | Fiziksel Stok | Kullanılabilir Fiziksel Miktar |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

**Filtreler** bölmesindeki ayarların, bu bölümün başlangıcında gösterilen ayrıntılı (toplanmayan) stok tablosuna uygulanacağını unutmayın. Bu nedenle, **Kullanılabilir Fiziksel Miktar** \| **küçüktür veya eşittir** \| _1_ ölçütü o tablodan iki satır bulur (her biri _1_ **Kullanılabilir Fiziksel Miktar** değerini gösterir). Ancak bu senaryoda, **Eldeki liste** sayfası **Ambar** boyutunu gösterecek şekilde ayarlanmamıştır. Bu nedenle, her iki satırda da gösterilen tüm boyutlarda aynı değerler olduğu için iki özgün satırı tek bir sonuç satırına toplar. **Kullanılabilir Fiziksel Miktar** değeri _2_ olarak gösterildiğinden, bu satır filtre ölçütünü ihlal ediyor gibi görünür. Ancak, **Filtreler** bölmesindeki ayarlar, **Eldeki liste** sayfasında gösterilen toplanmış tabloya değil, kaynak tabloya uygulandığı için sonuç doğrudur.
