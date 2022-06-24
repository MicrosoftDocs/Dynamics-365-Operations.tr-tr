---
title: Sevkiyat bilgileri kurulumu
description: Bu makalede, Varış yeri maliyeti modülü için sevkiyat bilgilerinin nasıl ayarlanacağı açıklanmaktadır.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 62277f66a36817e83b4c0bf101aa7b6cc14ecccb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882648"
---
# <a name="shipping-information-setup"></a>Sevkiyat bilgileri kurulumu

[!include [banner](../../includes/banner.md)]

Bu makalede, **Varış yeri maliyeti** modülü için sevkiyat bilgilerinin nasıl ayarlanacağı açıklanmaktadır.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Malların açıklaması

Malların açıklamaları bir seyahatin, sevkiyat konteynerinin veya mal folyosunun ve içinde bulunan malların tanımlanmasına yardımcı olur. Sevkiyat konteyneri başlığında veya folyo başlığında malların açıklamasını seçebilirsiniz.

Malların açıklamalarıyla çalışmak için, **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Malların açıklaması**'na gidin. Burada, malların açıklamaları için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Malların açıklaması | Bu açıklamayı kullanacak mal türü için benzersiz bir kimlik adı/numarası girin. |
| Tanım | Bu kategorideki malların türünün açıklamasını girin. |

## <a name="vessels"></a><a name="vessels"></a>Tekneler

Gemi, bir sevkiyat şirketinin veya acentesinin kullandığı bir geminin benzersiz adıdır. Bir seyahat oluşturduğunuzda, her zaman bunun için bir gemi seçmeli veya girmelisiniz. Sık sık aynı gemileri kullanıyorsanız her biri için bir gemi kaydı oluşturarak yeni bir seyahat oluşturmayı daha hızlı ve kolay hale getirebilirsiniz; böylece kullanıcıların her seferinde adı veya numarayı el ile girmeleri yerine gemiyi bir listeden seçmelerini sağlayabilirsiniz.

Gemilerle çalışmak için, **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Gemiler**'e gidin. Burada, gemiler için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Tekne | Bir seyahatte mal taşımak için kullanılacak gemi için benzersiz bir kimlik adı/numarası girin. |
| Tanım | Gemi için açıklama girin. Genellikle, bu açıklama geminin ve sevkiyat şirketinin/acentesinin adını tanımlar. |
| Teslimat şekli | Geminin kullandığı teslimat modunu seçin _(Hava yolu_, _Deniz yolu_ veya _Demir yolu_ gibi). |

## <a name="exporters"></a>İhracatçılar

Her ihracatçı kaydı, bir seyahat için satıcı olarak tanımlanabilecek bir satıcı veya ihracatçı tanımlar. İhracatçı bir seyahatle ilişkilendirilebilir ve raporlama için kullanılabilir.

İhracatçılarla çalışmak için **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Gemiler**'e gidin. Burada, ihracatçılar için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| İhracatçı | Bir seyahatte taşınan malların ihracatçısı için benzersiz bir kimlik adı/numarası girin. |
| Tanım | İhracatçı için açıklama girin. Genellikle, bu açıklama sevkiyat şirketinin/acentesinin tam adını tanımlar. |

## <a name="commodity-codes"></a>Emtia kodları

Gümrük tanımlamasına ve bir seyahatteki mallar için vergi oranlarının hesaplanmasına yardımcı olmak için emtia kodlarını kullanırsınız. Emtia kodlarını **Serbest bırakılan ürünler** sayfasından seçebilirsiniz.

Emtia kodlarıyla çalışmak için **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Emtia kodları**'na gidin. Burada, emtia kodları için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Emtia kodu | Bu tür emtialar için benzersiz bir kod girin. |
| Tanım | Emtia türü için açıklama girin. |

## <a name="customs-description"></a>Gümrük açıklaması

Gümrük açıklamaları, gümrük amacıyla malların tanımlanmasına yardımcı olur. **Serbest bırakılan ürünler** sayfasında veya satın alma siparişi satırlarında bir gümrük açıklaması seçebilirsiniz.

Gümrük açıklamalarıyla çalışmak için **Varış yeri maliyeti \> Sevkiyat bilgileri kurulumu \> Gümrük açıklaması**'na gidin. Burada, gümrük açıklamaları için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Gümrük açıklaması | Bu tür gümrük sınıflandırması için benzersiz bir kod girin. Genellikle, bu kod malların tanımı ve nitel değeri için bir gümrük idaresi tarafından sağlanan resmi açıklama olur. |
| Tanım | Gümrük sınıflandırması için açıklama girin. |
