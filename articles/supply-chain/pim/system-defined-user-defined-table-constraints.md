---
title: Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları
description: Bu makalede, kullanıcı tanımlı ve sistem tanımlı olmak üzere, bir ürün yapılandırma modelindeki bileşenler için iki tablo sınırlandırma türü açıklanmaktadır. Tablo sınırlandırmaları, her bir satırın bir pozitif öznitelik değeri setine karşılık geldiği, izin verilen öznitelik kombinasyonlarının matrislerini temsil eder.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4b484c99bc8f1cc830d4177460ec15a26714a56
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577396"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları

[!include [banner](../includes/banner.md)]

Bu makalede, kullanıcı tanımlı ve sistem tanımlı olmak üzere, bir ürün yapılandırma modelindeki bileşenler için iki tablo sınırlandırma türü açıklanmaktadır. Tablo sınırlandırmaları, her bir satırın bir pozitif öznitelik değeri setine karşılık geldiği, izin verilen öznitelik kombinasyonlarının matrislerini temsil eder.

Tablo kısıtlamaları, ürün yapılandırma modelindeki bileşenler için izin verilen özniteliklerin birleşimlerinin matrislerini temsil eder. Tablodaki her satır bir dizi olası öznitelik değerini tanımlar. Ürün yapılandırma modelindeki kısıtlamaları iki türde bildirebilirsiniz:

-   **İfade kısıtlaması** – Ürün yapılandırması sırasında yalnızca uyumlu değerlerin seçilebileceğini güvence altına almak için öznitelikler arasındaki ilişkileri tanımlayan bir ifade oluşturun.
-   **Tablo kısıtlaması** – Belirtilen öznitelikler kümesi için izin verilen tüm kombinasyonları tanımlayan bir tablo oluşturun. İki türde tablo kısıtlaması vardır: Kullanıcı tanımlı tablo kısıtlamaları ve sistem tanımlı tablo kısıtlamaları.

Bu makalede, ürün yapılandırma modelinde bileşenler için kullanıcı tanımlı ve sistem tanımlı tablo kısıtlamaları açıklanmaktadır.

## <a name="user-defined-table-constraints"></a>Kullanıcı tanımlı tablo kısıtlamaları
Kullanıcı tanımlı bir tablo kısıtlaması öznitelik türleri tarafından tanımlanan öznitelik değerlerinin bir dizi kombinasyonunu tanımlamak için kullanılan bir matris türüdür. Örneğin, hoparlör üretiyorsanız kullanıcı tanımlı tablo kısıtlamasında kabin rengi ve ızgara rengi için sütunlar ekleyebilirsiniz. Kabin renginin öznitelik türünde dört; ızgara renginin öznitelik türünde üç değer vardır. Bu nedenle, kısıtlamalar kullanılmazsa 4 × 3 = 12 olası kombinasyon oluşur. Ancak, bu örnekte aşağıdaki tabloda gösterildiği şekilde yalnızca altı kombinasyona izin verilir. Bu bilgiler **Tablo kısıtlamasını düzenle** sayfasında **İzin verilen kombinasyonlar** sekmesinde görüntülenir.

| Kabin rengi | Izgara rengi |
|----------------|-------------|
| Siyah          | Siyah       |
| Siyah          | Metal       |
| Meşe            | Siyah       |
| Pelesenk       | Beyaz       |
| Beyaz          | Siyah       |
| Beyaz          | Beyaz       |

Kullanıcı tanımlı tablo kısıtlamaları ifade kısıtlamasıyla aynı şekilde işleyen statik tablo girişiyle tanımlanır. Kullanıcı tanımlı bir tablo kısıtlaması kullandığınızda tabloları oluşturmanın, anlamanın ve sağlamanın genellikle uzun ifade kısıtlamalarından daha kolay olması bir avantaj sağlar.

## <a name="system-defined-table-constraints"></a>Sistem tanımlı tablo kısıtlamaları
Sistem tanımlı bir tablo kısıtlaması, bir tablodaki öznitelik türü ile alan arasındaki dinamik eşlemeyi temsil eder. Sistem tanımlı bir tablo kısıtlaması bir ürün yapılandırma modeline dahil edildiğinde, öznitelik türü değerlerinin yerine tablodaki verileri güvence altına alan eşleme gösterilir. Tablo içeriği değiştirilebileceğinden (örneğin, diğer modüller tarafından) sonuçta dinamik bir kısıtlama ortaya çıkar.  

Sistem tanımlı bir tablo kısıtlaması oluşturduğunuzda, bir tablo seçer, isteğe bağlı olarak kullanmak istediğiniz sorguyu tanımlar ve ardından seçilen tablodaki alanlarla öznitelik türlerini ilişkilendirirsiniz. Alanların türleri öznitelik türlerinin türleriyle eşleşmelidir.  

Bir ürün yapılandırma modeline bir tablo kısıtlaması getirilebilmesi için, tablo kısıtlamasının model bileşenlerinden birindeki kısıtlamaya dahil edilmesi gerekir. Yeni kısıtlama oluşturmak için prosedür, tablo kısıtlaması türünün seçilmesi ve ardından kullanılacak tablo kısıtlaması tanımının seçilmesidir. Son olarak, tablo kısıtlamasındaki tüm alanlar ürün yapılandırma modelindeki özniteliklerle eşlenmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün yapılandırma modellerine genel bakış](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]