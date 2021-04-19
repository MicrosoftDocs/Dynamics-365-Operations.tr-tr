---
title: Ürün yaşam döngüsü durumuna genel bakış
description: Ürün yaşam döngüsü durumu, serbest bırakılan bir ürünün veya ürün çeşidinin yaşam döngüsü durumunu belgeler.
author: cvocph
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 1def67750fe6328087fe6bf7eeb22105232390fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820214"
---
# <a name="product-lifecycle-state-overview"></a>Ürün yaşam döngüsü durumuna genel bakış

[!include [banner](../includes/banner.md)]

Ürün yaşam döngüsü durumu, serbest bırakılan bir ürünün veya ürün çeşidinin yaşam döngüsü durumunu belgeler. Ürün yaşam döngüsü durumları genellikle bir ürün yöneticisi veya ürün ana verileri yöneticisi olan bir kullanıcı tarafından tanımlanır. Master planlama gibi belirli iş süreçleri belirli bir yaşam döngüsü durumu tarafından etkilenebilir.

Serbest bırakılan ürün veya ürün çeşidi, belirli bir ürün veya ürün çeşidi yaşam döngüsü durumunun içinde bulunduğunu belgeleyen bir ürün yaşam döngüsü durumu ile ilişkilendirilebilir. Bir durum adı ve açıklaması atayarak istediğiniz sayıda ürün yaşam döngüsü durumu tanımlayabilirsiniz. Yeni serbest bırakılan ürünler için varsayılan durum olarak bir yaşam döngüsü durumu seçebilirsiniz. Serbest bırakılan ürün çeşitleri, ürün yaşam döngüsü durumlarını oluşturma sırasındaki serbest bırakılan ana üründen alır. Serbest bırakılan bir ana üründe yaşam döngüsü durumunu değiştirirken, aynı orijinal duruma sahip mevcut tüm ürün çeşitlerini güncelleştirmeyi seçebilirsiniz.  

## <a name="create-a-new-product-lifecycle-state"></a>Yeni ürün yaşam döngüsü durumu oluşturma

- Yeni bir ürün yaşam döngüsü durumu oluşturmak için [Yeni ürün yaşam döngüsü durumu oluşturma](tasks/new-product-lifecycle-state.md) konusuna bakın.

- Varsayılan ürün yaşam döngüsü durumu oluşturmak için [Varsayılan ürün yaşam döngüsü durumu oluşturma](tasks/default-product-lifecycle-state.md) konusuna bakın.

## <a name="associate-product-lifecycle-states-to-released-products"></a>Ürün yaşam döngüsü durumlarını serbest bırakılan ürünlerle ilişkilendirme  

Bir ürün yaşam döngüsü durumunu serbest bırakılan ürün veya ürün çeşitleriyle ilişkilendirmenin birden çok yolu vardır.

- Yeni serbest bırakılan bir ürün oluşturma sırasında varsayılan **Ürün yaşam döngüsü durumu** otomatik olarak atanır.
- Bir ürün bir tüzel kişiliğe serbest bırakıldığında varsayılan **Ürün yaşam döngüsü durumu** otomatik olarak atanır.
- Bir ürün çeşidi bir tüzel kişilik için serbest bırakıldığında, bu tüzel kişilikte serbest bırakılan ana ürünle ilişkili **Ürün yaşam döngüsü durumu** otomatik olarak yeni ürün çeşidine atanır.

Ürün yaşam döngüsü durumunu aşağıdakileri kullanarak el ile güncelleştirebilirsiniz:

- **Serbest bırakılan ürünler** liste sayfası veya **Ayrıntılar görünümü**.
- **Serbest bırakılan ürün çeşitleri** liste sayfası veya **Ayrıntılar görünümü**.
- Eski ürünleri veya ürün çeşitlerini talebe göre bulun ve bir yaşam döngüsü durumuyla ilişkilendirin.  

Daha fazla bilgi için:

- Bir ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürünle ilişkilendirmek için [Serbest bırakılan ana ürüne bir ürün yaşam döngüsü durumu atama](tasks/product-lifecycle-state-released-product-master.md) konusuna bakın.

- Bir ürün yaşam döngüsü durumunu serbest bırakılan bir ürünle ilişkilendirmek için [Serbest bırakılan ürüne bir ürün yaşam döngüsü durumu atama](tasks/product-lifecycle-state-released-product.md) konusuna bakın.

## <a name="impact-on-master-planning"></a>Master planlama üzerindeki etkisi

Ürün yaşam döngüsü durumunun yalnızca bir denetim bayrağı bulunur: **Planlama için etkin**. Varsayılan olarak, oluşturulan tüm ürün yaşam döngüsü durumları için **Evet** olarak ayarlanır ancak **Hayır** olarak değiştirilebilir. **Hayır** olarak ayarlandığında, ilişkilendirilmiş serbest bırakılan ürünler veya serbest bırakılan ürün çeşitleri için aşağıdakiler geçerli olur:

- Master planlamada hariç tutulur.
- Ürün reçetesi düzeyinde hesaplamadan hariç tutulur.

Ürünleri master planlama ve ürün reçetesi düzeyinde hesaplama dışında tutmak amacıyla ürün yaşam döngüsü durumunun nasıl kullanılacağı hakkında daha fazla bilgi edinmek için [Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma](tasks/exclude-products-master-planning.md) konusuna bakın.

> [!NOTE]
> Performansı iyileştirmek amacıyla, tüm eski serbest bırakılan ürünlerin ve ürün çeşitlerinin, özellikle de yeniden kullanılmayan ürün yapılandırma çeşitleriyle çalışılırken, master planlama için devre dışı bırakılmış bir ürün yaşam döngüsü durumuyla ilişkilendirilmesi önerilir.  

## <a name="default-migration-import-and-export"></a>Varsayılan geçiş, içe aktarma ve dışa aktarma

Ürün yaşam döngüsü durumları veri varlıkları tarafından desteklenmez ve yaşam döngüsü durumu serbest bırakılan ürün veri varlığı ya da yayınlanan değişken veri varlığı aracılığıyla değişken bir duruma ayarlanamaz.

## <a name="find-obsolete-products-and-products-variants"></a>Eski ürünleri ve ürün çeşitlerini bulma

Eski ürünleri ve ürün çeşitlerini bulmak için bir benzerim analizi çalıştırabilir ve daha sonra ürün yaşam döngüsü durumlarını güncelleştirebilirsiniz. Eski ürünleri bulmak için [Eski ürün çeşitlerini bulma ve bir ürün yaşam döngüsü durumu atama](tasks/obsolete-product-variants.md) konusuna bakın. Bu konu, eski ürünleri veya ürün çeşitlerini nasıl bulabileceğinizi ve bir ürün yaşam döngüsü durumunu eski ürünlerle nasıl ilişkilendirebileceğinizi gösterir. Ayrıca, benzetim sonuçlarının nasıl görüntüleneceğini ve benzetim olmadan güncelleştirme çalıştırıldığında ne kadar ürün ve ürün çeşidinin yeni bir ürün yaşam döngüsü durumuyla ilişkilendirileceğinin nasıl değerlendirileceğini gösterir.  

Analiz benzetim modunda çalıştırıldığında, eski olarak tanımlanan ürünler ve ürün çeşitleri kolay bir şekilde gözden geçirilmelerini sağlayan özel bir formda görüntülenir. Analiz, değişken bir dönem içinde talep edilmemiş olan ve talep durumunda herhangi bir ana veriye ulaşılamayacak ürünleri tanımlamak için hareketleri ve belirli ana verileri arar. Değişken bir dönem içinde yeni serbest bırakılan ürünler bu analizin dışında bırakılabilir. Analiz benzetimi beklenen sonucu döndürdüğünde, kullanıcı analizi çalıştırabilir ve analiz tarafından eski olarak tanımlanan tüm ürünler için yeni bir ürün yaşam döngüsü durumu ayarlayabilir.  

> [!NOTE]
> Tüm analizlerin ve güncelleştirmelerin aynı tüzel kişilik içinde yapılması gerektiğini unutmayın.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Serbest bırakılan ürünleri veya ürün çeşitlerini seçme ve güncelleştirme ölçütü

Serbest bırakılan ürünleri ve ürün çeşitlerini seçmek ve güncelleştirmek için aşağıdaki ölçütü kullanın:

- Ürün veya ürün çeşidinin ürün yaşam döngüsü durumu istenen yeni durumdan farklı olmalıdır.
- Seçim iletişim kutusuna girdiğiniz gün sayısına bağlı olarak ürün veya ürün çeşidi belirli bir günden önce oluşturulmuş olmalıdır.
- Ürün veya ürün çeşidi için açık üretim emirleri (=durum < bitti) olmamalıdır.
- Ürün veya ürün çeşidi için açık stok hareketleri olmamalıdır (= durum çıkış ReservPhysical - QuotationIssue veya durum giriş Registrered - QuotationReceipt).
- Ürün veya ürün çeşidi için son gün sayısı içinde herhangi bir stok hareketi olmamalıdır.
- Ürün veya ürün çeşidi için geleceğe yönelik bir talep veya tedarik tahmini bulunmamalıdır.  
- Ürün veya ürün çeşidi için madde karşılamada minimum stok düzeyi ayarlanmamış olmalıdır.
- Ürün veya ürün çeşidi için etkin sabit miktar kanban kuralı olmamalıdır.  
- Ürün veya ürün çeşidi için servis sipariş satırı olmamalıdır.
- Ürün veya ürün çeşidi için etkin veya geleceğe yönelik satış veya satınalma sözleşmesi satırları bulunmamalıdır.
- Ürün veya ürün çeşidi, planlama için etkin olan bir ürün veya ürün çeşidi için süresi sona ermemiş, onaylanmış ürün reçetesi sürümüyle ilişkilendirilmiş bir ürün reçetesinde kullanılmamalıdır.

## <a name="related-topics"></a>İlgili konular

- [Yeni ürün yaşam döngüsü durumu oluşturma](tasks/new-product-lifecycle-state.md)
- [Varsayılan ürün yaşam döngüsü durumu oluşturma](tasks/default-product-lifecycle-state.md)
- [Serbest bırakılan ana ürüne ürün yaşam döngüsü durumu atama](tasks/product-lifecycle-state-released-product-master.md)
- [Serbest bırakılan ürüne ürün yaşam döngüsü durumu atama](tasks/product-lifecycle-state-released-product.md)
- [Eski ürün çeşitlerini bulma ve bir ürün yaşam döngüsü durumu atama](tasks/obsolete-product-variants.md)
- [Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]