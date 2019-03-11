---
title: Esnek gruplar
description: Bu konu, esnek grupların Saat ve işe devamda nasıl kullanıldığını açıklar.
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgFlexGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: aae00f3605a6598a34e58fad3e06e687476dd859
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "361211"
---
# <a name="flex-groups"></a>Esnek gruplar

[!include[banner](../includes/banner.md)]

Esnek çalışma saatleri şirketlerin çalışanlara iş yükünün düşük olduğu dönemlerde ek izin sunarak fazla mesai ödemelerini en aza indirmesine olanak sağlar. Bu özellik, örneğin iş yükünde dönemsel değişiklikler yaşayan segmentlerle ilgilidir.

Esnek grupları bir çalışanın esnek saatleri için aşağıdaki kuralları ve ilkeleri ayarlamak için kullanabilirsiniz:

- Esnek düzenlemeler için kurallar
- Çalışanın esnek bakiyesini hesaplama ilkesi

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Esnek gruplarda esnek çalışma saatleri ayarlama

- **Saat ve işe devam** \> **Kurulum** \> **Gruplar** \> **Esnek gruplar**'ı seçerek esnek saatler için esnek grupları ayarlayın.

## <a name="associate-workers-with-flex-groups"></a>Çalışanları esnek gruplarla ilişkilendirme

- **Saat ve işe devam** \> **Kurulum** \> **Zaman kayıtlı çalışanlar**'a gidin.

## <a name="rules-for-flex-regulations"></a>Esnek düzenlemeler için kurallar

Esnek sınırları tanımlamak için esnek düzenlemeler kurallarını veya çalışanın esnek hesabında izin verilen minimum ve maksimum saat sayısını kullanabilirsiniz. Esnek sınırlar esnek grupta ayarlanır. Esnek sınırlar açıldığında, çalışanın esnek bakiyesi ve ödemesi ayarlanabilir.

Bir çalışanın izin verilen esnek minimum saati aşılırsa (diğer bir deyişle, esnek hesaptaki saat sayısı belirtilen minimumdan azsa), çalışanın esnek bakiyesini bir esnek düzenleme yaparak ayarlamak için bu yöntemleri kullanabilirsiniz.

- Çalışanın esnek hesabı belirtilen izin verilen minimum değere ayarlanabilir ancak bu esnek hesabın izin verilen minimum altında olduğu saat sayısını çalışanın ödemesinden düşmeden yapılır.
- Çalışanın ödemesinde esnek hesabın izin verilen minimum değerin altında olduğu saat sayısı için kesinti yapılabilir. Bu kesinti, negatif veya pozitif ödeme birimi olan belirli bir ödeme türü için ödeme maddeleri oluşturularak yapılır.

Çalışanın izin verilen esnek maksimum saati aşılırsa, bir esnek düzenlemesi yaparak çalışanın esnek bakiyesini bu yöntemleri kullanarak ayarlayabilirsiniz:

- Çalışanın esnek hesabı belirtilen izin verilen maksimum değere ayarlanabilir ancak bu çalışanın izin verilen maksimum değer üstünde çalıştığı saat sayısı için çalışana ödeme yapılmadan gerçekleştirilir.
- Çalışanın izin verilen maksimum saat üzerinde çalıştığı saat sayısı ödemeye dönüştürülebilir. Bu dönüştürme belirli bir ödeme türü için ödeme maddeleri oluşturarak yapılır.

Aşağıdaki durumlarda bir esnek bakiye ayarlayabilirsiniz:

- Bordro verisini temel alan bir ödeme dosyası **Ödeme aktar** işi kullanılarak dışa aktarıldığında. Bordro verileri çalışanın kaydını **Onayla** sayfasından aktardığınızda oluşturulur.
- **Esnek bakiyeyi ayarla** işi işlendiğinde.

> [!NOTE]
> Esnek düzenlemeler çalışan kayıtlarının **Onayla** sayfasından günlük onayı veya aktarımı sırasında gerçekleşmez.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Çalışanın esnek bakiyesini hesaplama ilkesi

Çalışanın esnek bakiyesinin saatlerini hesaplama ilkesi esnek grupta ayarlanır. **Saat ve işe devam** \> **Kurulum** \> **Gruplar** \> **Esnek gruplar**'ı seçin. 

Aşağıdaki iki ilke kullanılabilir:

- **Zaman** – Çalışanın esnek saatleri yalnızca çalışanın gün için kaydedilen süresinden hesaplanır. Çalışanın günlük kayıtları hesaplanırken, güne ait Esnek+ ve Esnek- saatlerin sayısı çalışanın zaman profilinde tanımlanan Esnek+ ve Esnek- bölgelerinden hesaplanır.
- **Ödeme türleri** – Çalışanın esnek saatleri çalışanın ödeme sözleşmesinde tanımlanan Esnek+ ve Esnek- ödeme türleri kazançları temel alınarak hesaplanır. Ödeme sözleşmesi zaman kayıtlı çalışan ile ilişkilidir. Ödeme türlerini örneğin çalışanın esnek hesabını bir veya daha fazla esnek alandaki belirli bir faktöre göre artırmak istediğinizde esnek hesapları yönetmek için kullanmak isteyebilirsiniz.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>Senaryo 1: İzin verilen esnek minimum aşıldığından çalışanın ödeme ve esnek hesabını ayarlama

Esnek saatlerde çalışabilen bir çalışanın negatif esnek hesabı vardır.

- **Esnek hesap:** -4

Çalışan aşağıdaki yapılandırmaya sahip bir esnek grupla ilişkilendirilir:

- **Esnek minimum:** -0,5
- **Minimum ödeme türü:** 1302
- **Ödeme türü faktörü:** -1,00

Çalışan esnek hesabı ile izin verilen minimum esnek saati arasındaki farkın gösterdiği gibi çalışan 3,5 saatlik izin verilen minimum esnek saat sayısını aşmıştır.

Bordro yöneticisi çalışanın ödeme verisini **Ödeme transferi** veya **Esnek düzeltme** işi çalıştırarak aktardığında, aşağıdaki ayarlamalar yapılır:

- Çalışanın esnek hesabı 3,5 saat ayarlanır. Bu nedenle, -4,0 olan esnek bakiye çalışan için minimum esnek izin verilen değer olan 0,5 saate ayarlanır.
- 1302 türünde bir ödeme maddesi oluşturulur. Bu ödeme maddesi, çalışanın ödemesinden düşülecek olan -3,5 saatlik ödeme birimine sahiptir. Bu durumda, ödeme birimi negatif bir sayıdır çünkü 3,5 saatlik pozitif ayarlama esnek grupta tanımlanmış -1,0 olan negatif ödeme türü faktörüyle çarpılır. Bu ödeme maddesi **Ödeme transferi** işi tarafından oluşturulan ödeme dosyasının bir parçası olur.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>Senaryo 2: İzin verilen esnek maksimum aşıldığından çalışanın ödeme ve esnek hesabını ayarlama

Esnek saatlerde çalışabilen bir çalışanın pozitif esnek hesabı vardır.

- **Esnek hesap:** 6

Çalışan aşağıdaki yapılandırmaya sahip bir esnek grupla ilişkilendirilir:

- **Esnek maksimum:** 2,0
- **Minimum ödeme türü:** 1302
- **Ödeme türü faktörü:** -1,0

Çalışan esnek hesabı ile izin verilen maksimum esnek saati arasındaki farkın gösterdiği gibi çalışan 4,0 saatlik izin verilen maksimum esnek saat sayısını aşmıştır.

Bordro yöneticisi çalışanın ödeme verisini **Ödeme transferi** veya **Esnek düzeltme** işi çalıştırarak aktardığında, aşağıdaki ayarlamalar yapılır:

- Çalışanın esnek hesabı -4,0 saate göre ayarlanır. Bu nedenle, 6,0 olan esnek bakiye çalışan için maksimum esnek izin verilen değer olan 2,0 saate ayarlanır.
- 1302 türünde bir ödeme maddesi oluşturulur. Bu ödeme maddesi, çalışanın ödemesine eklenecek olan 4,0 saatlik ödeme birimine sahiptir. Bu durumda, ödeme birimi pozitif bir sayıdır çünkü 4,0 saatlik negatif ayarlama esnek grupta tanımlanmış -1,0 olan negatif ödeme türü faktörüyle çarpılır. Bu ödeme maddesi **Ödeme transferi** işi tarafından oluşturulan ödeme dosyasının bir parçası olur.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>Senaryo 3: Ödeme türlerini temel alarak bir çalışanın esnek bakiyesini yönetme

Daha önce de açıkladığımız gibi, esnek hesaplar çalışanın zaman profilinde tanımlanan Esnek+ ve Esnek- bölgelerine kaydedilen zaman veya çalışanın ödeme sözleşmelerinde tanımlanan ödeme türleri temel alınarak yönetilebilir. Ödeme türleri kullanılırsa, çalışanın esnek hesabı çalışanın kaydını **Onayla** sayfasından aktardığınızda oluşturulan ödeme maddelerine göre ayarlanır. Ödeme türlerini örneğin çalışanın esnek hesabını bir veya daha fazla esnek alandaki belirli bir faktöre göre artırmak istediğinizde esnek hesapları yönetmek için kullanmak isteyebilirsiniz.

Bu senaryo bir iş gününü gösteren aşağıdaki esnek profili kullanır.

| Profil türü  | Başlat    | Bitir      |
|---------------|----------|----------|
| Esnek+         | 12:00 | 08:00 |
| Giriş saati      | 08:00 | 08:00 |
| Esnek-         | 08:00 | 09:00 |
| Standart zaman | 09:00 | 11:30 |
| Ücretli mola    | 11:30 | 12:00 |
| Esnek-         | 12:00 | 04:00 |
| Çıkış saati     | 04:00 | 04:00 |
| Esnek+         | 04:00 | 12:00 |

Bu durumda, çalışanın esnek bakiyesini ödeme türlerini temel alarak yönetebilmek istersiniz. Bu nedenle, çalışanın esnek grubundaki **Ödeme türlerine göre** seçeneğini **Evet** olarak ayarlamanız gerekir.

Esnek saatleri hesaplamak için yeni bir ödeme türü de tanımlamanız gerekir. Bu senaryoda ödeme türü adı **FlexCnt**'dir.

| Ödeme türü | Tanım  |
|----------|--------------|
| FlexCnt  | Esnek sayacı |

Sonra, bir ödeme türü ayarlamak için şu adımları izleyin ve yeni türdeki satırları bir ödeme profiline ekleyin.

1. **Saat ve işe devam** \> **Kurulum** \> **Gruplar** \> **Esnek gruplar**'ı ve **Yeni**'yi seçin.
2. Hem **Esnek+** hem de **Esnek-** alanında yeni ödeme türünü (**FlexCnt**) belirtin.
3. **Saat ve işe devam** \> **Kurulum** \> **Ödeme sözleşmeleri**'ni ve ardından **Sözleşme satırları**'nı seçin.
4. **Pazartesi** için **Esnek+** profil türü için aşağıdaki üç satırı ekleyin.

    | Ödeme türü | Tanım  | Başlangıç saati | Bitiş zamanı  | Minimum | Maksimum | Faktör |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Esnek sayacı | 12:00  | 06:00 | 00,00   | 00,00   | 1.00   |
    | FlexCnt  | Esnek sayacı | 06:00  | 12:00 | 00,00   | 02,00   | 1,50   |
    | FlexCnt  | Esnek sayacı | 06:00  | 12:00 | 02,00   | 06,00   | 2.00   |

    > [!NOTE]
    > Her satır farklı bir zaman aralığı için kullanılır ve farklı bir faktöre sahiptir. Çalışanın bir zaman aralığında çalıştığı esnek saatler bu satıra ilişkin faktörle çarpılır. Örneğin 18:00 ile 20:00 arasında çalışılan saatler 1,50 ile çarpılır. Faktör, **Ödeme sözleşmesi satırları** sayfasının **Genel** sekmesindeki **Faktör** alanında belirtilir.

Çalışan gün için aşağıdaki kayıtları girer.

| Günlük kaydı türü | Başlat    | Bitir      |
|---------------------------|----------|----------|
| Giriş saati                  | 07:00 | 07:00 |
| Üretim işi            | 07:00 | 09:00 |
| Çıkış saati                 | 09:00 | 09:00 |

Ödenmesi gereken tutar çalışanın kaydı temel alınarak **Onayla** sayfasında hesaplanır. Kayıt hesaplandıktan sonra, sonuçları **Saatler** sekmesinde görebilirsiniz. Bu senaryo için aşağıdaki alanlarla ilgilenirsiniz.

| Esnek + | Esnek - | Saat  | Ödeme zamanı |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 08,00    |

Esnek+ zaman tutarı altı saattir ve hesaplama zaman profilindeki esnek bölgeleri temel alır. Bu tutar 07:00 ile 08:00 arasındaki bir saatlik Esnek+ zamanından ve 16:00 ile 21:00 arasındaki beş saatlik Esnek+ zamanından oluşur.

Kayıtları aktardığınızda, Esnek+ zamanı tutarının 6,0 saat yerine 8,0 saat olarak değiştiğini görürsünüz.

| Esnek + | Esnek - | Saat  | Ödeme zamanı |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 08,00    |

Bu değişikli aktarım sonrasında gerçekleşir çünkü esnek saatler zaman yerine ödeme türleri temel alınarak hesaplanmıştır. Aşağıdaki tabloda sekiz saatin nasıl hesaplandığı gösterilmiştir:

| İlk     | Son       | Saat | Faktör    | Esnek hesap |
|----------|----------|------|-----------|--------------|
| 07:00 | 08:00 | 1    | 1         | 1            |
| 04:00 | 06:00 | 2    | 1         | 2            |
| 06:00 | 08:00 | 2    | 1.5       | 3            |
| 08:00 | 09:00 | 1    | 2         | 2            |
|          |          |      | **Toplam** | **8**        |
