---
title: "Öznitelikler oluşturmak ve yönetmek"
description: "Bu makale Microsoft Dynamics 365 işlemleri için öznitelikleri açıklar. Öznitelikler kullanıcı tanımlı alanlar aracılığıyla ürün ve özellikleri açıklamanızı sağlar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Öznitelikler oluşturmak ve yönetmek

Bu makale Microsoft Dynamics 365 işlemleri için öznitelikleri açıklar. Öznitelikler kullanıcı tanımlı alanlar aracılığıyla ürün ve özellikleri açıklamanızı sağlar.

Öznitelikler kullanıcı tanımlı alanlar aracılığıyla ürün ve özellikleri açıklamanızı sağlar. Örneğin, ürünün bellek boyutu ve sabit disk kapasitesi belirtebilir ve ürünün Energy star uyumlu olup olmadığını belirtebilirsiniz. Öznitelikleri ürün kategorileri ve perakende kanalları gibi çeşitli perakende varlıklar ile ilişkili olabilir ve bunlar için varsayılan değerler ayarlanabilir. Ürün kategorileri veya perakende kanalları ile ilişkili olduğunda ürünleri özniteliklerini ve bu öznitelikleri için varsayılan değerleri devralır. Varsayılan değerleri tek tek ürün, perakende kanal düzeyinde veya perakende Kataloğu düzeyinde geçersiz kılınabilir.

#### <a name="examples"></a>Örnekler

Kategori

Öznitelik

İzin verilen değerler

Varsayılan değer

TV ve Video

Marka

Herhangi bir geçerli **marka** değeri

Yok

TV

Ekran Boyutu

**20"**–**80"**

Yok

Dikey Çözünürlük

**480i**, **720p**, **1080i** veya **1080p**

**1080p**

Ekran yenileme hızı

**60hz**, **120hz** veya **240hz**

**60hz**

HDMI Girdileri

**0**–**10**

**3**

DVI Girdileri

**0**–**10**

**1**

Bileşik Girdiler

**0**–**10**

**2**

Bileşen Girdileri

**0**–**10**

**1**

LCD

3D Hazır

**Evet** veya **Hayır**

**Evet**

3D etkin

**Evet** veya **Hayır**

**Hayır**

Plazma

Çalıştırma Sıcaklığı Başlangıç

**32**–**110** derece

**32**

Çalıştırma Sıcaklığı Son

**32**–**110** derece

**100**

Projeksiyon

Projeksiyon tüp garanti

**6**, **12** veya **18** ay

**12**

\#Projeksiyon Tüpleri

**1**–**5**

**3**

## <a name="attribute-type"></a>Öznitelik türü
  [![öznitelikler sabit kopya](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) özniteliklerin öznitelik türlerini temel alan. Öznitelik türleri, belirli bir öznitelik için girilen veri türünü tanımlar. Şu anda Microsoft Dynamics 365 işlemleri için aşağıdaki öznitelik türlerini destekler:

-   **Para** – bu öznitelik türü para birimi değerlerini destekler. Bağlantılı olmalıdır (diğer bir deyişle, bir değer aralığı destekleyebilir) veya açık bırakılabilir.
-   **DateTime** – bu öznitelik türü, tarih ve saat değerlerini destekler. Bağlantılı olmalıdır (diğer bir deyişle, bir değer aralığı destekleyebilir) veya açık bırakılabilir.
-   **Ondalık** – bu öznitelik türü, ondalık basamak içeren sayısal değerleri destekler. Ayrıca, ölçü birimleri destekler. Bağlantılı olmalıdır (diğer bir deyişle, bir değer aralığı destekleyebilir) veya açık bırakılabilir.
-   **Tamsayı** – bu öznitelik türü sayısal değerleri destekler. Ayrıca, ölçü birimleri destekler. Bağlantılı olmalıdır (diğer bir deyişle, bir değer aralığı destekleyebilir) veya açık bırakılabilir.
-   **Metin** – bu öznitelik türü metin değerlerini destekler. önceden tanımlanmış bir dizi olası değerleri de (numaralandırma) destekler.
-   **Boole** – bu öznitelik türü ikili değerleri destekler (**doğru**/**yanlış**).
-   **Referans**.

## <a name="attribute"></a>Öznitelik
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) adı, kolay ad, açıklama ve Yardım metni ek olarak, aşağıdaki bilgi türlerinden bir veya bir öznitelik için yakalanabilir:

-   Varsayılan değer
-   Öznitelik aradı, Siyah Zeminli veya sıralanabilecek olup olmadığını gösterir meta veriler gibi öznitelik meta verileri

## <a name="attribute-group"></a>Öznitelik grubu
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) özniteliklerin tanımladıktan sonra öznitelik gruplar halinde gruplandırılabilir. Öznitelik grupları bireysel niteliklerini gruplandırmaları sağlar ve perakende kategoriler veya perakende kanalları için atanabilir.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Öznitelik gruplarını perakende kategorilere atama
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) bir veya daha fazla öznitelik gruplarýný perakende ürün kategori sıradüzenindeki kategori düğümleri ile ilişkili olabilir. Ürünler kategorize edildiğinde, öznitelik gruplarına dahil edilen öznitelikleri devralır.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Öznitelik gruplarını perakende mağazalarına atama
  [![createandmanageattribute-13-1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) bir veya daha fazla öznitelik gruplarý olabilir ilişkili bir veya daha fazla perakende mağazaları perakende mağazaları hiyerarşisinde ile. Ürünler belirli perakende mağazaları için zenginleştirildiğinde, öznitelik gruplarına dahil edilen öznitelikleri devralır.

## <a name="overriding-attribute-values"></a>Geçersiz kılınan öznitelik değerleri
### <a name="at-the-product-level"></a>Ürün düzeyinde

  [![createandmanageattribute-14-1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) ürün düzeyinde geçersiz kılınabilir özniteliklerinin varsayılan değerlerini (diğer bir deyişle, tek tek ürünler için).

### <a name="in-a-retail-catalog"></a>Perakende kataloğunda

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) tek tek ürünlerin belirli perakende kanalları için hedeflenen belirli kataloglar özniteliklerinin varsayılan değerlerini geçersiz kılınabilir.

### <a name="at-the-retail-channel-level"></a>Perakende kanalı düzeyinde

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) özel perakende kanalları için hedeflenen belirli kataloglar bireysel ürünlerin özniteliklerinin varsayılan değerlerini geçersiz kılınabilir.


