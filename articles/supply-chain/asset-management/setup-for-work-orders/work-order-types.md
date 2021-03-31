---
title: İş emri türleri
description: Bu konuda Varlık Yönetimi'nde iş emri türünü açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 561ca87740d90590262716f0042fca6b59dafc69
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223542"
---
# <a name="work-order-types"></a>İş emri türleri

[!include [banner](../../includes/banner.md)]

 

İş emri türleri, iş emirlerini sınıflandırmak için kullanılır. Örneğin, önleyici bakım ve düzeltici bakım ya da ilgili bakımiş emirlerine sahip olabilirsiniz.

Bir iş emri türü, iş emri yaşam döngüsü modeliyle bir ilişki tanımlar. Bir iş emri yaşam döngüsü modeli, bir iş emrinde ayarlayabilecek iş emri yaşam döngüsü durumlarını tanımlar. (İş emri yaşam döngüsü durumlarına örnek olarak **Oluşturma tarihi**, **İşlemde**, ve **Tamamlandı** verilebilir.)

İş emri yaşam döngüsü durumları ve proje aşamaları hakkında daha fazla bilgi için bkz [İş emri yaşam döngüsü durumu](work-order-lifecycle-states.md).

1. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **İş emri türleri**'ni seçin.
2. İş emri türü oluşturmak için **Yeni**'yi seçin.
3. **İş emri türü** alanına iş emri türü için bir kimlik girin.
4. **Ad** alanına, bir ad girin.
5. **İş emri yaşam döngüsü modeli** alanında bir yaşam döngüsü modeli seçin.
5. Bu tip bir iş emriyle ilişkili tüm iş siparişi işleri aynı bakım görevlisine zamanlanacaksa, **Bir bakım görevlisi** seçeneğini **Evet** olarak ayarlayın.
6. **Maliyet türü** alanında, uygun şekilde **Düzeltici**, **Önleyici** veya **Yatırım** seçeneğini belirleyin. Bir iş emrindeki tüm iş emri işleri maliyet türünde olmalıdır.
7. **Zorunlu** bölümünde, arıza ile ilgili veya bakım kapalı kalma süresi ile ilgili bilgilerin bu tip bir iş emrine eklendiğini belirtmek için, ilgili seçenekleri **Evet** olarak ayarlayın.

    > [!NOTE]
    > **Zorunlu** bölümündeki seçenekler **İş emri yaşam döngüsü durumları** sayfasının **Doğrula** hızlı sekmesindeki seçeneklerle ilişkilidir (**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Yaşam döngüsü durumuları**).

8. **Kaydet**'i seçin.

![İş emri türleri](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]