---
title: Kamyon yükünden az (LTL) sınıfları
description: Bu makale, kamyon yükünden az (LTL) sınıflarının ne olduğunu açıklar ve Microsoft Dynamics 365 Supply Chain Management'ta bunların nasıl ayarlanacağını açıklar .
author: Weijiesa
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9ab05e1bc5d0ae2c8b5d98dda32660d2436676e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857213"
---
# <a name="less-than-truckload-ltl-classes"></a>Kamyon yükünden az (LTL) sınıfları

[!include [banner](../includes/banner.md)]

Kamyon yükünden az (LTL) sınıfı, sevk edilebilecek maddeleri sınıflandırmak için kullanılan bir navlun sevkiyat sınıfıdır. Genellikle, her ürün veya emtia türü, LTL sevkiyatları için belirli bir navlun sınıfı numarasına karşılık gelen bir Ulusal Motorlu Navlun Sınıflandırması (NMFC) koduna sahiptir. LTL navlun sınıfları maddelerin kategorilerini temsil ederken, NMFC kodları 18 navlun sınıfındaki belirli emtialarla ilgilidir.

Bu özellik, sisteminizi kullanarak aşağıdaki görevleri yerine getirmenizi sağlar:

- Şirketinizde kullanılan LTL navlun sınıflarını tanımlayın.
- Her LTL sınıfını **NMFC kodları** sayfasındaki bir NMFC koduna atayın. Daha fazla bilgi için bkz. [Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları](nmfc-codes.md).
- **Ürünler** sayfasındaki her ürüne bir NMFC kodu (ve böylece ilişkilendirilmiş LTL kodu) atayın.
- Bir NMFC kodunun atandığı her ürünün LTL sınıfını doğru şekilde değerlendirin.
- Uluslararası LTL standartlarını denetleyerek her LTL sınıfı için ambalaj gereksinimlerini belirleyin. Bu şekilde, ürünlerinizin iyi korunması ve güvenle sevk edilmesini güvence altına alırsınız.
- Her bir ürün için LTL navlun sınıfına göre doğru sevkiyat tahminleri elde edin.

Bu makalede, Microsoft Dynamics 365 Supply Chain Management'ta LTL sınıfları oluşturma yöntemi açıklanmıştır.

## <a name="create-an-ltl-class"></a>LTL sınıfı oluşturma

LTL sınıfı oluşturmak için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **Ambar yönetimi \> Kurulum \> Stok \> LTL sınıfları** seçeneğine gidin.
    - **Taşımacılık yönetimi \> Kurulum \> Taşıma standartları \> LTL sınıfları** seçeneğine gidin.

2. Eylem bölmesinde, bir LTL sınıfı oluşturmak için **Yeni**'yi seçin. Ardından aşağıdaki alanları ayarlayın:

    - **LTL sınıfı** – Şirketinizin emtia türü için dahili LTL sınıf tanımlayıcısını (ID) girin. Birçok şirket uluslararası standardı kullanır. Bu durumda, bu alanın değeri **Sınıf** alanındaki değerle eşleşecektir . Ancak, şirketiniz kendi standardını kullanıyorsa, o standarda uyan bir kod girin.
    - **Ad** – Her bir NMFC kodu için doğru LTL sınıfını seçme konusunda size ve diğer kullanıcılara yardımcı olacak açıklayıcı bir ad girin.
    - **Sınıf** – Emtia türü için uluslararası standart LTL sınıf kodunu girin. Buraya gireceğiniz kod, resmi standarda uygun olmalıdır.

## <a name="example-set-up-ltl-classes"></a>Örnek: LTL sınıflarını ayarlama

Aşağıdaki örnekte, farklı ürün türleriyle kullanabileceğiniz iki farklı LTL sınıfının nasıl ayarlanacağı gösterilmektedir.

1. **Ambar yönetimi \> Kurulum \> Stok \> LTL sınıfları** seçeneğine gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **LTL sınıfı:** *92.5*
    - **Ad:** *Bilgisayarlar, monitörler, soğutucular*
    - **Sınıf:** *92.5*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **LTL sınıfı:** *125*
    - **Ad:** *Küçük ev aletleri*
    - **Sınıf:** *125*

1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Ulusal Motorlu Navlun Sınıflandırması (NMFC) kodları](nmfc-codes.md)
- [Konşimento oluşturma](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
