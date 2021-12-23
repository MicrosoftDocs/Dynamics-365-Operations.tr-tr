---
title: Madde vergisi gruplarını ayarlama
description: Bu konuda, Vergi Hesaplama hizmetinde madde vergi gruplarının nasıl ayarlanılacağı açıklanmaktadır.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883887"
---
# <a name="set-up-item-tax-groups"></a>Madde vergisi gruplarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konuda, Vergi Hesaplama hizmetinde madde vergi gruplarının nasıl ayarlanılacağı açıklanmaktadır. Ayrıca, madde vergi grubu uygulanabilirlik kuralı matrisinin nasıl ayarlanıp matristeki satırların nasıl yapılandırılacağı açıklanmaktadır.

Vergi Hesaplama hizmetindeki madde vergi grupları kavramı, Microsoft Dynamics 365 Finance'teki madde satış vergisi grupları kavramına benzerdir. Bunlar vergi kodu gruplarıdır. Vergi Hesaplama hizmeti, vergi kodlarını belirlemek için bir vergi grubu ile madde vergi grubunun kesişimini kullanır.

> [!IMPORTANT]
> Vergi Hesaplama hizmetinde madde vergi grupları düzeni tüzel kişilikten bağımsızdır. Bu düzeni Regulatory Configuration Service'ten (RCS) yalnızca bir kez tamamlayabilirsiniz. Finance'te Vergi Hesaplama hizmetini etkinleştirdiğinizde, madde vergi grupları seçili tüzel kişilik için otomatik olarak eşitlenir.

## <a name="set-up-an-item-tax-group"></a>Madde vergi gruplarını ayarlama 

Madde vergi grubu ayarlamak için aşağıdaki adımları izleyin.

1. [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)'te oturum açın.
2. **Çalışma Alanları** \> **Globalleştirme özellikleri** \> **Vergi hesaplama**'ya gidin.
3. Ayarlamak istediğiniz özellik ve sürümün ardından **Düzenle**'yi seçin.
4. **Genel** sekmesinde, **Yapılandırma sürümü**'nü seçin.
5. **Madde vergi grubu** sekmesinde **Sütunu yönet**'i seçin. İlk kez bir madde vergi grubu ayarlıyorsanız **Sütunu yönet** iletişim kutusundaki alanlar otomatik olarak ayarlanır.
6. Soldaki listede, **Satırlar** düğümünü genişletin ve **Madde Vergi Grubu** onay kutusunu seçin.

    ![Sütunları yönet iletişim kutusundaki Satırlar düğümü altında vergi grubu seçildi.](media/select-item-tax-group.png)

7. **Madde Vergi Grubu**'nu sağdaki **Seçili sütunlar** listesine eklemek için sağ ok düğmesini seçin.

    ![Madde Vergi Grubu Seçili sütunlar listesine eklenmiştir.](media/add-item-tax-group.png)

8. **Tamam**'ı seçin.

## <a name="configure-an-item-tax-group"></a>Madde vergi gruplarını yapılandırma

Bir madde vergi grubunu ayarladıktan sonra, uygulanabilirlik kuralı matrisi oluşturulur. Madde vergi grubunu yapılandırmak için matrise satır ekleyebilirsiniz.

1. **Madde vergi grubu** sekmesinde **Ekle**'yi seçin.
2. **Madde vergi grubu** alanına madde vergi grubunun adını girin.

    > [!IMPORTANT]
    > Madde vergi grubunun adını 10 karakterle sınırlamanızı öneririz. Bu ad, Finance ile eşitlenir. Finance'te madde satış vergisi gruplarının adları için sınır 10 karakterdir.

3. **Vergi kodları** alanında, madde vergi grubuna dahil etmek istediğiniz her vergi kodunun onay kutusunu işaretleyin. Bir madde vergi grubuna birden çok vergi kodu ekleyebilirsiniz.

    ![Vergi kodları alanında birden çok vergi kodu seçilidir.](media/multiple-tax-codes-selection.png)

4. Daha fazla madde vergi grupları eklemek için 1 ile 3 arasındaki adımları yineleyin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
