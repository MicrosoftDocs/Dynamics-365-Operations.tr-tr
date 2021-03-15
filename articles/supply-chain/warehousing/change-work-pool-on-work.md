---
title: İşteki iş havuzunu değiştir
description: Bu konu, varolan işin iş havuzunu değiştirmek için iş öğelerinin İş havuzunu değiştir düğmesini nasıl kullanabileceğinizi açıklamaktadır.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001161"
---
# <a name="change-work-pool-on-work"></a>İşteki iş havuzunu değiştir

[!include [banner](../includes/banner.md)]

İş havuzlarını, işi gruplar halinde düzenlemek için kullanabilirsiniz. Örneğin, belirli bir ambar konumundaki gerçekleşen işi sınıflandırmak için bir iş havuzu oluşturabilirsiniz.

*İşte iş havuzunu değiştir* özelliği iş öğeleri için Eylem Bölmesine bir **İş havuzunu değiştir** düğmesi ekler. Bu şekilde, ambar yöneticileri mevcut işin iş havuzunu kolayca değiştirebilir. Bu özellik, yöneticilerin ambar atölyesindeki değişikliklere hızla tepki vermesine olanak tanır ve değişen durumlara uyum yeteneği ve işi başka bir iş havuzuna aktarma gereksinimini geliştirmeye yardımcı olur.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>İşte iş havuzunu değiştir özelliğini açma

Bu özelliği ayarlamaya veya kullanmaya başlamadan önce, sisteminizde kullanılabilir olduğundan emin olmanız gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Değişiklik adı:** *İşte iş havuzunu değiştir*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>İşte iş havuzunu değiştir özelliğini ayarlama

Bu özelliği kullanmak için ayarlanmış iş havuzlarınız olmalıdır. Ayrıca iş şablonlarınızı otomatik olarak bir havuz atayacak şekilde ayarlayabilirsiniz. Bu konunun ilerleyen kısımlarında sağlanan örnek senaryo aracılığıyla çalışmak istiyorsanız, sisteminizi bu bölümde anlatıldığı şekilde ayarlayın.

### <a name="set-up-work-pools"></a>İş havuzlarını ayarlama

İş havuzları, iş öğelerini türlerine göre düzenlemenizi sağlar. *İşte iş havuzunu değiştir* özelliğini kullanmak için en az iki iş havuzunuz olması gerekir. İş havuzlarını görüntülemek ve eklemek için şu adımları izleyin:

1. **Ambar yönetimi \> Kurulum \> İş \> İş öğeleri** seçeneğine gidin.
1. **USMF** şirketinden demo verilerle çalışıyorsanız ve bu konunun ilerleyen kısımlarında örnek senaryo üzerinden çalışacaksanız, aşağıdaki ayarlara sahip iki iş havuzu ekleyin:

    - İş havuzu 1:

        - **İş havuzu kimliği:** *Webshop*
        - **Açıklama:** *Web Mağazası*

    - İş havuzu 2:

        - **İş havuzu kimliği:** *CallCenter*
        - **Açıklama:** *Çağrı Merkezi*

1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-work-templates"></a>İş şablonlarını ayarla

Her iş şablonunuz için, istediğiniz şekilde varsayılan bir iş havuzu ayarlayabilirsiniz. Her ilgili şablon için **İş havuzu kimliği** sütununa bir iş havuzu atarsınız. Bu durumda, belirli bir şablon kullanılarak oluşturulan tüm iş öğeleri atanan iş havuzunu otomatik olarak devralır. **USMF** şirketinden demo verilerle çalışıyorsanız ve bu konunun ilerleyen kısımlarında örnek senaryo üzerinden çalışacaksanız aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Eylem Bölmesinde, sayfayı düzenleme moduna geçirmek için **Düzenle** öğesini seçin.
1. Aşağıdaki değerleri ayarlayarak şablonu düzenleyin:

    - **İş şablonu:** *62 Paketleme için çek*
    - **İş havuzu kimliği:** *Webshop*

1. **Kaydet**'i seçin.

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryo, çalışma havuzunu değiştirerek varolan bir iş öğesinin işlem akışının nasıl değiştirileceğini gösterir. **USMF** şirketinden demo veriler ve bu konunun önceki bölümlerinde önerilen ayarlar kullanılır.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Satış siparişi oluşturma ve ambara serbest bırakma

1. Ambar *62*'de *A0001* ve *A0002* öğeleri için yeterli eldeki stok olduğunu doğrulayın. **Stok yönetimi \> Sorgular ve raporlar \>Eldeki stok listesi**'ne gidin ve filtreleri aşağıda gösterildiği gibi düzenleyin:

    - **Ambar** değeri *62* ile başlar.
    - **Madde numarası** değeri *A001* veya *A002*'dir.

    Demo verilerinde miktar olarak her birinden 10 birim bulunmalıdır.

    Daha sonra, bir satış siparişi oluşturmanız gerekir.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-007*
    - **Ambar:** *62*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *2*

1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.
1. Sayfayı kapatın.
1. **Satış siparişi satırları** hızlı sekmesinde, satış siparişinize başka bir satır eklemek için **Satır ekle**'yi seçin. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *2*

1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.
1. Sayfayı kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.
1. Serbest bırakma işleminden oluşturulan dalga kimliğini ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız. Dalga kodunu not edin.

### <a name="review-the-outbound-wave"></a>Giden dalgayı gözden geçirme

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. Kılavuzda, satış siparişinin serbest bırakma işleminden oluşturulan dalga kodunu arayın.
1. Ayrıntıları görüntülemek için dalga kodunu seçin.
1. **Dalga satırları** hızlı sekmesinde, satış siparişi için bir sevkiyat kodu gösterildiğinden emin olun.

    > [!TIP]
    > **Ambara serbest bırakıldığında dalgayı işle** seçeneğinin sevkiyat dalga şablonu için *Hayır* olarak ayarlanmış olması durumunda , işi oluşturmak için Eylem Bölmesindeki **Dalga** sekmesinden **İşlem**'i seçerek işlemi el ile oluşturmanız gerekir.

1. Dalganın işlenmiş olduğundan emin olun. Bu işlem gerekli işi oluşturur.

### <a name="view-work-details-and-change-the-work-pool"></a>İş ayrıntılarını görüntüleme ve iş havuzunu değiştirme

Oluşturulan işi görüntülemek ve iş havuzunu yönetmek için **İş ayrıntıları** sayfasını kullanabilirsiniz.

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. Yeni oluşturulan işe ilişkin satırı seçin. **Sipariş numarası** sütunu satış siparişi numarasını gösterir.

    **İş havuzu kimliği** alanı, iş şablonunda ayarlanmış olan iş havuzu kimliğine ayarlanır.

    > [!TIP]
    > **İş havuzu kimliği** alanını göremiyorsanız, sütunu kılavuza ekleyin ve sonra sayfayı yenileyin.

1. İş koduyla ilişkilendirilmiş çalışma havuzunu değiştirmek için, Eylem Bölmesindeki **İş** sekmesinde **İş havuzu kodunu değiştir**'i seçin.
1. **İş havuzunu değiştir** iletişim kutusunda, **Parametreler** hızlı sekmesindeki **İş havuzu kimliği** alanında *CallCenter*'ı seçin.
1. Değişiklerinizi uygulamak için **Tamam**'ı seçin.
1. **İş havuzu kimliği** alanı değerinin şimdi *CallCenter* olarak değiştirilmiş olduğuna dikkat edin.

> [!IMPORTANT]
> **İş havuzunu değiştir** iletişim kutusu göründüğünde, **İş havuzu kimliği** alanı varsayılan olarak boş olabilir. Değişiklikleri uygulamak için **Tamam**'ı seçtiğinizde alan boşsa, iş havuzunu tamamen işten kaldırırsınız.
>
> İş havuzlarını değiştirmeye ek olarak, bu yordamı iş havuzu olmayan bir iş öğesine iş havuzu eklemek veya iş havuzu olan bir iş öğesinden iş havuzunu kaldırmak için de kullanabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]