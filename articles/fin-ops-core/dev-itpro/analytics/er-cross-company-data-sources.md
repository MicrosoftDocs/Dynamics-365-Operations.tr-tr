---
title: Elektronik raporlamada (ER) şirketler arası veri kaynakları
description: Bu konu, Elektronik raporlamada (ER) şirketler arası veri kaynaklarını nasıl kullanabileceğinizi açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1a5c05b65c9022220056947471e95b703d923dc5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680842"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Elektronik raporlamada (ER) şirketler arası veri kaynakları

[!include[banner](../includes/banner.md)]

Çeşitli biçimlerde giden belgeler oluşturmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz. Bir belge oluşturulurken, bir ER biçimi, karşılık gelen bir ER model eşlemesinde yapılandırılmış veri kaynaklarını çağırır. Kayıt alma amacıyla uygulama tablolarına erişimi yapılandırmak için **Tablo kayıtları** türünde ER veri kaynakları kullanabilirsiniz. Erişilen tablo bir paylaşılan tabloysa (yani şirket kimlik tanımlayıcısı olmadan verilerin kaydedildiği bir tabloysa) bu veri kaynağı tüm kayıtları döndürür. Erişilen tablo bir şirkete bağlı tabloysa (yani verilerin şirkete göre kaydedildiği bir tabloysa) bu veri kaynağı yalnızca o şirket (yani ER biçiminin çalıştığı şirket bağlamı) için kaydedilmiş kayıtları döndürür.

Bir model eşlemede **Tablo kayıtları** türündeki her veri kaynağı artık şirketler arası veri kaynağı olarak işaretlenebiliyor. Bu sayede, uygulama tablolarındaki şirketler arası verilere erişmek için **Tablo kayıtları** türünde veri kaynakları kullanabilirsiniz.

Bir veri kaynağını şirketler arası olarak işaretlerseniz aşağıdaki davranış gerçekleşir:

- CompanyInfo dışındaki herhangi bir paylaşılan tabloya başvuran bir veri kaynağı için, veri kaynağı, başvurulan tablodaki tüm kayıtları döndürür. 
- CompanyInfo tablosuna başvuran bir veri kaynağı için, CompanyInfo paylaşılan bir tablo olsa bile, veri kaynağı tanımlanan kapsamdan bir şirkete ait kimlik tanımlayıcısını içeren kayıtları döndürür.
- Şirkete bağlı bir tablo için, veri kaynağı, başvurulan tablodaki, tanımlanan kapsamdan bir şirkete ait kimlik tanımlayıcısını içeren kayıtları döndürür.

Sistem sorgusu iletişim kutusunda, şirketler arası olarak işaretlenmiş bir veri kaynağı için **Sorgu iste** seçeneğini açıldıysa, **Şirket aralığı** sekmesine eklemek üzere bir veya daha fazla şirketi el ile seçebilirsiniz.

> [!IMPORTANT]
> Diğer filtrelerde olduğu gibi, bir ER biçimi çalıştırdığınızda, şirket filtresi, sorgular için son kullanılan değer olarak kalır. Bir veri kaynağı için şirketler arası değeri değiştirdiğiniz zaman filtre otomatik olarak değişmez. Başka bir veri kaynağı için farklı bir şirketler arası değeri kullanmak için ilgili kullanıcıya özgü seçimi silin.

Şirketler arası olarak işaretlenen her veri kaynağı için, kullanmak istediğiniz kayıtları ER ifadelerinde **FILTER** ve **WHERE** işlevleri kullanarak seçin. **dataAreaID** alanı şirket kimlik tanımlayıcısı olarak da kullanılabilir. Şu anda **dataAreaID** alanı, **FILTER** işlevi kullanılırken aşağıdaki koşul türleriyle sınırlandırılmıştır:

- Yalnızca tek bir **dataAreaID** alanı karşılaştırması olan koşullar desteklenir.
- Yalnızca, kayıtlar listesindeki öğelere bağlı olmayan ifadelerin yer aldığı karşılaştırmalara izin verilir.

Bu nedenle, aşağıdaki ifade geçerlidir.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Varsayılan olarak, kapsam, geçerli uygulamanın tüm şirketlerini içerir. Ancak, buna kısıtlama getirilebilir. Tek bir ER biçimine ilişkin şirketler arası veri erişim kapsamını kısıtlamak için, biçime belirli bir kuruluş hiyerarşisi atayın. Bir ER biçimi için bir hiyerarşi tanımlandığı zaman, biçim şirketler arası veri kaynaklarını çağırsa bile, yalnızca atanan hiyerarşide sunulan tüzel kişiliklerin kayıtları döndürülür. Artık var olmayan bir hiyerarşiye başvuru tanımlandığı zaman, varsayılan kapsam uygulanır ve biçim, şirketler arası veri kaynaklarını çağırır. Bu durumda, tüm uygulama şirketlerine ait kayıtlar döndürülür.

Tek bir ER biçimine atanan kuruluş hiyerarşisi için **Taslak kullan** seçeneği etkinleştirildiği zaman, şirketler arası veri kaynakları için kapsamı tanımlamada bu hiyerarşinin taslak sürümünden tüzel kişiliklerin kullanılacağına dikkat edin. Taslak sürüm yoksa, bunun için, bu kuruluş hiyerarşisinin son yayımlanan sürümünden tüzel kişilikler kullanılır.

Tek bir ER biçimine atanan kuruluş hiyerarşisi için **Taslak kullan** seçeneği kapatıldığı zaman, şirketler arası veri kaynakları için kapsamı tanımlamada bu kuruluş hiyerarşisinin son yayımlanan sürümünden tüzel kişilikler kullanılacağına dikkat edin. ER çerçevesinde henüz kuruluş hiyerarşilerinin tarih geçerliliği desteklenmiyor.

Hiyerarşi, ER çalışma alanından veya **Kuruluş yönetimi \> Elektronik raporlama \> Biçimler için tüzel kişilik filtresi** menü öğesi kullanılarak erişilebilen belirli bir sayfadaki bir biçime atanabilir. Sayfaya erişmek için, bir kullanıcıya **Biçimler için tüzel kişilik filtrelerini koru** ayrıcalığı (ERMaintainFormatMappingLegalEntityFilters) verilmelidir. Biçim için hiyerarşi tabanlı tüzel kişilikler kapsamı kısıtlaması, kullanıcının sistem sorgu iletişim kutusunda el ile belirtebileceği kısıtlamaya ek olarak uygulanır. Biçim çalıştırılınca bu kısıtlamaların kesişimi kullanılır.

Bu özellik hakkında daha fazla bilgi için, 7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin bir parçası olan ve [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirilebilen **ER - Şirketler arası modda şirkete bağlı tabloların kayıtlarına erişim** görev kılavuzunu oynatın. Bu görev kılavuzu, şirketler arası modda uygulama tablolarına erişmek için bir ER model eşlemesi ve ER biçimi yapılandırma işleminde size yol gösterir.

Görev kılavuzunu tamamlamak için aşağıdaki dosyaları indirin:

- [ER modeli yapılandırması - CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER biçimi yapılandırması - CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)
