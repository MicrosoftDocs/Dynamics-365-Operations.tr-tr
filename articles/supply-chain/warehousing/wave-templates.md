---
title: Dalga şablonları
description: Bu konu bir dalga işlendiğinde bir ambar için hangi işin oluşturulacağını belirlemek için ölçütleri ayarlamayı ve dalgaların manuel mi yoksa otomatik olarak mı işlemden geçirileceğini açıklar.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a606f413bf3660a89270c0751b2656fab07cd80d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576004"
---
# <a name="wave-templates"></a>Dalga şablonları

[!include [banner](../includes/banner.md)]

Bu konu bir dalga işlendiğinde bir ambar için hangi işin oluşturulacağını belirlemek için ölçütleri ayarlamayı ve dalgaların manuel mi yoksa otomatik olarak mı işlemden geçirileceğini açıklar. Ölçütleri, bir dalgayı yayımlanan satış siparişleri, üretim emirleri ve kanbanlar ile eşleştiren dalga şablonları ve sorguları oluşturarak belirtebilirsiniz.

## <a name="settings-for-wave-templates"></a>Dalga şablonları ayarları

Bir dalga şablonu kurduğunuzda, aşağıdakileri belirtirsiniz:

- Şablonun iş oluşturacağı **tesis** ve **ambar**.
- Şablonların değerlendirileceği sipariş. Şablonların, satış siparişleri, üretim emirleri ve kanbanlar üzerindeki serbest bırakılmış satırlarla eşleştirildiği sıra. Bir satır serbest bırakıldığında, sistem satırın ölçütlerini karşılayan ilk dalga şablonunu uygular. Ölçütler ne kadar geniş ise, bir satırın ölçütleri karşılaması o kadar büyük olasılığa sahiptir, bu nedenle şablonları listenin en üstüne en belirgin olacak şekilde koymanız gerekir. Şablonları listede düzenlemek için Eylem Bölmesindeki **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanın.
- Her bir şablon tarafından gerçekleştirilen eylemler. Dalga **yöntemleri** şablon tarafından oluşturulan eylemleri (örneğin, her bir dalga şablonu türü için iş oluşturma veya dağıtma) gerçekleştirir.
- Kullanılacak Dalga şablonuna uygulanması gereken dalga öznitelikleri (filtreler).

> [!NOTE]
> Gerekirse, geliştirici ek yöntemler oluşturabilir. **Dalga işlem yöntemleri** sayfasında yöntemlerin tam listesini görebilirsiniz.

Bazı ayarlar, aşağıdaki gibi dalga işleme için stratejik kararları temsil eder:

- Şablon, satış siparişleri ve transfer emirleri için madde göndermek üzere veya üretim emirleri veya kanbanlar için maddeleri üretime taşımak amacıyla kullanılacaksa.
- Bir dalga el ile veya otomatik olarak işlenirse, aşağıdaki ayarlar kullanılır:

  - **El ile işleme**: Satır bir dalgaya eklenir ve stok rezerve edilir, ancak sipariş için malzeme çekme çalışması oluşturmak üzere **tüm dalgalar** liste sayfasında **işlem** seçeneğini seçmeniz gerekir.
  - **Otomatik işleme**: Dalga işlemeyi tamamen veya kısmen otomatikleştirebilirsiniz. Dalga işlemeyi tamamen otomatikleştirdiyseniz, bir satış siparişi, üretim emri veya Kanban oluşturulduğunda, satış siparişi, üretim emri veya Kanban satırını içeren bir dalga oluşturulur. Maddeler eldeki stoktan düşülür ve malzeme çekme işi oluşturulur. Dalga işlemeyi kısmen otomatikleştirdiyseniz dalga işlemeyi tetikleyecek değerleri belirtebilirsiniz. Örneğin, bir dalga alanındaki satırların toplam ağırlığı değere ulaştığında, dalga işlemeyi tetikleyecek sevkiyatlar için maksimum ağırlığı belirtebilirsiniz.

- Açık bir dalgaya sevkiyatlar atarsanız. Örneğin, müşterilere 12:00'a kadar verilen bir siparişin 24 saat içinde sevk edilecek olduğunu taahhüt ediyorsanız, dalga şablonunu açık bir dalgaya 12:00'a kadar otomatik olarak bir dalga satırları atayacak şekilde ayarlayabilirsiniz. Bu sırada, dalga otomatik olarak işlenir.

Bir dalga işlenirken, oluşturulan malzeme çekme işi iş şablonuna ve ambar için belirtilen yerleşim yönergesine dayanır. Çalışma şablonu, malzeme çekme çalışmasının nasıl oluşturulduğunu ve yerleşim yönergesi çekme ve yerine koyma yerlerini belirtir.

## <a name="create-a-wave-template"></a>Dalga şablonu oluşturma

Dalga şablonu ayarlamak için aşağıdaki adımları takip edin:

1. **Ambar yönetimi** \> **Kurulum** \> **Dalgalar** \> **Dalga şablonları**'na gidin.
1. Yeni dalga şablonu oluşturmak için **Yeni**'yi seçin.
1. **Dalga şablonu türü** alanında, aşağıdaki seçeneklerden birini seçin:

    - *Sevkiyat*: Satış siparişleri ve transfer emirleri için madde sevk etmek üzere dalga şablonunu kullanın.
    - *Üretim siparişleri*: Maddeleri üretim emirlerine taşımak için dalga şablonunu kullanın.
    - *Kanban*: Maddeleri Kanban emirlerine taşımak için dalga şablonunu kullanın.

1. **Dalga şablonu adı** ve **dalga şablonu Açıklaması** alanlarına, dalga şablonu için bir ad ve açıklama girin.

    > [!NOTE]
    > Bir ambar için birden fazla şablon oluşturulduysa **Dalga şablonu sırası** alanındaki sayı şablonun ölçütleri sağlandığında şablonların uygulandığı sıradaki şablonun konumunu gösterir. Şablonların sırasını yeniden düzenlemek için **yukarı taşı** veya **aşağı taşı** seçeneğini belirleyebilirsiniz.

1. **Tesis** ve **Ambar** alanlarında, dalga şablonunun dalgalar ve çalışma için malzeme çekme işi oluşturmasını istediğiniz tesisi ve ambarı seçin.
1. Dalga işlemeyi otomatikleştirmek istiyorsanız, gerekirse aşağıdaki ayarları yapın:

    - **Dalga oluşturmayı otomatikleştir**: Bir satış emri, üretim emri veya kanban ambara serbest bırakıldığında otomatik olarak dalga oluşturmak için bunu *Evet* olarak ayarlayın.
    - **Açık dalgalara ata**: Satırlar serbest bırakıldığında, açık bir dalgaya otomatik olarak satır atamak için bunu *Evet* olarak ayarlayın. Satırlar, dalgalara, dalga şablonu için sorgu filtresi temel alınarak atanır.
    - **Ambara serbest bırakıldında dalgayı işle**: Satırın ambara serbest bırakılmasıyla, dalgayı otomatik olarak işlemek ve iş oluşturmak için bunu *Evet* olarak ayarlayın.
    - **Eşikte dalgayı otomatik olarak işle**: Dalganın değerleri **Dalga eşikleri** alan grubunda belirtilen ağırlık, sevkiyat ve satır eşiklerine eriştiğinde dalgayı otomatik olarak işlemek için bu seçeneği *Evet* olarak ayarlayın. Bu ayar yalnızca, **Dalga şablon türü** alanında *Sevkiyat* seçilirse etkindir.
    - **Dalga serbest bırakmayı otomatikleştir**: Dalgayı otomatik olarak serbest bırakmak için bunu *Evet* olarak ayarlayın. Malzeme çekme işi oluşturulur ve mobil cihazlarda kullanılabilir.
    - **Stok yenileme işi serbest bırakmayı otomatik hale getir**: Talep tabanlı stok yenileme işi oluşturmak ve bunu otomatik olarak serbest bırakmak için bu seçeneği *Evet* olarak ayarlayın. Stok yenileme dalga yöntemini dalga şablonuna eklemeniz *Dalga talebi* türünü kullanarak stok yenileme şablonu oluşturmanız gerekir. **Stok yenileme şablonları** sayfasında bir stok yenileme şablonu ayarlayın. Bu, dalga şablonuna stok yenileme yöntemi eklemenizi gerektirir.
    - **İş oluşturma başarısız olduğunda dalga işlemeye devam et**: *Evet* olarak ayarlandığında sistem, yerleşim yönergesi tarafından önerilen yerleşimde stok rezerve edemiyorsa boş bir yerleşim kullanır (ör. stokun artık kullanılamaması durumunda). *Hayır* olarak ayarlandığında sistem stoku rezerve edemezse dalga başarısız olur.

1. **Dalga eşikleri** alan grubunu gerektiği gibi ayarlayın:
    - **Dalga ağırlığı eşiği**: Bir dalganın içerebileceği en yüksek ağırlığı girin.
    - **Sevkiyat eşiği**: Bir dalgaya dahil edilebilecek maksimum sevkiyat sayısını girin.
    - **Satır eşiği**: Bir dalgaya dahil edilebilecek maksimum satır sayısını girin.

1. **Varsayılan değerler** alan grubunda, dalga şablonu için ek ölçüt olarak kullanılacak dalga özniteliklerini seçin. Dalga nitelikleri, bir dalga şablonuna belirli bir müşteri adı gibi ek ölçütler atamak için yararlıdır. **Dalga Öznitelikleri** sayfasında bu öznitelikleri oluşturabilirsiniz. 

1. Bu şablonu kullanan dalgalar ile ilgili bildirimleri oluşturmak için, **dalga bildirim ilkesini** kullanmak istediğiniz ilkeye ayarlayın. Dalga bildirim ilkesi örneği için, bkz. [Dalga yürütme bildirimleri](wave-execution-notifications.md).

1. **Yöntemler** hızlı sekmesinde **Seçili yöntemler** bölmesi, seçili dalga şablonu için yöntemleri listeler. Dalga yöntemleri şablon tarafından oluşturulan eylemleri (örneğin, iş oluşturma veya dağıtma) gerçekleştirir. Bu eylemler, dalga adımları olarak da adlandırılır. Wave yöntemleri, her bir dalga şablonu türü için önceden tanımlanmıştır. Önceden tanımlanmış dalga yöntemlerini kaldıramazsınız, ancak yöntemlerin sırasını yeniden düzenleyebilir ve ek yöntemler ekleyebilirsiniz. Örneğin, sevkiyat için bir dalga şablonu oluşturuyorsanız, stok yenileme ve kapsayıcı hale getirme için yöntemler ekleyebilirsiniz. Dalga şablonunda işlenen satırların kapsayıcıya alınmasını tanımlamak için dalga yöntemleri dizisine dalga kapsayıcıya alma eklenebilir. Başka bir yöntem eklemek için, aşağıdakileri yapın:

    - **Kalan projeler** bölmesinde, bir yöntem seçin ve ardından **Seçilen yöntemler** bölmesine eklemek için **Sol** ok düğmesini seçin.
    - Sırayı değiştirmek için, bir yöntem seçin ve **yukarı** veya **aşağı** oku seçin.

    > [!NOTE]
    > Bir yöntem eklediğinizde, adımlar sırasında otomatik olarak uygun konumda listelenir.

1. Sorguyu serbest bırakılan satırları uygun bir dalgayla eşleştirecek şekilde ayarlamak için, Eylem bölmesinde **Sorguyu Düzenle**'yi seçin.
1. Dalga şablonu ayarlarının geçerli olduğunu doğrulamak için **şablonu doğrula**'yı seçin.
