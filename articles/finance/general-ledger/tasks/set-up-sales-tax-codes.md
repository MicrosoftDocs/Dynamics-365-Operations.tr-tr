---
title: Satış vergisi kodlarını ayarlama
description: Bu konuda, Dynamics 365 Finance'da satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c7208fa65905fcc902d9c08b5b90178745e76d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815056"
---
# <a name="set-up-sales-tax-codes"></a>Satış vergisi kodlarını ayarlama

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
    - **Hesaplama** hızlı sekmesindeki Kaynak alanında Birim başına tutar seçiliyse, değer, hareketteki miktarla çarpılarak satış vergisi tutarı hesaplanır.  Vergi kodu birim tabanlı bir vergi değilse, değer, satış vergisi tutarını hesaplamak için bu vergi kodunun Kaynağına uygulanan yüzdedir.     
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. **Kaydet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]