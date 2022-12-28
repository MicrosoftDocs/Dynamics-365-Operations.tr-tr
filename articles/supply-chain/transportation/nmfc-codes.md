---
title: Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management'ta Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodlarıyla nasıl çalışılacağı açıklanmaktadır
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c173057b8e1357790e780469c5806afb857be62a
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838348"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları

[!include [banner](../includes/banner.md)]

Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları, sevk edilebilecek maddeleri sınıflandırmanıza yardımcı olur. NMFC kodu, emtiaları gruplamak için kullanılan bir atamadır. Taşıma şirketlerinin, kamyonu alanı, yükleme sorunları, işleme sorunları ve bozulabilirlik gibi konulara göre maddeleri sınıflandırarak sevk edilecek malları değerlendirmesini sağlar. Emtialar, 50 ile 500 arasında bir sayı aralığı kullanılarak 18 navlun sınıfından biri olarak gruplandırılır. Bir emtianın gruplandırıldığı sınıf, dört taşıma özelliği değerlendirmesine dayanır: yoğunluk, stoklanabilirlik, idare ve yükümlülük. Birlikte, bu özellikler emtianın taşınabilirliğini oluşturur.

NMFC kodu, tüm kamyon yükünden az (LTL) sevk maddesiyle ilişkilendirilir. Örneğin, bir dizüstü bilgisayara 2,5 olarak sınıflandırılmış bir NMFC atanırken elektrik kablolarına 65 olarak sınıflandırılmış bir NMFC atanabilir.

Bu özellik, çalışanların LTL sevkiyat maddelerini sınıflandırmak için NMFC kodlarını kullanmasına yardımcı olabilir. Burada bazı örnekler verilmiştir:

- Şirketinizde konşimento (BOL) üzerinde bir navlun açıklaması varsa, taşıyıcının navlunun ne olduğuna dair bir fikri olacaktır. Birçok taşımacılık şirketi, iş modellerini sevk edilen navlun türlerine dayandırdığı için navlun önemli bir sınıflandırmadır.
- Belirli bir yükün maliyetini belirlemek için kullanıldığından, bu sınıflandırma şirketiniz için gerekli olabilir.
- Şirketiniz, bir LTL lojistik ve taşımacılık şirketinin karlılığını tanımlayabilir.

Bu makalede, Microsoft Dynamics 365 Supply Chain Management'ta NMFC kodlarıyla nasıl çalışılacağı açıklanmaktadır.

## <a name="prerequisites"></a>Ön Koşullar

NMFC kodlarını oluşturabilmeniz için önce kendileriyle eşleştirilmesi gereken tüm LTL navlun sınıflarını ayarlamanız gerekir. LTL navlun sınıfları maddelerin kategorilerini temsil ederken, NMFC kodları 18 navlun sınıfındaki belirli emtialarla ilgilidir. LTL sınıflarıyla nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Kamyon yükünden az (LTL) sınıfları](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Bir NMFC kodu oluşturma

Bir NMFC kodu oluşturmak için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **Ambar yönetimi \> Kurulum \> Stok \> NMFC kodları** seçeneğine gidin.
    - **Taşımacılık yönetimi \> Kurulum \> Taşıma standartları \> NMFC kodları** seçeneğine gidin.

1. Bir NMFC kodu oluşturmak için **Yeni**'yi seçin. Ardından aşağıdaki alanları ayarlayın:

    - **NMFC kodu** – Emtia türü için NMFC kodunu girin.
    - **Ad** – NMFC kodu için bir ad girin.
    - **LTL sınıfı** – NMFC koduyla ilişkilendirilmiş LTL sınıfını seçin.
    - **BOL işleme birimi** – Sevkiyatın varsayılan işleme türünü tanımlayın.

## <a name="example-set-up-nmfc-codes"></a>Örnek: NMFC kodlarını ayarlama

Aşağıdaki örnekte, farklı ürünlerle kullanabileceğiniz iki farklı NMFC kodunun nasıl ayarlanacağı gösterilmektedir.

1. **Warehouse Management \> Kurulum \> Stok \> NMFC kodları** veya **Nakliye yönetimi \> Kurulum \> Nakliye standartları \> NMFC kodlarına** gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **NMFC kodu:** *92.5*
    - **Ad:** *Bilgisayarlar*
    - **LTL sınıfı:** *92.5*
    - **BOL işleme birimi:** *Birim*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **NMFC kodu:** *125*
    - **Ad:** *Telefonlar*
    - **LTL sınıfı:** *125*
    - **BOL işleme birimi:** *Birim*

1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kamyon yükünden az (LTL) sınıfları](ltl-class.md)
- [Konşimento oluşturma](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
