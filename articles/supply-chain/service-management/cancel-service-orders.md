---
title: Servis siparişlerini iptal et
description: Bir servis siparişini veya servis siparişi satırını servis siparişinin kendisinden silebilir veya bir periyodik iş çalıştırarak birden çok servis siparişini iptal edebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce3cb9ebc3536ba1b333a7bef6b5c679e09d7516
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980423"
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


  


