---
title: Satınalma ticari sözleşmeleri ile master planlama
description: Bu konuda, planlama Iyileştirmenin planlı bir sipariş için satıcı ve/veya sağlama süresini, satınalma ticari anlaşmalarında bulunan en iyi fiyat veya sağlama süresine göre nasıl bulabileceği açıklanmaktadır.
author: t-benebo
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: cb790836042506ed6676ee7edbd8bba58191519b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468427"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Satınalma ticari sözleşmeleri ile master planlama

[!include [banner](../../includes/banner.md)]

Bu konuda, planlama iyileştirmenin planlı bir sipariş için satıcı ve/veya sağlama süresini, belirli bir ürün için belirtilen tüm satınalma ticari anlaşmalarında bulunan en iyi fiyat veya sağlama süresine göre nasıl bulabileceği açıklanmaktadır.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Planlama için iyileştirme özelliği için satınalma ticari anlaşmalarını açın

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Master planlama*
- **Özellik adı:** *Planlama için iyileştirme için satınalma ticari anlaşmalarını açın*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Sisteminizi Master planlama sırasında satınalma ticari anlaşmalarını değerlendirmek için hazırlayın

Sisteminizi, satınalma ticari anlaşmalarını değerlendiren planlama en Iyileştirmesi uygulayacak şekilde konfigüre etmek için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin. **Planlanan siparişler** sekmesinde, **satıcı** bölümünde aşağıdaki değerleri ayarlayın:

    - **Ticari sözleşmeyi bul** – master planlamaya satınalma ticari sözleşmeleri dahil etmek için bu seçeneği **Evet** olarak ayarlayın.
    - **Arama ölçütü** – her bir satınalma ticari sözleşmesi için öncelik ayarlamak istediğiniz faktörü seçin: **Minimum sağlama süresi** veya **En düşük birim fiyatı**.

1. **Tedarik ve kaynak \>Kurulum \> fiyatları ve iskontolar \> fiyatı/iskontoyu etkinleştir**'e gidin ve **satıcı** seçeneğinin **Evet** olarak ayarlandığından emin olun.
1. **Ürün bilgileri yönetimi \> Kurulum \>boyutuna ve çeşit gruplarına \> depolama boyutu gruplarına** gidin ve Master planlamanın satınalma ticari anlaşmalarını değerlendirmesi gereken ürünler için bir depolama boyutu grubu seçin. Bu gruptaki ilgili depolama boyutunun, **Satınalma Fiyatları** sütunu için onay işareti olduğundan emin olun. İlgili tüm diğer depolama boyutları grupları için bu adımı yineleyin.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Kullanıma sunulan ürün Master planlama sırasında satınalma ticari anlaşmalarını değerlendirmek için hazırlayın

Sisteminiz önceki bölümde anlatıldığı şekilde hazırlandıktan sonra, bu özellikle kullanmak istediğiniz her ürünün doğru ayarlandığından emin olmak için aşağıdaki adımları izlemeniz gerekir.

1. **Ürün bilgileri yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin ve bir hedef ürün açın.
1. **Satınalma** hızlı sekmesinde, **satıcı** alanında hiçbir satıcı atanmadığını doğrulayın.
1. Seçili üün için Eylem Bölmesi'nde, **Plan** sekmesinde, **Kapsam** grubunda **Madde kapsamı**'nı seçerek **Madde kapsamı** sayfasını açın. Şu ayarları doğrulayın:

    - **Genel** sekmesinde, satıcı geçersiz kılma işlemleri ayarlayabilirsiniz. Planlama Iyileştirmenin bir satıcıyı seçmek için satınalma ticari sözleşmeleri kullanmasını istiyorsanız, **belirli ayarı kullan** onay kutusunu temizleyerek satıcı geçersiz kılmalarını önlersiniz .
    - **Sağlama süresi** sekmesinde, ön süre geçersiz kılmaları ayarlayabilirsiniz. Planlama Iyileştirmenin, sağlama sürelerini seçmek amacıyla satınalma ticari sözleşmeleri kullanmasını istiyorsanız, ön zaman geçersiz kılmalarını önlersiniz. Satınalma ticari sözleşmeleri (**Satınalma**, **Üretim** ve/veya **Transfer**) kullanarak seçmek istediğiniz her bir sağlama süresi türünün onay kutusunu temizleyin.

1. Seçili ürünün ayrıntılar sayfasına dönmek için **madde kapsamı** sayfasını kapatın.
1. Eylem bölmesinde, **plan** sekmesinde, **tahmin** grubunda, **tedarik tahmin** sayfasını açmak için **tedarik tahmini** seçeneğini belirleyin . Burada gösterilen herhangi bir satırın **satıcı hesabı** sütununda bir değere sahip olmadığından emin olun .
1. Seçili ürünün ayrıntılar sayfasına dönmek için **tedarik tahmini** sayfasını kapatın.
1. Eylem Bölmesinde **Satın alma** sekmesinde **Ticare anlaşmaları** grubunda **Ticare anlaşmalarını görüntüle** öğesini seçin. İlgili tüm satınalma ticari anlaşmalarının listelendiğinden emin olun. Ayrıca, planlama iyileştirmenin o anlaşma için belirtilen sağlama süresini kullanmasını istediğiniz her anlaşma için, **sağlama süresini göz ardı et** seçeneğinin **Hayır** olarak ayarlandığından emin olun.
1. Seçili üün için Eylem Bölmesi'nde, **Plan** sekmesinde, **Sipariş ayarları** grubunda **Varsayılan sipariş ayarları**'nı seçerek **Varsayılan sipariş ayarları** sayfasını açın. **Satınalma siparişi** hızlı sekmesinde, **Satınalma sağlama süresi** alanının değerini görüntüleyin . Madde karşılama müşteri adayı zaman geçersiz kılma tanımlanmazsa, planlama Iyileştirme, **sağlama süresini gözardı et** seçeneği **Evet** olarak ayarlanmış olan ticari sözleşmeleri seçtiğinde bu değeri kullanır . Bu nedenle, bu değeri gereksinim duyduğunuz şekilde ayarlamanız gerekir.
1. Her bir ilgili ürün için bu yordamı yineleyin.

> [!NOTE]
> Planlama Optimizasyonu, ticari anlaşmaları için birden fazla para birimli satın alımları destekler. **En düşük birim fiyatı** seçeneğini kullanarak bir ticari sözleşme ararken, sistem, ticari anlaşma satırları para birimi ile yasal varlığın muhasebe para birimi arasında bir döviz kuru tanımlandığında, farklı para birimlerine sahip ticari sözleşme satırlarını dikkate alır. Aksi durumda, ticari anlaşma satırı yok sayılır ve master planlama sırasında hata görürsünüz. Bu nedenle, master planlama fiyatların muhasebe para birimine dönüştürülebileceği tüm ilgili satınalma ticari sözleşme satırlarından bilgileri içerir. Ticari anlaşma satırı fiyat dönüştürmesi sırasında yuvarlama kurallarının dikkate alınmayacağını hatırlatmak isteriz.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Nasıl En Iyi duruma getirme planlanmasına ilişkin örnekler satıcı ve sağlama sürelerini bulur

Aşağıdaki tablo, yayınlanmış bir ürün ve ilişkili satınalma ticari anlaşmalarının çeşitli ayarlarının, sonuçta elde edilen planlı satınalma siparişi için bulunan değerleri nasıl etkilediğini gösteren örnekler içerir. En sağdaki iki sütundaki **kalın** değerler, planlama eniyileme ile seçilen değerlerdir. Diğer sütunlardaki **_kalın ve italik_** değerler, her satır için sonuç değerlerini üreten ayarlardır.

| Serbest bırakılan: Satıcı | Varsayılan sipariş ayarları: Sağlama süresi | Madde karşılama: satıcıyı geçersiz kıl | Madde karşılama: sağlama süresini geçersiz kıl | Ticari sözleşme: Satıcı | Ticari sözleşme: sağlama süresi | Ticari sözleşme: sağlama süresini göz ardı et | Sonuçta elde edilen satıcı | Sonuçta elde edilen sağlama süresi |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Hayır | Hayır | US003 | 3 | Hayır | **US001** | **1** |
| US001 | 1 | ***Evet: US002** _ | _*_Evet: 2_*_ | US003 | 3 | Hayır | **US002** | **2** |
| *(Boş)* | 1 | Hayır | Hayır | ***US003** _ | _*_3_*_ | Hayır | **US003** | **3** |
| *(Boş)* | ***1** _ | Hayır | Hayır | _*_US003_*_ | 3 | Evet | **US003** | **1** |
| *(Boş)* | ***1** _ | _*_Evet: US002_*_ | Hayır | US003 | 3 | Hayır | **US002** | **1** |
| *(Boş)* | ***1** _ | _*_Evet: US002_*_ | Hayır | US003 | 3 | Hayır | **US002** | **1** |
| *(Boş)* | 1 | Hayır | Evet: 2 | ***US003** _ | _*_3_*_ | Hayır | **US003** | **3** |
| *(Boş)* | 1 | Hayır | ***Evet: 2** _ | _*_US003_*_ | 3 | Evet | **US003** | **2** |

## <a name="additional-resources"></a>Ek kaynaklar

[Satın alma sözleşmeleri](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
