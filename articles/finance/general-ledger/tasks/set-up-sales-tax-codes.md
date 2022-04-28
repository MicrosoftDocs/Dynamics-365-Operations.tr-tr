---
title: Satış vergisi kodlarını ayarla
description: Bu konuda, Dynamics 365 Finance'te satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69e2cf9a16fe0e694154cccf9b49944b49c79b90
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565867"
---
# <a name="set-up-sales-tax-codes"></a>Satış vergisi kodlarını ayarla

[!include [banner](../../includes/banner.md)]

Bu konuda, satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır. Tüzel kişiliğin hesaplamak, tahsil etmek ve vergi dairelerine ödemekle yükümlü olduğu her dolaylı vergi ve harç için satış vergisi kodları oluşturulur.

Bu görevde USMF demo şirketi kullanılmaktadır.

1. **Gezinme bölmesi > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kodları**'na gidin.
2. **Yeni**'yi seçin.
3. **Satış vergisi kodu** alanına bir değer girin.
4. **Ad** alanına bir değer yazın.
5. Bu satış vergisinin hangi vergi dairesine, hangi aralıklarda bildirilip ödenmesi gerektiğini belirtmek üzere açılır listeyi açarak bir **Kapatma dönemi** seçin.
6. Satış vergisinin genel muhasebeye nakledileceği ana hesapları belirtmek için bir **Genel muhasebe deftere nakil grubu** seçin.
7. **Hesaplama** hızlı sekmesini genişletin. Burada, satış vergisi tutarlarının nasıl hesaplanacağını denetleyen birden çok alan vardır. Bu alanları gerektiği gibi doldurun.  
8. Arabirimin üst kısmındaki **Eylem Bölmesinde**, **Satış vergisi kodunu** seçin.
9. **Değerler**'i seçin.
10. Bu vergi kodunun değerini **değer** sütununa girin.

    **Hesaplama** hızlı sekmesindeki **Menşe** alanında **Birim başına tutar** seçiliyse değer ile hareketteki miktarla çarpılarak satış vergisi tutarı hesaplanır.  Vergi kodu, birim tabanlı bir vergi değilse değer, satış vergisi tutarını hesaplamak için bu vergi kodunun Menşei'ne uygulanan bir yüzdedir.     

11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. **Kaydet**'i seçin.

Microsoft Dynamics 365 Finance uygulamasının 10.0.22 sürümü itibarıyla [Vergi hizmetini](../../localizations/global-tax-calcuation-service-overview.md) kullanıyorsanız ve **Özellik yönetimi** çalışma alanında [**Birden çok KDV sicil numarasını destekle**](../../localizations/emea-multiple-vat-registration-numbers.md) özelliği etkinleştirilmişse vergi kodunun türünü belirtmek için **Vergi türü** alanını kullanabilirsiniz. Aşağıdaki değerler kullanılabilir:

- Standart KDV
- Düşürülen KDV
- %0 KDV
- Tüketim vergisi
- Diğer

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
