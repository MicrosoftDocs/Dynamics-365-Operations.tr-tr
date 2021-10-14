---
title: Uygunsuzluk oluşturma ve işleme
description: Bu konu, uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi açıklar.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580876"
---
# <a name="create-and-process-nonconformances"></a>Uygunsuzluk oluşturma ve işleme

[!include [banner](../../includes/banner.md)]

Bu konu, uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi açıklar. Genel olarak, uygunsuzluk yönetimi bir kalite görevlisi tarafından gerçekleştirilir. Önkoşul olarak, kullanılabilir bir kalite emrinizin olması gerekir. (Kalite emri oluşturma hakkında bilgi edinmek için bkz. [ Malların kalitesini denetleme](inspect-quality-goods.md) .)

Bir kullanıcı uygunsuzluk onayını işlemeden önce  **Kullanıcılar** sayfasındaki **Kişi** alanında bir çalışanın atanması gerekir. Ek olarak, kullanıcının belge notlarını kullanabilmesi için önce **Belge işlemeyi etkinleştir** seçeneğinin kullanıcı seçeneklerinde *Evet* olarak ayarlanmış olması gerekir.

## <a name="create-a-nonconformance"></a>Uygunsuzluk oluşturma

Uygunsuzluk oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Eylem Bölmesi'nde **Yeni**'yi seçin.
1. **Uygunsuzluk oluştur** iletişim kutusunda, **Sorun türü** alanında, denetleme işlemi sırasında bulunan sorunun türünü seçin.
1. **Tamam**'ı seçin.

## <a name="approve-or-reject-a-nonconformance"></a>Bir uygunsuzluğu onaylama veya reddetme

Bir uygunsuzluğu onaylamak veya reddetmek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara düzeltme ekleyebilirsiniz.

1. Eylem Bölmesi'nde, uygunsuzluğu onaylamak için **İşlevler \> Uygunsuzluğu onayla**'yı seçin ya da reddetmek için **İşlevler \> Uygunsuzluğu reddet**'i seçin. Onaylanmış uygunsuzlukları [ilgili işlemlerle](../quality-operations.md) ilişkilendirebilirsiniz. Bu şekilde, uygunsuzluk işlemenin bir parçası olarak yapılan çalışmayı ve düzeltme işleme işlemini kaydedebilirsiniz.
1. Seçiminizi onaylamanız istenir. Devam etmek için **Eve**'i seçin.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Uygunsuzluklara işlemler ve diğer ayrıntılar ekleme

Uygunsuzluk oluşturduktan sonra, ilgili işlemler eklemeye başlayabilir ve bu işlemlerle ilgili ek bilgiler belirtebilirsiniz. Yalnızca onaylanan uygunsuzluklara ilgili işlemler ekleyebilirsiniz.

Temel bilgilerin yanı sıra, bir işleme aşağıdaki detayları da ekleyebilirsiniz:

- **Öğeler** - Düzeltmeyi gerçekleştirmek için tüketilen öğelerin listesini oluşturabilirsiniz. Örneğin, bu öğeler tamamlanmış bir ürünün yeniden çalıştırılması için gerekli olan ekipman veya malzemeleri onarmak için gerekli ürünler olabilir.
- **Kalite giderleri** – Harici kaynaklar için tahakkuk edilen veya faturalanan giderlerin listesini oluşturabilirsiniz.
- **Zaman çizelgesi** – Her çalışanın işlemde harcadığı zamanı içeren bir günlük oluşturabilirsiniz.

Kalan ayarlar isteğe bağlıdır. Her öğe, kalite ücreti ve zaman çizelgesinin maliyeti toplanır ve işlemde gösterilir. İşlemde **Maliyet** alanını doğrudan düzenleyemezsiniz.

### <a name="create-an-operation-for-a-nonconformance"></a>Uygunsuzluk için işlem oluşturma

Uygunsuzluk için bir işlem oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.

1. Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.
1. **İlgili işlemler** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **İşlem** – Uygunsuzlukta gerçekleştirilecek işlemin kodunu seçin.
    - **Neden** – İşlemin neden gerekli olduğunu anlatan ayrıntılı bir açıklama girin.
    - **Satış siparişi** – Seçilen işlem kodu satış siparişi türüyle ilişkiliyse işlemi bağladığınız satış siparişini seçin.
    - **Satınalma siparişi** – Seçilen işlem kodu satınalma siparişi türüyle ilişkiliyse işlemi bağladığınız satınalma siparişini seçin.

1. Sayfaları kapatın.

### <a name="add-items-to-an-operation"></a>İşleme öğe ekleme

Bir işleme öğeler eklemek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.

1. Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.
1. **İlgili işlemler** sayfasında, öğe eklemek istediğiniz işlemi seçin.
1. Eylem Bölmesinde, **Maddeler**'i seçin.
1. **İlgili işlemler** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Öğe numarası** – Seçilen işlemin parçası olarak tüketilecek ürünü seçin.
    - **Miktar** – Tüketilecek öğelerin sayısını girin.

    > [!NOTE]
    > Öğenin maliyetini **Genel** sekmesindeki **Maliyet** alanında görüntüleyebilirsiniz . Gösterilen maliyet, **Serbest bırakılan ürün** sayfasında ayarlanan maliyetten alınır. Maliyet, **İlgili işlem öğesi** sayfasında doğrudan güncelleştirilemez. **İlgili operasyon maddeleri** sayfasına eklenen tüm öğelerin maliyeti, **İlgili operasyonlar** sayfasındaki **Maliyet** alanına otomatik olarak eklenir.

1. Eklemeniz gereken her ek öğe için önceki adımı tekrarlayın.
1. Sayfaları kapatın.

### <a name="add-quality-charges-to-an-operation"></a>Bir işleme kalite giderleri ekleme

Bir işleme kalite giderleri eklemek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.

1. Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.
1. **İlgili işlemler** sayfasında, kalite giderleri eklemek istediğiniz işlemi seçin.
1. Eylem Bölmesi'nde, **Kalite giderleri**'ni seçin.
1. **İlgili işlem giderleri** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Gider kodu** – Eklemek istediğiniz kalite giderini seçin.
    - **Açıklama**: Gider grubunun detaylı bir açıklamasını girin.
    - **Gider değeri** – Gider tutarını girin.

1. Eklemeniz gereken her ek gider için önceki adımı tekrarlayın.
1. Sayfaları kapatın.

> [!NOTE]
> **Gider değeri** alanındaki tutar tüm kalite gideri için otomatik olarak toplanır ve **İlgili işlemler** sayfasındaki **Maliyet** alanındaki diğer tüm tutarlara eklenir.

### <a name="create-a-timesheet-on-an-operation"></a>Bir işlemde zaman çizelgesi oluşturma

Bir işleme zaman çizelgesi eklemek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.

1. Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.
1. **İlgili işlemler** sayfasında, zaman çizelgesi eklemek istediğiniz işlemi seçin.
1. Eylem Bölmesi'nde **Zaman çizelgesi**'ni seçin.
1. **İlgili işlem zaman çizelgeleri** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Tarih** – Çalışmanın yapıldığı tarihi belirtin. Varsayılan olarak bu alan şu anki tarihe ayarlanır.
    - **Çalışan** – Çalışmayı gerçekleştiren çalışanı seçin. Varsayılan olarak, bu alan geçerli kullanıcıya atanan çalışana ayarlanır.
    - **İşlem saatleri** – Seçili işleme harcanan saat sayısını girin.
    - **Faturalanan** – Ayrılan süre faturada bir müşteriye veya satıcıya faturalanmışsa bu onay kutusunu seçin.

    > [!NOTE]
    > Maliyeti, **Genel** sekmesindeki **Maliyet** alanında görüntüleyebilirsiniz. Maliyet, **Stok yönetimi parametreleri** sayfasında tanımladığınız oran kullanılarak hesaplanır.

1. Eklemeniz gereken her ek zaman çizelgesi satırı için önceki adımı tekrarlayın.
1. Sayfaları kapatın.

> [!NOTE]
> **Gider** alanındaki tutar tüm zaman çizelgesi satırları için toplanır ve **İlgili işlemler** sayfasındaki **Maliyet** alanındaki diğer tüm tutarlara eklenir.

## <a name="add-a-correction-to-a-nonconformance"></a>Bir uygunsuzluğa düzeltme ekleme

Bir uygunsuzluğa düzeltme eklemek için bu adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara düzeltme ekleyebilirsiniz.

1. Eylem Bölmesi'nde, **Düzeltmeler**'i seçin.
1. Eylem Bölmesinde, **Düzeltmeler** sayfasında ızgaraya satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Tanılama** – Oluşturmakta olduğunuz düzeltme türünü belirten tanılama türünü seçin.
    - **Çalışan** – Düzeltmeden sorumlu kişiyi seçin.
    - **Düzeltme önceliği** – Düzeltmenin nasıl önceliklendirilmesi gerektiğini ( *Düşük*, *Normal* veya *Yüksek*) belirtmek için bir seçenek belirleyin.
    - **Talep edilen tarih** – Düzeltici eylemin talep edildiği tarihi girin.
    - **Planlanan tarih** – Düzeltmenin tamamlanması beklenen tarihi girin.
    - **Kısa vadeli çözüm** – Düzeltici eylem uygunsuzluğu yalnızca kısa bir süre için düzelttiyse bu onay kutusunu seçin.

1. Sayfaları kapatın.

## <a name="mark-a-correction-as-completed"></a>Düzeltmeyi tamamlandı olarak işaretleme

Bir uygunsuzluk düzeltmesini tamamlandı olarak işaretlemek için bu adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.

    > [!NOTE]
    > Yalnızca onaylanan uygunsuzluklara düzeltme ekleyebilirsiniz.

1. Eylem Bölmesi'nde, **Düzeltmeler**'i seçin.
1. **Düzeltmeler** sayfasında, ızgarada, tamamlandı olarak işaretlemek istediğiniz düzeltmeyi seçin.
1. Eylem Bölmesinde, **Tamamlandı olarak işaretle** öğesini seçin.
1. Seçiminizi onaylamanız istenir. Devam etmek için **Tamam**'ı seçin. **Tamamlanma tarihi ve saati** alanı, geçerli tarih ve saate ayarlanır ve **Tamamlandı** onay kutusu işaretlenir.
1. Sayfayı kapatın.

## <a name="reopen-a-completed-correction"></a>Tamamlanmış bir düzeltmeyi yeniden açma

Tamamlanan bir düzeltmeyi yeniden açmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.
1. Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.
1. Eylem Bölmesi'nde, **Düzeltmeler**'i seçin.
1. **Düzeltmeler** sayfasında, ızgarada, yeniden açmak istediğiniz düzeltmeyi seçin.
1. Eylem Bölmesi'nde, **Yeniden aç**'ı seçin.
1. Seçiminizi onaylamanız istenir. Devam etmek için **Tamam**'ı seçin. Değer, **Tamamlanma tarihi ve saati** alanından silinir ve **Tamamlandı** onay kutusu temizlenir.
1. Sayfayı kapatın.

Artık düzeltmeye ek düzenlemeler veya güncelleştirmeler yapabilirsiniz. İşinizi bitirdiğinizde düzeltmeyi yeniden tamamlandı olarak işaretleyebilirsiniz.

## <a name="close-a-nonconformance"></a>Bir uygunsuzluğu kapat

Uygunsuzluğu kapatmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.
1. Izgarada bir kalite emri seçin.
1. Eylem Bölmesi'nde, **Sorgular \> Uygunsuzluklar**'ı seçin.
1. **Uygunsuzluklar** sayfasında, ızgaradaki hedef uygunsuzluğu seçin.
1. Eylem Bölmesi'nde, **İşlevler \> Uygunsuzluğu kapat**'ı seçin.
1. Seçiminizi onaylamanız istenir. Devam etmek için **Eve**'i seçin.
1. Sayfaları kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](../quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](../enable-quality-management.md)
- [Uygunsuzlukları onaylamaktan sorumlu çalışanlar](../quality-responsible-workers.md)
- [Uygunsuzluklar için karantina bölgeleri](../quality-quarantine-zones.md)
- [Uygunsuzluklar için tanılama türleri](../quality-diagnostic-types.md)
- [Uygunsuzluklar için kalite masrafları](../quality-charges.md)
- [Uygunsuzluklar için işlemler](../quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
