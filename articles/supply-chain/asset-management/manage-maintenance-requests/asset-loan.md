---
title: Ödünç varlıklar
description: Bu konuda Varlık Yönetimi'nde ödünç varlık kaydetme işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 355e3d3e0e952db14a03810145528f9701804ca2
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022344"
---
# <a name="asset-loans"></a>Ödünç varlıklar

[!include [banner](../../includes/banner.md)]

 

Şirketiniz, dahili konumlardan veya müşterilerden onarım veya bakım işleri için varlıklar alırsa ve varlıkları bu konumlara veya müşterilere geçici olarak ödünç veriyorsanız varlık yönetimi ödünç varlıklarını izleyebilir.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Bir bakım talebine ödünç varlık kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.
2. Bir ödünç varlığa kaydedilecek bakım talebini seçin ve ardından **Düzenle**'yi seçin.
3. **İstek** sayfasında **Ödünç varlığı gönder**'i seçin.
4. Varlığı seçin ve beklenen dönüş tarihini girin.
5. **Tamam**'ı seçin.

> [!NOTE]
> - Bir ödünç varlığı yalnızca aynı varlık türünün bir varlığı kullanılabilir olduğunda gönderebilirsiniz.
> - Ödünç verilen varlığın **Depoda** gibi bir ödünç varlık olarak kullanılmasını sağlayan bir varlığın yaşam döngüsü durumuna sahip olması gerekir. Ödünç varlık kaydedildiğinde, varlığın varlık yaşam döngüsü durumu otomatik olarak, örneğin **Ödünç Verildi** olarak güncelleştirilir.

Diğer yerlere veya müşterilere ödünç vermiş olduğunuz tüm varlıkların listesini görüntülemek için **Varlık yönetimi** \> **Ortak** \> **Ödünç varlık** \> **Tüm ödünç varlıklar**'ı seçin. Bir varlık için **Sona erdi** kutusu seçiliyse varlık şirketiniz için iade edilmiş olarak kalır.

![Bakım Taleplerini Yönetme](media/06-manage-maintenance-requests.png)

**Etkin ödünç varlıklar** sayfasında henüz şirketinize iade edilmeyen tüm ödünç varlıkların listesini görüntüleyebilirsiniz.

## <a name="register-loan-assets-as-returned"></a>İade edilen ödünç varlıkları kaydedin

1. **Varlık yönetimi** \> **Ortak** \> **Ödünç varlık** \> **Etkin ödünç varlıklar**'ı seçin.
2. İade edilen olarak kaydetmek için ödünç varlık'ı seçin ve sonra **Ödünç varlığı iade edin**'i seçin..
3. **İade edildi** alanında tarihi ve saati girin.
4. **Tamam**'ı seçin.
5. **Etkin ödünç varlıklar** listesi sayfasını yenileyin ve ödünç varlığın artık listede görünüp görünmediğine dikkat edin.
