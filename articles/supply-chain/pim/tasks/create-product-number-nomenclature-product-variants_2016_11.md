---
title: Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921023"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir. Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır. Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.

## <a name="create-a-product-number-nomenclature"></a>Ürün numara terminolojisi oluşturma

1. **Ürün bilgi yönetimi \> Kurulum \> Ürün terminolojisi**'ne gidin.
1. **Yeni**'yi seçin.
1. **Ad** alanına bir değer yazın.
1. **Tanım** alanına bir değer girin.
1. **Ekle**'yi seçin.
1. **Ürün ana numarası**'nı seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. Listede, seçili satırı işaretleyin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Yapılandırma**'yı seçin.
1. Sayfayı kapatın.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Ana ürüne, ürün numara terminolojisi atama

1. **Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin.
1. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Ürün numarası** alanında "D" değeriyle filtreleyin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Düzenle** öğesini seçin.
1. *Terminolojiyi kullan* alanında **Evet**'i seçin.
1. **Ürün çeşidi numara terminolojisi** alanında bir değer girin veya seçin.
1. Sayfayı kapatın.
1. Sayfayı kapatın.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Ürün yapılandırma model bileşeni için terminoloji oluşturma

1. **Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. Listede, istenen kaydı bulun ve seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Düzenle** öğesini seçin.
1. **Yapılandırma terminolojisini kullan** alanında *Evet*'i seçin.
1. **Ekle**'yi seçin.
1. **Öznitelik değeri**'ni seçin.
1. Listede, seçili satırı işaretleyin.
1. **Öznitelik** alanına bir değer girin veya seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. Listede, seçili satırı işaretleyin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Öznitelik değeri**'ni seçin.
1. Listede, seçili satırı işaretleyin.
1. **Öznitelik** alanına bir değer girin veya seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. Listede, seçili satırı işaretleyin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Öznitelik değeri**'ni seçin.
1. Listede, seçili satırı işaretleyin.
1. **Öznitelik** alanına bir değer girin veya seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. Listede, seçili satırı işaretleyin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Öznitelik değeri**'ni seçin.
1. Listede, seçili satırı işaretleyin.
1. **Öznitelik** alanına bir değer girin veya seçin.
1. **Ekle**'yi seçin.
1. **Metin sabiti** seçin.
1. Listede, seçili satırı işaretleyin.
1. **Metin** alanına bir değer yazın.
1. **Ekle**'yi seçin.
1. **Numara serisi değeri**'ni seçin.
1. Listede, seçili satırı işaretleyin.
1. **Numara sırası** alanında, bir değer girin veya seçin.
1. Sayfayı kapatın.
1. Sayfayı kapatın.
1. Sayfayı kapatın.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]