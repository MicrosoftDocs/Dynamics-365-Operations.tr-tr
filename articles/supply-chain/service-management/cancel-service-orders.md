---
title: Servis siparişlerini iptal et
description: Bir servis siparişini veya servis siparişi satırını servis siparişinin kendisinden silebilir veya bir periyodik iş çalıştırarak birden çok servis siparişini iptal edebilirsiniz.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e75ed6e30ece1f4807ff036d831c269774d941a7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670986"
---
# <a name="cancel-service-orders"></a>Servis siparişlerini iptal et   

[!include [banner](../includes/banner.md)]


Bir servis siparişini veya servis siparişi satırını servis siparişinin kendisinden silebilir veya bir periyodik iş çalıştırarak birden çok servis siparişini iptal edebilirsiniz.


> [!NOTE]
> <P>Servis siparişinin aşaması iptal etmeye izin vermiyorsa, servis siparişinin madde gereksinimleri varsa veya servis siparişi zaten deftere nakledildiyse servis siparişi iptal edilemez.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Servis siparişini Servis siparişleri formundan iptal etme

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın. Servis siparişini seçin Eylem bölmesinde **Siparişi iptal et**'e tıklayın.

## <a name="cancel-a-service-order-line"></a>Servis siparişi satırını iptal etme

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın. İptal etmek istediğiniz satırı içeren servis siparişine çift tıklayın.

2.  İptal etmek istediğiniz servis siparişi satırını seçin ve **Sipariş satırı iptal et**'e tıklayarak satırın durumunu **İptal edildi** olarak değiştirin.


> [!TIP]
> <P>Bir servis siparişi satırının iptalini geri almak ve durumu yeniden <STRONG>Oluşturuldu</STRONG> olarak değiştirmek için <STRONG>İptali geri al</STRONG>'a tıklayın.</P>


## <a name="cancel-multiple-service-orders"></a>Birden çok servis siparişini iptal etme

1.  **Servis yönetimi** \> **Periyodik** \> **Servis siparişleri** \> **Servis siparişlerini iptal et**'e tıklayın.

2.  **Seç** düğmesine tıklayın.

3.  **Sorgu** formunda, **Ölçüt** sütununda iptal etmek istediğiniz servis siparişlerini seçin.

4.  **Sorgu** formunu kapatmak için **Tamam**'a tıklayın.

5.  İptal edilen servis siparişlerini gösteren bir bilgi günlüğü oluşturmak için **Bilgi Günlüğünü Göster** onay kutusunu işaretleyin.

6.  Bir servis siparişinin **İptal edildi** durumunu tersine çevirmek istiyorsanız, **İptali geri al** onay kutusunu seçin.

7.  **Tamam** seçeneğini tıklatın.

Seçilen servis siparişleri iptal edilir veya **İptal edildi** ilerleme durumları tekrar **İşlemde**'ye döndürülür.


> [!NOTE]
> <P><STRONG>İptali geri al</STRONG> onay kutusunu işaretlerseniz, <STRONG>İptal edildi</STRONG> ilerleme durumundaki servis siparişleri tersine çevrilir ve <STRONG>İşlemde</STRONG> ilerleme durumuna sahip servis siparişleri iptal edilmez.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]