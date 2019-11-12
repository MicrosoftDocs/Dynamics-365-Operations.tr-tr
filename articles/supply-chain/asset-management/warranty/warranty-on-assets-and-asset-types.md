---
title: Kıymet ve kıymet türlerinde garantiler
description: Bu konu, Varlık Yönetimi'nde kıymet garantilerinin ve kıymet türlerinin nasıl ayarlanacağını açıklar.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e69b471af0853159ba807af5f39db64dbbb04f8
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569720"
---
# <a name="warranties-on-assets-and-asset-types"></a>Kıymet ve kıymet türlerinde garantiler

[!include [banner](../../includes/banner.md)]

 


Bu konu, Varlık Yönetimi'nde kıymet garantilerinin ve kıymet türlerinin nasıl ayarlanacağını açıklar.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Kıymet türünde garanti ayarlayın

1. **Varlık yönetimi** \> **Kurulum** \> **Varlık türleri** \> **Varlık türleri**'ni seçin.
2. Sol bölmede, satıcı garanti sözleşmesini iliştirmek için sabit kıymet türünü seçin ve **Kıymet türü varsayılanları**'nı seçin.
3. **Genel** hızlı sekmesinde, **Satıcı garantisi** alanında, sözleşmeyi seçin.

## <a name="set-up-a-warranty-on-an-asset"></a>Kıymette garanti ayarlayın

1. **Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin.
2. Kıymeti seçin ve **Düzenle**'yi seçin.
3. **Satıcı** hızlı sekmesinde, **Satıcı garantisi** bölümünde, **Garanti** alanında, garanti sözleşmesini seçin.
4. **Garanti başlangıcı** ve **Garanti sonu** alanlarında, başlangıç ve bitiş tarihlerini seçin.

    > [!IMPORTANT]
    > Bir iş emrinin **Garanti başlangıcı** alanında bir tarih seçilirse garanti o tarihteki iş emri için geçerli olur. Bir iş emri oluşturduğunuzda, **Garanti başlangıcı** alanı otomatik olarak oluşturma tarihine göre ayarlanır. Ancak, tarihi, örneğin garanti anlaşmasının başlangıç tarihine karşılık gelecek şekilde değiştirebilirsiniz.
    >
    > ![İş emri sayfası](media/02-warranty.png)

> [!NOTE]
> Satıcı garantisinin kapsadığı bir kıymet için çalışma emri oluşturduğunuzda, iş emrinde garanti dönemi içinde beklenen başlangıç tarihi varsa garanti sözleşmesiyle ilgili bir bildirim alırsınız. Böylece, gereksinim duyduğunuz şekilde iş emrini iptal edebilirsiniz.
