---
title: Dalga işlemeyi yapılandırma örneği
description: Bu başlık bir dalga işlendiğinde bir ambar için hangi işin oluşturulacağını belirlemek için ölçütleri ayarlamayı ve dalgaların manuel mi yoksa otomatik olarak mı işlemden geçirileceğini açıklayan bir örnek sunar.
author: Mirzaab
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSParameters, ProdParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10277c22f5988797dd55a33ef5151d2bc7a4b0be
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831062"
---
# <a name="configure-wave-processing-example"></a>Dalga işlemeyi yapılandırma örneği

[!include [banner](../../includes/banner.md)]

Bu başlık bir dalga işlendiğinde bir ambar için hangi işin oluşturulacağını belirlemek için ölçütleri ayarlamayı ve dalgaların manuel mi yoksa otomatik olarak mı işlemden geçirileceğini açıklayan bir örnek sunar. Ölçütleri, bir dalgayı yayımlanan satış siparişleri, üretim emirleri veya kanban siparişleri ile eşleştiren dalga şablonları ve sorguları oluşturarak belirtebilirsiniz.

## <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart tanıtım verilerinin yüklenmiş olduğu bir sistem kullanmanız gerekir. Ayrıca başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

## <a name="example-scenario-configure-wave-processing"></a>Örnek senaryo: Dalga işlemeyi yapılandırma

Bu örnek senaryo, dalgaların oluşturulma, doldurulma, işlenme ve serbest bırakılma şeklini etkileyen çeşitli ayarların çoğunu açıklar.

1. **Gezinti bölmesi > Modüller > Ambar yönetimi > Kurulum > Dalgalar > Dalga şablonları**'na gidin.
1. **Yeni**'yi seçin.
1. **Dalga şablonu adı** alanına bir değer girin. Bir dalga şablonu oluştururken, şablonların hangi sırada eşleneceğini ve satış siparişlerine, üretim emirlerine veya kanbanlara yayınlanacağını belirtirsiniz. Bir satır ambar veya üretim için serbest bırakıldığında ölçütlerini karşılayan ilk dalga şablonunu kullanır. Listenin üstündeki en belirgin ölçütlerle sahip şablonları koymanızı öneririz. Ölçüt ne kadar geniş olursa, bir satırın ölçüte uyması o kadar yüksek olasılığa sahip olur ve bu da satırların yanlış dalgaya atanmasına sebep olabilir.  
1. **Dalga şablonu açıklaması** alanında bir değer girin.
1. **Tesis** alanına bir değer girin veya buradan bir değer seçin. USMF kullanıyorsanız, site 2'yi seçebilirsiniz.  
1. **Ambar** alanında bir değer girin veya bir değer seçin. USMF kullanıyorsanız, ambar 24'ü seçebilirsiniz.  
1. **Otomatik dalga oluşturma** alanını **Evet** olarak ayarlayın. Bir satış emri, üretim emri veya kanban serbest bırakıldığında otomatik olarak dalga oluşturmak için bu seçeneği belirleyin.  
1. **Dalga yayın ambar işleme** seçeneğini **Evet** olarak ayarlayın. Satır ambara serbest bırakıldığında otomatik olarak dalgayı işlemek ve iş oluşturmak için bu seçeneği belirleyin.  
1. **Otomatik dalga yayımlama seçeneği**'ni **Evet** olarak ayarlayın. Dalgayı otomatik olarak serbest bırakmak için bu seçeneği belirleyin. Malzeme çekme işi oluşturulur ve mobil cihazlarda kullanılabilir.  
1. **Açık dalgalara ata seçeneği**'ni **Evet** olarak ayarlayın. Satırlar, dalgalara, dalga şablonu için sorgu filtresi temel alınarak atanır.  
1. **Dalgayı eşikte otomatik işle seçeneği**'ni **Evet** olarak ayarlayın. Dalganın değerleri **Dalga eşikleri** alan grubunda belirtilen ağırlık, sevkıyat ve satır eşiklerine eriştiğinde dalgayı otomatik olarak işlemek için bu seçeneği seçin. Bu seçenek yalnızca, **Dalga şablon türü** alanında **Sevkiyat** seçilirse kullanılabilir.  
1. **Otomatik stok yenileme işi yayımla seçeneği**'ni **Evet** olarak ayarlayın. Talep tabanlı stok yenileme işi oluşturmak ve bunu otomatik olarak serbest bırakmak için bu seçeneği belirleyin. Stok yenileme dalga yöntemini dalga şablonuna eklemeniz **Dalga talebi** türünü kullanarak stok yenileme şablonu oluşturmanız gerekir.  
1. Dalga niteliklerini atamak için dosyalanan **varsayılan değerler** grubundaki ayarları kullanın. Dalga öznitelikleri, dalgayı kullanabilecek öğelerin türünü sınırlamak için filtreler olarak çalışır. Örneğin, bir madde grubu belirtebilirsiniz.  
1. **Yöntemler** bölümünü genişletin ve dalga şablonu tarafından gerçekleştirilen eylemleri ayarlayın. Dalga şablonu yöntemleri, her bir dalganın işlendiğinde geçirileceği etkinlikler dizisini denetlemenize olanak sağlar. Örneğin, dalga stok yenilemesi için bir yönteme sahip olabilirsiniz. Bir yöntem eklediğinizde, adımlar sırasında otomatik olarak uygun konumda listelenir. **Otomatik stok yenileme işi yayını** seçeneğini **Evet** olarak ayarladıysanız, yenileme yöntemini buraya eklemeniz gerekir.  
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.
1. **Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri** öğesine gidin.
1. **Dalga işleme** bölümünü genişletin.
1. **Dalga işleme toplu iş grubu** alanında bir değer girin veya seçin.
1. **Dalgaları toplu iş olarak işle seçeneği**'ni **Evet** olarak ayarlayın.
1. **Kilit için bekle (ms)** alanında, bir sayı girin. Tahsisat adımının, başka bir tahsisat kaynağı tarafından kilitlenmiş olan bir sistem kaynağı için bekleyeceği zamanı, milisaniye cinsinden girin. Bu süre aşıldığında, dalga işlenmez ve bir hata iletisi görüntülenir.  
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.
1. **Gezinti bölmesi > Modüller > Üretim kontrol > Kurulum > Üretim kontrol parametreleri**'ne gidin.
1. **Ambara yayınla** alanında, bir seçenek belirleyin.

    Satış siparişleri ve kanban siparişleri için, sipariş için ambarda serbest bırakılmadan önce stok ayrılmalıdır. Aksi halde, maddeler veya tahsisat satırları dalga içerisinde işlenemez. Üretim emirleri için **Kısmi rezervasyona izin ver**'i seçme seçeneğiniz de vardır. Örneğin, üretimi başlatmak için gereken malzemeler varsa ve işlemin bitirilmesi için ek malzemelerin kullanılabilir olmasını bekleyebiliyorsanız. Bu seçeneği belirlerseniz, ek malzemeler kullanılabilir duruma geldiğinde, ambara serbest bırak işlemini el ile tekrar etmeniz gerekir.
1. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Dalga oluşturma ve işleme](../wave-processing.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
