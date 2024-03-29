---
title: Servis anlaşmaları oluşturma
description: Bu makale, Servis yönetimi ve Proje yönetimi ile muhasebe modüllerinde servis sözleşmeleri oluşturmak için özelliklerin nasıl kullanılacağını açıklar.
author: sorenva
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d18d279cd437e98cad6495def953978cb78e723e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901777"
---
# <a name="create-service-agreements"></a>Servis anlaşmaları oluşturma

[!include [banner](../includes/banner.md)]

Bu makale, Servis yönetimi ve Proje yönetimi ile muhasebe modüllerinde servis sözleşmeleri oluşturmak için özelliklerin nasıl kullanılacağını açıklar.

## <a name="create-a-service-agreement-from-service-management"></a>Servis yönetiminden servis sözleşmesi oluşturma

1. **Servis yönetimi**'ne gidin.
2. Sayfa başlığında yeni bir servis sözleşmesi oluşturmak için **Servis sözleşmeleri**'ni seçin. 
3. **Yeni**'yi seçin. Açıklama girin, **Proje Kodu** alanındaki bir projeye yönelik bir referans seçin ve servis sözleşmesi için geri kalan alanları ve satırları doldurun. **Kaydet**'i seçin.
4. Servis sözleşmesi için servis nesnesi ilişkileri veya servis görevi ilişkileri oluşturmak için **İlişkiler** sekmesinde, **Servis nesneleri**'ni veya **Servis görevleri**'ni seçin. Kendilerine ait ilişkiler oluşturduğunuz servis nesneleri ve görevleri servis anlaşmasının satırlarına iliştirilebilir.
5. Sayfanın alt yarısında, satırları bir servis şablonundan ya da başka bir servis sözleşmesinden kopyalayarak veya servis sözleşmesi satırlarını el ile oluşturarak servis sözleşmesi satırları oluşturun.

> [!NOTE]
> Satırları servis sözleşmesine başka bir servis sözleşmesinden kopyalarsanız, servis nesnesi ve servis görevi ilişkilerini kopyalamayı isteyip istemediğinizi gösterebilirsiniz. Bu ilişkileri kopyalarsanız, bunlar servis anlaşmasındaki mevcut ilişkilere eklenecektir. Servis anlaşması satırlarını bir servis şablonundan kopyalarsanız, servis nesnesi ve servis görevi ilişkileri otomatik olarak yeni servis anlaşması satırlarına servis nesnesi ilişkileri ve servis görevi ilişkileri olarak kopyalanacaktır.

## <a name="create-service-agreement-lines-manually"></a>Servis sözleşmesi satırlarını el ile oluşturma

1. **Service sözleşmeleri** sayfasından satır kılavuzundaki bir servis sözleşmesini ekleyin. 
2. Servis sözleşmesi satırı için uygun bilgileri girin. 
3. Satırı kaydetmek için **Kaydet**'i seçin ve ardından sayfayı kapatın.

## <a name="create-a-service-agreement-from-project"></a>Proje'den bir servis anlaşması oluşturma

1. **Proje yönetimi ve muhasebe**'yi seçin.
2. **Tüm projeler**'i seçin.
3. Listeden projeyi seçin.
4. **Eylem Bölmesinde**, **Yönet**'i seçin. **Yeni** Eylem grubunda **Servis**'i ve **Servis sözleşmesi**'ni seçin.
5. Proje referansını girmek için bu makalede daha önce açıklandığı gibi **Servis sözleşmesi oluşturma** başlıklı bölümdeki adımları izleyin.


## <a name="related-articles"></a>İlgili makaleler

[Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]