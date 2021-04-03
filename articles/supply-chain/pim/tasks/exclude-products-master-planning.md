---
title: Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma
description: Bu yordam, ürünleri Master planlama ve ürün reçetesi düzeyinde hesaplama dışında tutan yeni bir ürün yaşam döngüsü durumunun nasıl oluşturulacağını açıklar.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc24aad05499adf9bfb2db3613c7f134c3a70770
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264710"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, ürünleri Master planlama ve ürün reçetesi düzeyinde hesaplama dışında tutan yeni bir ürün yaşam döngüsü durumunun nasıl oluşturulacağını açıklar.


## <a name="create-an-obsolete-state"></a>Geçersiz bir durum oluşturma
1. Ürün bilgileri yönetimi > Kurulum > Ürün yaşam döngüsü durumu seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Durum alanına bir değer yazın.
4. Planlama için etkin alanında Hayır'ı seçin.
5. Açıklama alanına bir değer girin.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Serbest bırakılan bir ürünle geçersiz durumunu ilişkilendirme
1. Sayfayı kapatın.
2. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
3. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ad ara alanına bir 'M00' değeriyle filtre uygulayın.
4. Düzenle öğesine tıklayın.
5. Listede, seçili satırı işaretleyin.
6. Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]