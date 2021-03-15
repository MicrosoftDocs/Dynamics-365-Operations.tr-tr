---
title: Hata yönetimi
description: Bu konuda Varlık Yönetimi'ndeki varlık yönetiminde açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 176fbebcf88e7557bf2bafc56524cd2ec015220e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020976"
---
# <a name="fault-management"></a>Hata yönetimi

[!include [banner](../../includes/banner.md)]

 

Kıymet yönetiminde, arıza belirtileri, arıza alanları ve kıymet türlerinde arıza türleri ayarlamak için hata tasarımcısını kullanabilirsiniz. Bu şekilde, kıymetler üzerinde algılanan hataları yönetebilirsiniz. Ayrıca, hataları düzeltmek için hata nedenleri ve öneriler bir iş siparişine kaydedilebilir.

Hata kayıt ve yönetim işlemi aşağıdaki adımlardan oluşur.

1. Kıymet türleriniz üzerinde oluşabilecek hata belirtileri, arıza alanları ve arıza türleri listesi oluşturun.
2. Arıza Tasarımcısında, belirtiler, arıza alanları ve arıza türlerini ayarlayın.

Hata belirtileri, arıza alanları ve arıza türleri arasındaki farkı anlamanıza yardımcı olacak bazı örnekler aşağıda verilmektedir.

**Hata belirtileri:**

- Dengesiz voltajlar
- Kısa devre
- Gürültü
- Sızıntı
- Titreşimler

**Hata alanları:**

- Elektrik
- Mekanik
- Hidrolik
- Pnömatik

**Hata türleri:**

- Arızalı ana stator sargısı
- Hatalı diyot
- Kirli sargılar
- Kusurlu oluşturucu
- Kusurlu algılayıcı

## <a name="create-fault-symptoms"></a>Hata belirtileri oluştur

Hata tasarımcısında kullanılabilecek belirtilerin listesini oluşturmak için bu adımları izleyin.

1. **Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata semptomları**'nı seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. **Hata semptomları** alanına hata semptomu adı girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Kaydet**'i seçin.

## <a name="create-fault-areas"></a>Hata alanları oluştur

Hata tasarımcısında kullanılabilecek alanların veya konumların listesini oluşturmak için bu adımları izleyin.

1. **Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata alanları**'nı seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. **Hata alanları** alanına hata alanı adı girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Kaydet**'i seçin.

## <a name="create-fault-types"></a>Hata türleri oluştur

Hata tasarımcısında kullanılabilecek hata türlerinin listesini oluşturmak için bu adımları izleyin.

1. **Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata türleri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. **Hata Türü** alanına hata türü için bir ad girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Kaydet**'i seçin.

## <a name="set-up-the-fault-designer"></a>Hata tasarımcısını ayarla

Hata tasarımcısında, kıymet türlerinde hata verileri ayarlarsınız.

1. **Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata tasarımcısı**'nı seçin.
2. Sol bölmede, bir hata kaydı kurmak üzere kullanılacak kıymetin türünü seçin.
3. **Hata semptomu** hızlı sekmesinde **Satır ekle**'yi seçin ve **Hata semptomu** alanında bir hata semptomu seçin.
4. **Hata alanı** hızlı sekmesinde **Satır ekle**'yi seçin ve **Hata alanı** alanında bir hata alanı seçin.
5. **Hata türü** hızlı sekmesinde **Satır ekle**'yi seçin ve **Hata türü** alanında bir hata türü seçin.
6. Seçili varlık türü için varolan tüm hata semptomları, alanlar ve türlerin birleşimlerini hızlı bir şekilde oluşturmak için **Hata birleşimleri oluştur**'u seçin. Birçok hata semptomu, alanı ve türü eklediyseniz bu işlev yararlıdır. Kıymet türüyle alakalı olmayan herhangi bir kombinasyon için satırları silmek, el ile yeni satırlar oluşturmaktan daha kolaydır.

    > [!NOTE]
    > Bir kıymet türündeki hata semptomları, alanlar ve türlerin kurulumunu seçili kıymet türüne kopyalamak için **Sabit kıymet türünden kopyala**'yı seçin.

7. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.

![Arıza tasarımcısı sayfası](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Hata nedenleri oluştur

Bir iş emrine veya bakım isteğine eklenebilen bilinen hata nedenlerinin bir listesini oluşturmak için bu adımları izleyin.

1. **Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata nedenleri**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. **Hata nedeni** alanına hata nedeni için bir ad girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Kaydet**'i seçin.

## <a name="create-fault-remedies"></a>Hata düzeltici oluştur

Bir iş emrine veya bakım isteğine eklenebilen düzeltici ve onarım önerilerinin bir listesini oluşturmak için bu adımları izleyin.

1. **Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata düzelticisi**'ni seçin.
2. Bir kayıt oluşturmak için **Yeni**'yi seçin.
3. **Hata düzeltici** alanına hata düzeltici adı girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Kaydet**'i seçin.

> [!NOTE]
> Hata semptomlarınızın adlarını, alanlarını, türlerini, nedenlerini ve gereksinim duyduğunuz değişiklikleri değiştirebilirsiniz. Ad değişiklikleri otomatik olarak ilgili hata kayıtlarında yansıtılır.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]