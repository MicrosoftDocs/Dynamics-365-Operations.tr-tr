---
title: Tehlikeli maddeler
description: Bu konu, ortamınızda depolanan tehlikeli madde belge ve bilgileri hakkında bilgi sağlamaktadır.
author: lachlancashMS
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: bda81f72d5dea24c7ba678b9a86258a02f7b8cd5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829438"
---
# <a name="hazardous-materials"></a>Tehlikeli maddeler

[!include [banner](../includes/banner.md)]

Tehlikeli maddeler hakkındaki bilgiler Ürün bilgileri yönetimi'nde ayarlanır. Bu modül, ambar yönetimiyle yazdırılabilen belgeleri de sağlar.

Tehlikeli mal olarak sınıflandırılmış malzemeler sevk ediyorsanız, sevkiyata ek resmi belgeler de dahil edilmesi gerekir. Tehlikeli maddeler işlevselliği, müşterilerin sınıflandırma bilgilerini depolamasına ve serbest bırakma kalemleriyle ilişkilendirmesine olanak sağlar. Bu bilgiler daha sonra sevkiyat belgelerinin hazırlanmasına yardımcı olarak kullanılabilir.

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Management'taki tehlikeli malzeme özellikleri, tehlikeli ürünlerinizle ilgili bilgileri kaydetmenize ve bu bilgilere başvurmanıza yardımcı olabilecek kullanışlı ürün bilgisi alanları ve ilgili işlevler koleksiyonu sağlar. Bu özellikler, sevk ettiğiniz tehlikeli malzemeler hakkındaki bilgilerin aynısını içeren sevkiyat belgelerini tasarlamanıza ve yazdırmanıza yardımcı olur. Ancak, sistem ülkenizdeki veya bölgenizdeki geçerli tüm yönetmeliklerle otomatik olarak uyumlu hale gelmez. Bu araçlar ortak yönetmeliklere uymanıza yardımcı olacak şekilde tasarlanmış olsa da kendi başlarına yeterli değillerdir ve bununla ilgili bir garanti sunulmaz. Geçerli tüm yönetmelikleri bilmek ve bunlara uymak için gerekli tüm adımları atmaktan kuruluşunuz sorumludur.

Bu işlevi kullanabilmeniz için aşağıdaki kurulum gereklidir:

- **Ürün bilgileri yönetimi:** Serbest bırakılan ürünlere uygulanabilecek kodları ayarlayın.
- **Ambar yönetimi:** Sevkiyat bilgilerini yazdırmak için ek sevkiyat belgeleri kullanın.

## <a name="product-information-management"></a>Ürün bilgileri yönetimi

Ürün bilgileri yönetimi'nde, kara, hava ve deniz yoluyla taşıma için tehlikeli mal listelerinde sağlanan referans bilgilerini ekleyebileceğiniz bir dizi kurulum tablosu vardır.

Sıklıkla başvurulan düzenlemelerden bazıları şunlardır:

- **ADR** – Tehlikeli malların uluslararası karayollarında taşınmasıyla ilgili düzenlemeler
- **CFR 49** – ABD'de tehlikeli malların taşınmasına yönelik düzenlemeler
- **IMDG** – Uluslararası Denizcilik Tehlikeli Maddeler (IMDG) kodu
- **IATA** – Uluslararası Hava Taşımacılığı Birliği (IATA) tehlikeli mal düzenlemeleri

Bu düzenlemelerin her biri, referans kodları içeren bir tehlikeli mallar listesi içerir. Her bir taşıma türünün listeleri, paylaşılan uluslararası sınıflandırmalarda birleştirilir. Supply Chain Management, bu listelerdeki paylaşılan kodlar için bir başvuru tablosu sağlar. Her listede, tanımlanabilecek bazı benzersiz kodlar da vardır.

Bu bilgileri yapılandırmaya başlamak için ilk parametreleri yapılandırmada kullanabileceğiniz bir düzenleme oluşturun.

## <a name="warehouse-management"></a>Ambar yönetimi

Bir sevkiyat hazırlanırken çeşitli yeni raporlar yazdırılabilir. Bu raporlar, Ürün bilgileri yönetimi'nde ayarladığınız bilgileri kullanır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]