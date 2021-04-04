---
title: Sevkiyat konteynerleri
description: Bu konuda, Varış yeri maliyeti modülü için sevkiyat konteynerlerinin nasıl ayarlanacağı açıklanmaktadır.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500970"
---
# <a name="shipping-container-setup"></a>Sevkiyat konteyneri kurulumu

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, **Varış yeri maliyeti** modülü için sevkiyat konteynerlerinin nasıl ayarlanacağı açıklanmaktadır.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Sevkiyat konteyneri türlerini ayarlama

Sevkiyat konteyneri türleri, sevkiyat ve seyahat sırasında kullanılabilen sevkiyat konteyneri türlerini tanımlar.

Sevkiyat konteyneri türleriyle çalışmak için **Varış yeri maliyeti \> Konteyner kurulumu \> Sevkiyat konteyneri türleri**'ne gidin. Burada, konteyner türlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Sevkiyat konteyneri türü | Sevkiyat konteyneri türü için benzersiz bir tanımlama adı/numarası girin. |
| Tanım | Sevkiyat konteyneri türü için açıklama girin. |
| Hacim | Bu tür sevkiyat konteynerlerinde izin verilen maksimum hacmi girin. |
| Ağırlık | Bu tür nakliye konteynerlerinde izin verilen maksimum ağırlığı girin. |
| İade edilebilir | Bu tür sevkiyat konteynerlerinin bir seyahat sırasında kullanıldıktan sonra satıcıya iade edilip edilmeyeceğini belirtin. Bu seçenek *Evet* olarak ayarlanırsa bu tür sevkiyat konteynerlerinin çıkış limanına iadesi için ek maliyetler uygulanabilir. |

## <a name="set-up-shipping-containers"></a>Sevkiyat konteynerlerini ayarlama

Seyahatler sırasında kullandığınız her konteyneri tanımlamak için sevkiyat konteyneri kayıtlarını kullanırsınız. Bir seyahat oluşturduğunuzda, burada tanımladığınız tüm sevkiyat konteyneri kayıtları listesinde bunun için belirli bir konteyner seçebilirsiniz. Bu özellik özellikle şirketiniz kendi sevkiyat konteynerlerine sahipse kullanışlıdır.

Yalnızca bir kez kullanılacak sevkiyat konteynerleri için sevkiyat konteyneri numaraları girmeniz gerekmemektedir. Bunun yerine, bir seyahat oluşturduğunuzda sevkiyat konteyneri numarası ekleyebilirsiniz.

Sevkiyat konteyneri kayıtları yalnızca Varış yeri maliyetinde kullanılır. Bunlar standart **Taşıma yönetimi** modülünde (TMS) mevcut değildir.

Sevkiyat konteynerleriyle çalışmak için **Varış yeri maliyeti \> Konteynerleri ayarlama \> Sevkiyat konteynerleri**'ne gidin. Burada, sevkiyat konteynerlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Sevkiyat konteyneri | Sevkiyat konteyneri için benzersiz bir tanımlama adı/numarası girin. |
| Sevkiyat konteyneri türü | Sevkiyat konteyneri türünü seçin. Daha fazla bilgi için bu konuda daha önce ele alınan [Sevkiyat konteyneri türlerini ayarlama](#shipping-container-types) bölümüne bakın. |

> [!NOTE]
> - Sevkiyat konteyneri kurulumu isteğe bağlıdır. Genellikle, yalnızca şirketiniz kendi sevkiyat konteynerlerine sahipse veya genellikle aynı sevkiyat konteynerlerini yeniden kullanıyorsa kullanırsınız.
> - Sevkiyat konteyneri numaraları için hiçbir denetleme basamağı hesaplanmaz.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Birim türlerini ayarlama

Birim türleri, sevkiyat konteynerleri için ek gruplandırmalar ve tanımlama yöntemleri oluşturur. Birim türü genellikle paletler veya variller gibi malların paketli olduğu konteyner türünü tanımlamak için kullanılır. **Tüm sevkiyat konteynerleri** sayfasında bir konteyner ayarlarken bir birim türü seçebilirsiniz.

Birim türleri yalnızca Varış yeri maliyetinde kullanılır. TMS'de mevcut değildir.

Birim türleriyle çalışmak için **Varış yeri maliyeti \> Konteynerleri ayarlama \> Birimi türleri**'ne gidin. Burada, birim türlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Birim türü | Birim türü için benzersiz bir tanımlama adı/numarası girin. |
| Tanım | Birim türü için açıklama girin. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Soğutma türlerini ayarlama

Soğutma türleri, sevkiyat konteynerleri (genellikle soğutmalı konteynerler) için ek gruplandırmalar ve tanımlama yöntemleri oluşturur. **Tüm sevkiyat konteynerleri** sayfasında bir konteyner ayarlarken bir soğutma türü seçebilirsiniz.

Soğutma türleriyle çalışmak için **Varış yeri maliyeti \> Konteynerleri ayarlama \> Soğutma türleri**'ne gidin. Burada, soğutma türlerinizin kayıtlarını görüntüleyebilir, ekleyebilir ve kaldırabilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Soğutma türü | Soğutma türü için benzersiz bir tanımlama adı/numarası girin. |
| Tanım | Soğutma türü için açıklama girin. |