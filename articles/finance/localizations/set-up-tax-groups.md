---
title: Vergi gruplarını ayarlama
description: Bu konuda, Vergi Hesaplama hizmetinde vergi gruplarının nasıl ayarlanılacağı açıklanmaktadır.
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
ms.openlocfilehash: 50abafb958edfb8476434ff5842cd84cb186962f
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883889"
---
# <a name="set-up-tax-groups"></a>Vergi gruplarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konuda, Vergi Hesaplama hizmetinde vergi gruplarının nasıl ayarlanılacağı açıklanmaktadır. Ayrıca, vergi grubu uygulanabilirlik kuralı matrisinin nasıl ayarlanıp matristeki satırların nasıl yapılandırılacağı açıklanmaktadır.

Vergi Hesaplama hizmetindeki vergi grupları kavramı, Microsoft Dynamics 365 Finance'teki satış vergisi grupları kavramına benzerdir. Bunlar vergi kodu gruplarıdır. Vergi Hesaplama hizmeti, vergi kodlarını belirlemek için bir vergi grubu ile madde vergi grubunun kesişimini kullanır.

Ancak, Vergi Hesaplama hizmetindeki vergi grupları, Finance'teki satış vergisi gruplarından farklıdır çünkü bunlarda **Vergi kullan** ve **Vergiyi muaf tut** gibi ek parametreler yoktur. Bunun yerine, bu parametreler vergi kodu düzeyinde kullanılabilir.

> [!IMPORTANT]
> Vergi Hesaplama hizmetinde vergi grupları düzeni tüzel kişilikten bağımsızdır. Bu düzeni Regulatory Configuration Service'ten (RCS) yalnızca bir kez tamamlayabilirsiniz. Finance'te Vergi Hesaplama hizmetini etkinleştirdiğinizde, vergi grupları seçili tüzel kişilik için otomatik olarak eşitlenir.

## <a name="set-up-a-tax-group"></a>Vergi grubu ayarlama

Vergi grubu ayarlamak için aşağıdaki adımları izleyin.

1. [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)'te oturum açın.
2. **Çalışma Alanları** \> **Globalleştirme özellikleri** \> **Vergi hesaplama**'ya gidin.
3. Ayarlamak istediğiniz özellik ve sürümün ardından **Düzenle**'yi seçin.
4. **Genel** sekmesinde, **Yapılandırma sürümü**'nü seçin.
5. **Vergi grubu** sekmesinde **Sütunu Yönet**'i seçin. İlk kez bir vergi grubu ayarlıyorsanız **Sütunu yönet** iletişim kutusundaki alanlar otomatik olarak ayarlanır.
6. Soldaki listede, **Satırlar** düğümünü genişletin ve **Vergi Grubu** onay kutusunu seçin.

    ![Sütunları yönet iletişim kutusundaki Satırlar Düğümü altında vergi grubu seçildi.](media/select-tax-group.png)

7. **Vergi Grubu**'nu sağdaki **Seçili sütunlar** listesine eklemek için sağ ok düğmesini seçin.

    ![Vergi Grubu Seçili sütunlar listesine eklenmiştir.](media/add-tax-group.png)

8. **Tamam**'ı seçin.

## <a name="configure-a-tax-group"></a>Vergi gruplarını yapılandırma

Bir vergi grubunu ayarladıktan sonra, vergi grubu uygulanabilirlik kuralı matrisi oluşturulur. Vergi grubunu yapılandırmak için matrise satır ekleyebilirsiniz.

1. **Vergi grubu** sekmesinde **Ekle**'yi seçin.
2. **Vergi grubu** alanına vergi grubunun adını girin.

    > [!IMPORTANT]
    > Vergi grubunun adını 10 karakterle sınırlamanızı öneririz. Bu ad, Finans ile eşitlenir. Finance'te satış vergisi gruplarının adları için sınır 10 karakterdir.

3. **Vergi kodları** alanında, vergi grubuna dahil etmek istediğiniz her vergi kodunun onay kutusunu işaretleyin. Bir vergi grubuna birden çok vergi kodu ekleyebilirsiniz.

    ![Vergi kodları alanında birden çok vergi kodu seçilidir.](media/multiple-tax-codes-selection.png)

4. Daha fazla vergi grupları eklemek için 1 ile 3 arasındaki adımları yineleyin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
