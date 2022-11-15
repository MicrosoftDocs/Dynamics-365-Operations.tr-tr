---
title: Satın alma ticari sözleşmeleri ile master planlama
description: Bu makalede, master planlamanın planlı bir sipariş için satıcı ve/veya sağlama süresini, satın alma ticari sözleşmelerinde bulunan en iyi fiyat veya sağlama süresine göre nasıl bulabileceği açıklanmaktadır.
author: t-benebo
ms.date: 08/09/2022
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
ms.openlocfilehash: c36827738b13d5ca71da910d32e8877c1a408f62
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740998"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Satın alma ticari sözleşmeleri ile master planlama

[!include [banner](../../includes/banner.md)]

Bu makalede, master planlamanın planlı bir sipariş için satıcı ve/veya sağlama süresini, belirli bir ürün için belirtilen tüm satın alma ticari sözleşmelerinde bulunan en iyi fiyat veya sağlama süresine göre nasıl bulabileceği açıklanmaktadır.

## <a name="turn-the-purchase-trade-agreements-for-planning-optimization-feature-on-or-off"></a>Planlamayı En İyi Duruma Getirme özelliği için Satınalma ticari sözleşmelerini açma veya kapatma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Planlamayı En İyi Duruma Getirme için satınalma ticari sözleşmeleri* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Sisteminizi Master planlama sırasında satınalma ticari sözleşmelerini değerlendirmek için hazırlayın

Sisteminizi, satın alma ticari sözleşmelerini değerlendiren master planlama uygulayacak şekilde yapılandırmak için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin. **Planlanan siparişler** sekmesinde, **satıcı** bölümünde aşağıdaki değerleri ayarlayın:

    - **Ticari sözleşmeyi bul** – master planlamaya satınalma ticari sözleşmeleri dahil etmek için bu seçeneği **Evet** olarak ayarlayın.
    - **Arama ölçütü** – her bir satınalma ticari sözleşmesi için öncelik ayarlamak istediğiniz faktörü seçin: **Minimum sağlama süresi** veya **En düşük birim fiyatı**.

1. **Tedarik ve kaynak \>Kurulum \> fiyatları ve iskontolar \> fiyatı/iskontoyu etkinleştir**'e gidin ve **satıcı** seçeneğinin **Evet** olarak ayarlandığından emin olun.
1. **Ürün bilgileri yönetimi \> Kurulum \>boyutuna ve çeşit gruplarına \> depolama boyutu gruplarına** gidin ve Master planlamanın satınalma ticari sözleşmelerini değerlendirmesi gereken ürünler için bir depolama boyutu grubu seçin. Bu gruptaki ilgili depolama boyutunun, **Satınalma Fiyatları** sütunu için onay işareti olduğundan emin olun. İlgili tüm diğer depolama boyutları grupları için bu adımı yineleyin.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Kullanıma sunulan ürün Master planlama sırasında satınalma ticari sözleşmelerini değerlendirmek için hazırlayın

Sisteminiz önceki bölümde anlatıldığı şekilde hazırlandıktan sonra, bu özellikle kullanmak istediğiniz her ürünün doğru ayarlandığından emin olmak için aşağıdaki adımları izlemeniz gerekir.

1. **Ürün bilgileri yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin ve bir hedef ürün açın.
1. **Satınalma** hızlı sekmesinde, **satıcı** alanında hiçbir satıcı atanmadığını doğrulayın.
1. Seçili üün için Eylem Bölmesi'nde, **Plan** sekmesinde, **Kapsam** grubunda **Madde kapsamı**'nı seçerek **Madde kapsamı** sayfasını açın. Şu ayarları doğrulayın:

    - **Genel** sekmesinde, satıcı geçersiz kılma işlemleri ayarlayabilirsiniz. Master planlamanın bir satıcıyı seçmek için satın alma ticari sözleşmeleri kullanmasını istiyorsanız **belirli ayarı kullan** onay kutusunu temizleyerek satıcı geçersiz kılmalarını önlemeniz gerekir.
    - **Sağlama süresi** sekmesinde, ön süre geçersiz kılmaları ayarlayabilirsiniz. Master planlamanın, sağlama sürelerini seçmek amacıyla satın alma ticari sözleşmeleri kullanmasını istiyorsanız sağlama süresi geçersiz kılmalarını önlemeniz gerekir. Satınalma ticari sözleşmeleri (**Satınalma**, **Üretim** ve/veya **Transfer**) kullanarak seçmek istediğiniz her bir sağlama süresi türünün onay kutusunu temizleyin.

1. Seçili ürünün ayrıntılar sayfasına dönmek için **madde kapsamı** sayfasını kapatın.
1. Eylem bölmesinde, **plan** sekmesinde, **tahmin** grubunda, **tedarik tahmin** sayfasını açmak için **tedarik tahmini** seçeneğini belirleyin . Burada gösterilen herhangi bir satırın **satıcı hesabı** sütununda bir değere sahip olmadığından emin olun .
1. Seçili ürünün ayrıntılar sayfasına dönmek için **tedarik tahmini** sayfasını kapatın.
1. Eylem Bölmesinde **Satın alma** sekmesinde **Ticare anlaşmaları** grubunda **Ticare anlaşmalarını görüntüle** öğesini seçin. İlgili tüm satınalma ticari sözleşmelerinin listelendiğinden emin olun. Ayrıca master planlamanın ilgili anlaşma için belirtilen sağlama süresini kullanmasını istediğiniz her anlaşma için, **sağlama süresini göz ardı et** seçeneğinin **Hayır** olarak ayarlandığından emin olun.
1. Seçili üün için Eylem Bölmesi'nde, **Plan** sekmesinde, **Sipariş ayarları** grubunda **Varsayılan sipariş ayarları**'nı seçerek **Varsayılan sipariş ayarları** sayfasını açın. **Satınalma siparişi** hızlı sekmesinde, **Satınalma sağlama süresi** alanının değerini görüntüleyin . Madde karşılama müşteri adayı sağlama süresi geçersiz kılma işlemi tanımlanmazsa master planlama, **Sağlama süresini göz ardı et** seçeneği **Evet** olarak ayarlanmış olan ticari sözleşmeleri seçtiğinde bu değeri kullanır. Bu nedenle, bu değeri gereksinim duyduğunuz şekilde ayarlamanız gerekir.
1. Her bir ilgili ürün için bu yordamı yineleyin.

> [!NOTE]
> Master planlama, ticari sözleşmeleri için birden fazla para birimli satın alımları destekler. **En düşük birim fiyatı** seçeneğini kullanarak bir ticari sözleşme ararken, sistem, ticari sözleşme satırları para birimi ile yasal varlığın muhasebe para birimi arasında bir döviz kuru tanımlandığında, farklı para birimlerine sahip ticari sözleşme satırlarını dikkate alır. Aksi durumda, ticari sözleşme satırı yok sayılır ve master planlama sırasında hata görürsünüz. Bu nedenle, master planlama fiyatların muhasebe para birimine dönüştürülebileceği tüm ilgili satınalma ticari sözleşme satırlarından bilgileri içerir. Ticari sözleşme satırı fiyat dönüştürmesi sırasında yuvarlama kurallarının dikkate alınmayacağını hatırlatmak isteriz.

## <a name="examples-of-how-master-planning-finds-vendor-and-lead-times"></a>Master planlamanın satıcı ve teslim sürelerini nasıl bulduğuyla ilgili örnekler

Aşağıdaki tablo, yayınlanmış bir ürün ve ilişkili satınalma ticari sözleşmelerinin çeşitli ayarlarının, sonuçta elde edilen planlı satınalma siparişi için bulunan değerleri nasıl etkilediğini gösteren örnekler içerir. En sağdaki iki sütundaki **kalın** değerler, master planlama ile seçilen değerlerdir. Diğer sütunlardaki **_kalın ve italik_** değerler, her satır için sonuç değerlerini üreten ayarlardır.

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

- [Satın alma sözleşmeleri](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
