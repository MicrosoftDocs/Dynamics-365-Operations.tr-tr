---
title: Şablon ürün reçetesi oluşturma
description: Çeşitli yöntemler kullanarak şablon ürün reçetesi oluşturabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470797"
---
# <a name="create-a-template-bom"></a>Şablon ürün reçetesi oluşturma   

[!include [banner](../includes/banner.md)]


Aşağıdaki yöntemlerden herhangi birini kullanarak şablon ürün reçetesi oluşturabilirsiniz. Tüm yöntemlerde **Başlangıç tarihi** ve **Bitiş tarihi** alanları isteğe bağlıdır ve yalnızca bilgi verici niteliktedir.

## <a name="create-a-template-bom-manually"></a>El ile şablon ürün reçetesi oluşturma

1.  **Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.

2.  **Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.

3.  **Ürün reçetesini satırlarını referanstan kopyala** altından **el ile** seçeneğini seçin.

4.  **Madde numarası** alanına **BOM** türünde bir madde girin.

5.  **Ad** alanına, şablon için bir ad girin.

6.  **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.

7.  **Tamam**'ı seçin.

Yeni, boş bir şablon ürün reçetesi oluşturulur.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Başka bir şablon ürün reçetesini temel alarak şablon ürün reçetesi oluşturma

1.  **Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.

2.  **Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.

3.  **Ürün reçetesini satırlarını referanstan kopyala** altından **Şablon ürün reçetesi** seçeneğini seçin.

4.  **Referans numarası** alanında, yeni şablon ürün reçetenize kopyalanacak mevcut şablon ürün reçetesini seçin.

5.  **Ad** alanına, şablon için bir ad girin.

6.  **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.

7.  **Tamam**'ı seçin.

Orijinal şablon ürün reçetesindeki satırlara karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Bir madde ürün reçetesini temel alarak şablon ürün reçetesi oluşturma

1.  **Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.

2.  **Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.

3.  **Ürün reçetesi satırlarını referanstan kopyala** altından **Ürün reçetesi**'ni seçin.

4.  **Referans numarası** alanında, bir ürün reçetesi versiyonu seçin. **Madde numarası**'na ürün reçetesi türünde bir madde kopyalanır.

5.  **Ad** alanına, şablon için bir ad girin.

6.  **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.

7.  **Tamam**'ı seçin.

**Üürn reçeteleri** içinde listelenen ürün reçetesinin satırlarına karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Bir üretim ürün reçetesi temel alınarak şablon ürün reçetesi oluşturma

1.  **Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.

2.  **Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.

3.  **Ürün reçetesi satırlarını referanstan kopyala** altından **Üretim**'i seçin.

4.  **Referans numarası** alanında, bir üretim ürün reçetesi seçin.

5.  **Ad** alanına, şablon için bir ad girin.

6.  **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.

7.  **Tamam**'ı seçin.

**Ürün reçetesi** içinde listelenen ürün reçetesinin satırlarına karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.

## <a name="see-also"></a>Ayrıca bkz.

[Şablon ürün reçeteleri](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]