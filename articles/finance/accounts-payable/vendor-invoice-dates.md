---
title: Satıcı fatura tarihleri
description: Bu makale, satıcı faturalarında görünen tarihleri açıklar. Ayrıca deftere nakil tarihinin otomatik olarak ayarlamasını da açıklar.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775285"
---
# <a name="vendor-invoice-dates"></a>Satıcı fatura tarihleri

[!include [banner](../includes/banner.md)]

Bu makale, satıcı faturalarında görünen tarihleri açıklar. Ayrıca deftere nakil tarihinin otomatik olarak ayarlamasını da açıklar.

**Bekleyen satıcı faturası ayrıntılı** sayfasında, fatura başlığı dört tarih gösterir: **Fatura alma tarihi**, **fatura tarihi**, **deftere nakil tarihi** ve **vade tarihi**. Bir satıcı faturası oluşturulduğunda, varsayılan olarak aşağıdaki tarihler girilir:

- **Fatura alınma tarihi** – Bu alan geçerli sistem tarihi olarak ayarlanır.
- **Deftere nakil tarihi** – Bu alan geçerli sistem tarihi olarak ayarlanır. 
- **Vade tarihi** – Bu alandaki tarih, deftere nakil tarihi ve ödeme koşulları temel alınarak hesaplanır.
- **Fatura tarihi** – Varsayılan olarak bu alan boştur. Ancak, istediğiniz değerleri girebilirsiniz. Bu durumda, **Vade tarihi** alanındaki tarih, fatura tarihi ve ödeme koşulları temel alınarak yeniden hesaplanır.

Bazen, satıcı faturası dönem kapanışıyla uzun bir süredir bekleme durumunda olabilir. Deftere nakil için hazır olduğunda, geçmiş deftere nakil döneminin eski deftere nakil tarihi kullanılmaya devam eder. Ancak bu dönem şimdi kapatıldı. Bu nedenle, Borç hesapları (AP) memuru, önceden oluşturulmuş tüm bekleyen faturalar için deftere nakil tarihlerini el ile yeni deftere nakil dönemiyle değiştirmek zorundadır.

Bu makalede açıklanan özellik, deftere nakil tarihini iş gereksinimlerine göre otomatik olarak ayarlamanıza olanak sağlar.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Satıcı faturası deftere nakil tarihini otomatik olarak ayarlamak için parametre

Satıcı faturalarının deftere nakil tarihini otomatik olarak ayarlamak için aşağıdaki adımları izleyin.

1.  **Borç hesabı \> Kurulum \> Borç hesabı parametreleri**'ne gidin.
2.  **Genel muhasebe ve satış vergisi** sekmesinde, **Deftere nakil tarihini otomatik ayarla** alanında aşağıdaki değerlerden birini seçin:

    - **Değişiklik yok** – Sistem, deftere nakil sırasında deftere nakil tarihini otomatik olarak değiştirmez. Bu değer, varsayılan olarak seçilir.
    - **Deftere nakil tarihini her zaman sistem tarihine değiştir** – Deftere nakil sırasında deftere nakil tarihi otomatik olarak sistem tarihine değiştirilir.
    - **Deftere nakil tarihi kapalı veya beklemedeyse deftere nakil tarihini sistem tarihi olarak değiştir** – Deftere nakil sırasında deftere nakil tarihi otomatik olarak sistem tarihine dönüştürülür, ancak bu deftere nakil tarihi için ilgili dönemin **Kapalı** veya **Beklemede** durumunda olması gereklidir.
    - **Deftere nakil tarihi kapalı veya beklemedeyse deftere nakil tarihini dönemin ilk günü olarak değiştir** – Deftere nakil tarihi yeni açık dönemin ilk günü olarak değiştirilir ancak bu deftere nakil tarihi için ilgili dönemin **Kapalı** veya **Beklemede** durumunda olması gereklidir.

> [!NOTE]
> Otomatik olarak düzeltilen yeni deftere nakil tarihi yeni bir mali yıldaysa, faturanın deftere nakil tarihi güncelleştirilmez. Kullanıcı "Mali yıl değişti. Lütfen deftere nakil tarihini denetleyip yeniden girin." hatası alır Deftere nakil için fatura deftere nakil tarihi yeni mali yıl tarihi olarak güncelleştirilmelidir.

## <a name="impact-of-posting-date-changes"></a>Deftere nakil tarihi değişikliklerinin etkisi

Bekleyen bir satıcı faturasındaki deftere nakil tarihi değiştiğinde, bu değişikliğin aşağıdaki etkileri vardır:

- **Bitiş tarihi**

    - **Fatura tarihi** alanı boşsa, teslim tarihi yeni deftere nakil tarihi ve ödeme koşulları temel alınarak yeniden hesaplanır.
    - **Fatura tarihi** alanı önceden ayarlanmışsa, deftere nakil tarihi değişikliği son tarihi etkilemez.

- **Nakit iskonto tarihi**

    - **Fatura tarihi** alanı boşsa, nakit iskontosunu hesaplamak için yeni deftere nakil tarihi kullanılır.
    - **Fatura tarihi** alanı önceden ayarlanmışsa, nakit iskontosu değiştirilmez.

- **Döviz kuru** -Döviz kuru tarihi, **Borç hesapları parametreleri** sayfasının **Fatura** sekmesindeki **Fatura tarihini kullanarak satıcı muhasebesini güncelleştir** seçeneğinin ayarı tarafından belirlenir (**Borç hesabı \> Kurulum \> Borç hesabı parametreleri**).

    - Bu seçenek **Evet** olarak ayarlanmışsa, **fatura tarihi** kullanılır ve **deftere nakil tarih** değişikliği döviz kurunu etkilemez.
    - Bu seçenek **Hayır** olarak ayarlanırsa, deftere nakil tarihi döviz kurunu hesaplamak için kullanılır. Deftere nakil tarihi güncelleştirildiğinde, muhasebe ve raporlama tutarları yeniden hesaplanır. Bu nedenle, uygun doğrulamanın yeniden gerçekleştirilmesi gerekir.

## <a name="validation"></a>Doğrulama

**Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde bulunan diğer iki alan (**Borç hesabı \> Kurulum \> Borç hesabı parametreleri**) fatura işlemeyi etkiler:

- **Kullanılan fatura numarası kontrolü** alanı **Mali yıl içinde tekrarlanan öğeleri reddedecek** şekilde ayarlandıysa, fatura deftere nakli sırasında tekrarlanan faturaları denetlemek için deftere nakil tarihi kullanılır.
- **Satıcı faturasında belge tarihi gerekli** alanında **Hata seçeneği** ayarlanırsa, **Bekleyen fatura başlığında fatura tarihi** alanı gereklidir. Fatura tarihi deftere nakil tarihinden sonra ise bir hata mesajı gösterilir.
