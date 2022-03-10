---
title: Uygunsuzluk işlemleri giderleri
description: Bu konu, uyumsuzlukla ilgili işlemlerle kullanılabilecek kalite masraflarının nasıl oluşturulacağını açıklamaktadır.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3306f3f9215ab03f408b8026f335dcf496515a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580972"
---
# <a name="charges-for-nonconformance-operations"></a>Uygunsuzluk işlemleri giderleri

[!include [banner](../includes/banner.md)]

Bu konu, uyumsuzlukla ilgili işlemlerle kullanılabilecek kalite masraflarının nasıl oluşturulacağını açıklamaktadır.

**Kalite giderleri** sayfasını, uygunsuzluklar ile ilgili işlemlerine eklenebilecek giderlerin türlerini tanımlamak için kullanırsınız. Giderler, uygunsuz ürünlerle ilgili olarak müşteriye borçlu olduğunuz ücretler veya giderlerle ilgili ayrıntıları izlemenize veya bir satıcının aldığınız uygunsuz ürünler için size olan borcuyla ilgili ayrıntıları izlemenize olanak tanır. Ayrıca giderleri, harici satıcılar veya servisler için gereken maliyetleri izlemek için de kullanabilirsiniz.

## <a name="examples-of-quality-charges"></a>Kalite gideri örnekleri

Bir üretim şirketi için çalışırsınız. Şirketinizin birkaç satıcıyla sözleşmesi vardır. Bu sözleşmeler, maddelere ait zamanında sevkiyat, zararlar ve ürün kalitesiyle ilgili standartların ana hatlarını belirler. Benzer şekilde, müşterilerinizin bazıları iadeler, zararlarla ve ürün kalitesiyle ilgili olarak şirketinizle sözleşmeleri vardır.

Her bir koşul için bir ücret yapısı belirlenir ve sözleşmede belirlenir. *Zararlar*, *Geç sevkiyat* ve *Kalite* gibi çeşitli türde giderleri ana hatlarıyla ortaya koymak için kalite ücretlerini yapılandırabilirsiniz. Daha sonra, uygunsuzluk oluşturduğunuzda bir veya daha fazla işlem eklersiniz. Her işlem için, ücretler hakkındaki ayrıntıları tanımlamak üzere **Giderler**'i seçersiniz.

## <a name="create-a-quality-charge"></a>Kalite gideri oluşturma

1. **Stok yönetimi \> Kurulum \> Kalite yönetimi \> Kalite giderleri** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Gider kodu** – Kalite gideri için benzersiz bir kod ya da ad girin.
    - **Açıklama** – Kalite giderinin detaylı bir açıklamasını girin.

1. Sayfayı kapatın.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Uygunsuzluk için işlem kalite gideri ekleme

Uygunsuzluklara işlem ekleme ve bunlara ücret uygulama hakkında ayrıntılar için bkz. [Uygunsuzluklar için işlemler](quality-operations.md).

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Uygunsuzlukları onaylamaktan sorumlu çalışanlar](quality-responsible-workers.md)
- [Uygunsuzluklar için karantina bölgeleri](quality-quarantine-zones.md)
- [Uygunsuzluklar için tanılama türleri](quality-diagnostic-types.md)
- [Uygunsuzluklar için kalite masrafları](quality-charges.md)
- [Uygunsuzluklar için işlemler](quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
