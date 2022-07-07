---
title: Ödünç varlıklar
description: Bu makalede Varlık Yönetimi'nde ödünç varlık kaydetme işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f70b29ef69b80160f108e6f53edda12b86c2c9db
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015768"
---
# <a name="asset-loans"></a>Ödünç varlıklar

[!include [banner](../../includes/banner.md)]

 

Şirketiniz, dahili konumlardan veya müşterilerden onarım veya bakım işleri için varlıklar alırsa ve varlıkları bu konumlara veya müşterilere geçici olarak ödünç veriyorsanız varlık yönetimi ödünç varlıklarını izleyebilir.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Bir bakım talebine ödünç varlık kaydetme

1. **Varlık yönetimi** \> **Bakım talepleri** \> **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.
2. Bir ödünç varlığa kaydedilecek bakım talebini seçin ve ardından **Düzenle**'yi seçin.
3. **İstek** sayfasında **Ödünç varlığı gönder**'i seçin.
4. Varlığı seçin ve beklenen dönüş tarihini girin.
5. **Tamam**'ı seçin.

> [!NOTE]
> - Bir ödünç varlığı yalnızca aynı varlık türünün bir varlığı kullanılabilir olduğunda gönderebilirsiniz.
> - Ödünç verilen varlığın **Depoda** gibi bir ödünç varlık olarak kullanılmasını sağlayan bir varlığın yaşam döngüsü durumuna sahip olması gerekir. Ödünç varlık kaydedildiğinde, varlığın varlık yaşam döngüsü durumu otomatik olarak, örneğin **Ödünç Verildi** olarak güncelleştirilir.

Diğer konumlara veya müşterilere ödünç vermiş olduğunuz tüm varlıkların listesini görüntülemek için **Varlık yönetimi** \> **Ödünç varlık** \> **Tüm ödünç varlıklar**'ı seçin. Bir varlık için **Sona erdi** kutusu seçiliyse varlık şirketiniz için iade edilmiş olarak kalır.

![Bakım Taleplerini Yönetme.](media/06-manage-maintenance-requests.png)

**Etkin ödünç varlıklar** sayfasında henüz şirketinize iade edilmeyen tüm ödünç varlıkların listesini görüntüleyebilirsiniz.

## <a name="register-loan-assets-as-returned"></a>İade edilen ödünç varlıkları kaydedin

1. **Varlık yönetimi** \> **Ödünç varlık** \> **Etkin ödünç varlıklar**'ı seçin.
2. İade edilen olarak kaydetmek için ödünç varlık'ı seçin ve sonra **Ödünç varlığı iade edin**'i seçin..
3. **İade edildi** alanında tarihi ve saati girin.
4. **Tamam**'ı seçin.
5. **Etkin ödünç varlıklar** listesi sayfasını yenileyin ve ödünç varlığın artık listede görünüp görünmediğine dikkat edin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]