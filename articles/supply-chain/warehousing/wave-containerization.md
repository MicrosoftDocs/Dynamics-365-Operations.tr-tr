---
title: Konteyner Kullanımı
description: Bu konu, yüklerde konteyner kullanımının nasıl otomatikleştirileceğini açıklar. Bir dalga işlendiğinde otomatik kapsayıcı hale getirme işlemi, kapsayıcılar ve sevkiyatlara malzeme çekme çalışması oluşturur.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f738c0404a41ef862d4985a170a0eba991e4dd4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686640"
---
# <a name="containerization"></a>Konteyner Kullanımı

[!include [banner](../includes/banner.md)]

Bu konu, yüklerde konteyner kullanımının nasıl otomatikleştirileceğini açıklar. Bir dalga işlendiğinde otomatik kapsayıcı hale getirme işlemi, kapsayıcılar ve sevkiyatlara malzeme çekme çalışması oluşturur.

Konteyner kullanımını ayarlamak için şunları oluşturmanız gerekir:

- **Konteyner türü**: Konteynerlerin fiziksel özelliklerini tanımlar. Stok maddelerini, bölmeler veya paletler gibi belirli tür ve ambalaj boyutunda paketlemek için konteyner tipleri kullanın.
- **Konteyner grupları**: Benzer konteyner türleri için grupları oluşturun. Örneğin, bir konteyner grubu benzer boyut boyutlarına sahip olan konteyner tipleri içerebilir. Konteyner grubu, konteynerlerin hangi sırayla paketleneceğini ve her bir konteynerin doldurulma yüzdesini belirtir.
- **Konteyner yapısı şablonu**: Konteyner kullanımı kurallarını tanımlayan şablonlar oluşturun. Örneğin, stok ve diğer ambalaj stratejilerini karıştırma kuralları.
- **Dalga şablonları**: Konteyner kullanma için malzeme çekme çalışması oluşturmak üzere bir veya daha fazla dalga şablonu ayarlayın.

## <a name="create-wave-templates-for-containerization"></a>Konteyner kullanımı için dalga şablonları oluşturma

Konteyner kullanımı için bir veya daha fazla nakliye dalgası şablonu ayarlamanız gerekir. Dalga şablonları aşağıdakileri belirleyen ölçütleri içerir:

- Dalgaların nasıl işleneceği. Bu, el ile veya otomatik olabilir.
- Malzeme çekme işinin nasıl oluşturulacağı. Bu, dalga yöntemleri tarafından belirlenir. Dalga şablonu, **Konteyner kullanımı** yöntemi içermelidir.
- Maddelerin veya tahsisat satırlarının bir dalgaya nasıl eşleştirileceği.

Daha fazla bilgi için bkz. [Dalga şablonları](wave-templates.md).

## <a name="create-container-types"></a>Konteyner türleri oluşturma

Fiziksel boyutlar ve ağırlık kapasitesi için maksimum değerler dahil olmak üzere konteynerlerin açıklamalarını oluşturmak için konteyner türleri kullanın. Konteynerli bir dalga işlenirken, Konteynerler Konteyner türü bilgilerine göre oluşturulur.

Konteyner türü ayarlamak için aşağıdaki adımları takip edin:

1. **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner türü** öğesine gidin.
1. Yeni bir konteyner türü oluşturmak için **Yeni**'yi seçin.
1. Konteyner türü için benzersiz bir tanımlayıcı (ID) ve açıklama girin.
1. **Dara ağırlık** alanında, konteynerin gerçek veya tahmini ağırlığını girin.
1. **Maksimum ağırlık** alanına, konteynerin tutabileceği maksimum ağırlığı girin.
1. **Konteyner kullanımı maksimum birimi**, **Konteyner kullanımı maksimum uzunluğu**, **Konteyner kullanımı maksimum genişliği** ve **Konteyner kullanımı maksimum yüksekliği** alanları konteynerin fiziksel boyutlarını belirtir.

    > [!NOTE]
    > Uzunluk ve genişlik değerleri değiştirilebilir. Bu, gerekirse maddeleri yana doğru veya x ekseninde döndürebileceğiniz anlamına gelir. Örneğin, uzunluk 2 ayak ve genişlik 1 ayak ise uzunluğu 1 ayak ve genişliği 2 ayak olarak değiştirebilirsiniz. Bunun Yükseklik boyutu için geçerli olmadığını unutmayın. Bir maddeyi dikey olarak döndürmek için yükseklik değerini değiştiremezsiniz.

1. Öznitelik alanlarında bulunan konteyner için özel öznitelik değerleri seçin. Öznitelikler, başka türlü kullanılamayan bir değeri temel alarak maddeleri filtrelemek veya sıralamak için kullanılan özel değerlerdir. Örneğin, belirli bir müşteriyle ilgili maddeleri paketlemek istiyorsanız, müşteri adı için bir öznitelik oluşturabilirsiniz. **Konteyner Öznitelikleri** sayfasında bu öznitelikleri oluşturabilirsiniz.

## <a name="create-container-groups"></a>Konteyner grupları oluşturma

Konteyner türleri için mantıksal grupları ayarlayabilirsiniz. Her bir grup için, konteynerleri paketleyecek sıralamayı ve konteynerlerin doldurulması istediğiniz yüzdesi belirtebilirsiniz. Maddenin boyut özellikleri konteynerin içine sığıp sığmayacağını belirler. Maddenin ebat boyutuna en yakın olan konteyner kullanılacaktır. Bir grup içinde birden çok konteyner türü varsa, sırayı boyuta göre düzenlemenizi öneririz, böylelikle en büyük konteyner birinci, sıralama içerisinde birinci numarada olur ve en küçük konteyner en sona kalır.

Konteyner grubu ayarlamak için aşağıdaki adımları takip edin:

1. **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner grupları** öğesine gidin.
1. Bir konteyner grubu oluşturmak için **Yeni**'yi seçin.
1. Konteyner grubu için benzersiz bir tanımlayıcı (ID) ve açıklama girin.
1. **Ayrıntılar** hızlı sekmesinde, gruba konteyner türü eklemek için **Yeni**'yi seçin.
1. **Konteyner türü** alanında bir konteyner türü seçin.
1. Konteyner tiplerinin paketleneceği sırayı belirtmek için **yukarı taşı** veya **aşağı taşı** seçeneğini belirleyin.

## <a name="create-container-build-templates"></a>Konteyner yapılandırma şablonları oluşturma

Konteyner kullanımı işlemi için stok karıştırma kuralları ve diğer ambalaj stratejileri gibi kurallar ayarlayabilirsiniz. Örneğin, çalışanların aynı konteynerdeki farklı müşterilerden gelen satış siparişlerini temsil eden tahsisat satırlarını paketlememesi için bir kural ayarlayabilirsiniz.

Konteyner yapılandırma şablonu ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner yapı şablonu** öğesine gidin.
1. Yeni bir Konteyner yapı şablonu oluşturun.
1. **Konteyner kullanımı adı** ve **sıra numarası** alanlarında, Konteyner kullanımı şablonunun adını ve tahsisat satırlarıyla eşleşen siparişi girin.

    > [!NOTE]
    > Sistem, tahsisat satırının Sorgu ölçütlerini karşılayan ilk şablonu uygular. Bu nedenle en belirgin ölçütlerle sahip şablonu listenin en üstüne koyun. Ölçütler ne kadar geniş ise, tahsisat satırının ölçütlere uygun olması o kadar olasıdır. Bu, yanlış bir Konteynere atanmış satırlara yol açabilir. Gerekirse Şablonların sırasını değiştirmek için **yukarı taşı** veya **aşağı taşı** seçeneğini belirleyebilirsiniz.

1. **Konteyner grup kodu** alanında, konteyner oluşturulacak konteyner grubunu seçin.
1. **Taban sorgu türleri** alanında, nelerin paketleneceğini ve filtre sorgusunun neyi temel alacağını belirleyen sorgu türünü seçin. Aşağıdaki seçenekler bulunur:

      - **Satış tahsisat satırı**: Satış siparişleri için oluşturulan tahsisat satırlarını paketleyin.
      - **Transfer tahsisat satırı**: Transfer siparişleri için oluşturulan tahsisat satırlarını paketleyin.
      - **Konteyner**: Konteyner kullanımı işlemi tarafından önceden oluşturulmuş bir Konteyneri paketleyin. Örneğin, bu, iç içe geçmiş Konteynerler için kullanılır.

        > [!NOTE]
        > İç içe geçmiş Konteynerleri kullanmak için Konteyner kullanımı yöntemini tekrarlanabilir yapmalısınız. Daha fazla bilgi için bkz. [Dalga şablonları](wave-templates.md).

1. **Genel** hızlı sekmesinde, **dalga adımı kodu** alanına, konteyner yapı şablonunu bir dalga şablonundaki adımlara bağlayan dalga işlemi yönteminin benzersiz tanımlayıcısını girin.
1. Çalışanların bir iş emrindeki maddeleri ayrı konteynerler olarak paketlemeleriyle izin vermek için, **Bölünmüş çekmelere izin ver** onay kutusunu seçin. Bu, tüm miktarın konteynere sığmasını gerektirir. Tahsisat satırındaki en büyük ölçü birimi her zaman kullanılır.
1. **Birime göre paketle** alanında, konteyneri temsil edecek ölçü birimini seçin. Örneğin, bir kutunun konteyner olduğunu belirtebilirsiniz. Ölçü birimine göre paketlerseniz ölçü birimi konteyner olduğundan aynı zamanda bir konteyner grubu belirleyemezsiniz.
1. **Konteyner paketleme stratejisi** alanında, kullanılacak paketleme stratejisini seçin. Aşağıdaki seçenekler bulunur:

    > [!NOTE]
    > Strateji yalnızca satış tahsisat satırları için ve transfer tahsisat satırları için geçerlidir.

      - **Tüm açık konteynerlere paketle**: Sistem tahsisat satırının konteyner kullanımı döngüsünde oluşturulan herhangi bir konteynere sığıp sığmayacağını değerlendirir.
      - **Yalnızca geçerli konteynere paketle**: Sistem yalnızca tahsisat satırının en son oluşturulan konteynere sığıp sığmayacağını değerlendirir.

    Konteyner paketleme stratejileriyle nasıl çalışılacağını gösteren daha fazla bilgi ve örnek için bkz. [Konteyner paketleme stratejileri](container-packing-strategy-overview.md).

1. Konteynerler içindeki paketleme tahsisat satırları için kurallar eklemek için **Karıştırma mantığı aralıkları**'nı seçin. Örneğin, çalışanların aynı konteynerdeki iki farklı madde için tahsisat satırlarına paket oluşturmasını sağlayacak bir kural oluşturabilirsiniz. Karıştırma kuralı oluşturmak için aşağıdaki adımları izleyin:

    1. **Karıştırma mantığı aralıkları** sayfasında **yeni**'yi seçin.
    1. **Tablo** alanında, karıştırma mantığı aralığı için ölçüt olarak kullanılacak alanı içeren tabloyu seçin.
    1. **Alan Seçimi** alanında, karıştırma mantığı aralığı için ölçüt olarak kullanılacak alanı içeren alanı seçin.
    1. Karıştırma mantığı aralığı için tüm ölçütleri ekleyinceye kadar bu adımları yineleyin.

    > [!NOTE]
    > Karıştırma mantığını kullanırsanız, filtre ölçütü sorgusunda aynı alanlara göre sıralama yapmanız önerilmektedir. Bu, oluşturulan konteyner sayısını azaltacaktır.
