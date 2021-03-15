---
title: Bağlı şirket verilerini dosyalara dışarı aktarma
description: Bu konu, Microsoft Dynamics 365 Finance'teki verileri dışarı aktarmak ve daha sonra konsolide edilmiş bir tüzel kişiliğe içeri aktarmak için nasıl hazırlık yapılacağı açıklanmaktadır.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968691"
---
# <a name="export-subsidiary-data-to-files"></a>Bağlı şirket verilerini dosyalara dışarı aktarma

[!include [banner](../includes/banner.md)]

Bağlı verileri, daha sonra konsolide edilmiş bir tüzel kişiliğe içeri aktarılabilen dosyalara dışarı aktarmaya hazırlanmak için **Dışarı Aktar** sayfasını (**Sistem yönetimi \> Çalışma alanları \> İçeri aktarma/Dışarı aktarma**) kullanabilirsiniz. İçeri ve dışarı aktarma işlemleri hakkında daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Konsolidasyon işlemi için tüzel kişilik oluşturun. Tüzel kişilik oluşturma hakkında bilgi için bkz. [Tüzel kişilik oluşturma](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Daha fazla bilgi için bkz [Konsolidasyon işleminde kullanılacak tüzel kişilik hazırlama](prepare-company-for-consolidation.md) ve [Konsolidasyon için bir alt şirket tüzel kişiliği ayarlama](set-up-subsidiary-company-for-consolidation.md). 

2. **Konsolidasyonlar \> Şirket bakiyelerini dışarı aktar**'a gidin. **Şirket bakiyelerini dışarı aktar** sayfasında, **Ölçüt** sekmesinde, aşağıdaki alanları ayarlayarak konsolidasyonun ayrıntılarını belirtin.

    | Alan                             | Tanım |
    |-----------------------------------|-------|
    | Ana hesap                      | Konsolide edilecek hesapları belirtin. Tüm hesapları dahil etmek için bu alanı boş bırakın. |
    | Konsolidasyon hesabı kullanma         | Konsolidasyon hesaplarını belirlediyseniz bu seçeneği **Evet** olarak ayarlayın. |
    | Şuradan konsolidasyon hesabı seç: | **Ana hesap** veya **Konsolidasyon hesabı grubu**'nu seçin. |
    | Konsolidasyon hesap grubu       | Seçtiğiniz konsolidasyon hesabı için bir konsolidasyon hesabı grubu seçin. |
    | Konsolidasyon dönemi              | Konsolidasyon için "Başlangıç" ve "Bitiş" tarihi belirtin. |
    | Gerçek tutarları dahil et            | Fiili tutarları dahil etmek için bu seçeneği **Evet** olarak ayarlayın. |
    | Bütçe tutarlarını dahil et            | Bütçe tutarlarını konsolidasyona dahil etmek için bu seçeneği **Evet** olarak ayarlayın. |
    | Bütçe modelleri                     | Dahil edilecek bütçe modelini belirtin. |

3. **Mali boyutlar** sekmesinde konsolidasyon ayrıntılarını belirtin:

    - Bağlı hesaplardaki hareketlerden konsolide edilmiş tüzel kişilikteki hareketlere aktarılması gereken mali boyut bilgilerini belirtin.
    - Listeden mali boyutları seçin.
    - Konsolide edilen her mali boyut için doğru özellikleri tanımlayın. Mevcut seçenekler arasında **Boyut**, **Grup boyutu**, **Şirket hesapları** ve **Hesap** vardır.

        > [!NOTE]
        > **Grup boyutu** seçeneği, konsolide edilen şirket grupları tarafından kullanılan boyut değerini tanımlamanızı sağlar.

    - Konsolide edilecek segment emrini belirtin.

4. **Tüzel kişilikler** sekmesinde, dışarı aktardığınız tüzel kimliği belirtmek için şu adımları izleyin:

    1. **Yeni**'yi seçin.
    2. **Kaynak tüzel kişilik** alanına tüzel kişiliği girin.

        Aynı ölçütler aynı veritabanında bulunan birkaç yan kuruluş için de geçerliyse, dosyaları dışarı aktarmayı tek bir işlemde ayırmak için bu yan kuruluşlardan veri aktarabilirsiniz:

        1. Dosyalara dışarı aktarılması gereken her yan kuruluş tüzel kişiliği için bir satır oluşturun. Bu dosyalar daha sonra konsolide edilen tüzel kişiliğe içe aktarılır.
        2. Her bağlı şirket için bağlı şirket adını ve dışa aktarma işi sırasında oluşturulacak dışa aktarma dosyasının adını girin.

    3. **Dönüştürme farkları için hesap türü** alanında, **Kar ve zarar**'ı veya **Bilanço**'yu seçin.
    4. Oluşturulacak dışarı aktarma dosyası için bir dosya adı girin.

5. Dışarı aktarmayı çalıştırmak için **Tamam**'ı seçin.

Dışa aktarma işlemi tamamlandığında, her dosyaya kaydedilen kayıt sayısını gösteren bir ileti alırsınız. Artık dosyaları konsolide tüzel kişilikteki dosyalara içe aktarabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]