---
title: Attract'te işe alım süreci şablonu oluşturma
description: Bu konu, Attract'te işe alım süreci şablonu oluşturma hakkında bilgi sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462871"
---
# <a name="create-a-hiring-process-template-in-attract"></a>Attract'te işe alım süreci şablonu oluşturma

[!include [banner](includes/banner.md)]

*İşe alma işlem şablonu*, bir işin işe alma işleminin parçası olarak dahil edilmesi gereken tüm faaliyetleri içerir. Bu konuda Microsoft Dynamics 365 Talent: Attract'teki bir işlem şablonunun öğeleri açıklanmaktadır. Bu aynı zamanda bir şablon oluşturmayı açıklar.

> [!NOTE]
> Şablon oluşturma Attract için Kapsamlı İşe Alım eklentisinin parçasıdır.

## <a name="template-management"></a>Şablon yönetimi

Kurumlar, Attract'te ekip üyelerinin veya yalnızca yöneticilerin süreç şablonları oluşturmasını belirler. Şablon yönetimi yapılandırmak için **Yönetici Merkezi**\>**Şablon yönetimi**'ne gidin. Ekip üyelerinin kendi şablonlarını oluşturmasına izin vermek için şablon yönetimini etkinleştirin. Şablon yönetimini etkinleştirmiyorsanız, yalnızca yöneticiler şablonları oluşturabilir.

## <a name="default-template"></a>Varsayılan şablon

Yalnızca yöneticiler varsayılan şablonu ayarlayabilir. Bir iş oluşturulduğunda şablon işaretli değilse varsayılan şablon kullanılır. Varsayılan şablonu ayarlamak için **Yönetici Merkezi** \> **Şablon yönetimi**'ne gidin. Varsayılan şablon olması gereken şablonla ilgili karttaki üç nokta düğmesini (**...**) seçin ve daha sonra **Varsayılan olarak ayarla**'yı seçin.

## <a name="create-a-process-template"></a>Süreç şablonu oluştur

Yöneticiler, işe alanlar ve işe alma müdürleri süreç şablonları oluşturabilir. Süreç şablonu, *aşamalar* ve *faaliyetlerden* oluşur. Aşamalar, bir veya birkaç faaliyeti gruplandırır. Varsayılan olarak, her işlem şablonu Aday müşteri, Başvuru ve Teklif faaliyetlerine sahiptir. Bu etkinlikleri içeren aşamalar yeniden adlandırılabilir. **+ Yeni Aşama**'yı seçerek daha fazla aşama ekleyebilirsiniz. Faaliyetleri uygun aşaamaya sürükleyerek veya faaliyet listesinde çift tıklayarak bir aşamaya ekleyebilirsiniz.

> [!NOTE]
> Aşama adları **Başvuru durumu** sayfasında adaylara görünür. Bu özelliği, aşamaları için adları seçtiğinizde dikkate almanız gerekir.

Faaliyetler hakkında daha fazla bilgi için bkz. [İşe alım süreçlerindeki faaliyetler](./activities-attract.md).

İşe alma süreç şablonu oluşturmak için şu adımları izleyin.

1. **Şablonlar**'a gidin.
2. **Yeni**'yi seçin.
3. **Şablon adı** alanında, şablon için bir ad girin ve sonra **Oluştur**'u seçin.
4. **Onay sürecini seç** listesinde bir iş için onay gerektirmek üzere **Varsayılan**'ı seçin.
5. Aday müşterileri etkinleştirme veya devre dışı bırakmak için seçin.
6. İsteğe bağlı: Aşama ekleyin veya kaldırın.

    - Aşama eklemek için **+ Yeni aşama** yı seçin.
    - Aşama kaldırmak için aşama üzerine imleci getirin ve görünen çöp kutusu düğmesini seçin.

        > [!NOTE]
        > Aday, Başvuru ve Teklif aşamaları kaldırılamaz ancak yeniden adlandırılabilir.

7. İsteğe bağlı: Faaliyet ekleyin veya kaldırın.

    - Faaliyet eklemek için sağdaki faaliyet listesinden uygun aşamaya sürükleyin. Alternatif olarak, faaliyete çift tıklatın ve eklemek için aşamayı seçin.
    - Faaliyeti kaldırmak için, genişletin ve faaliyet üst bilgisindeki çöp kutusu düğmesini seçin.

8. **Kaydet**'i seçin.
