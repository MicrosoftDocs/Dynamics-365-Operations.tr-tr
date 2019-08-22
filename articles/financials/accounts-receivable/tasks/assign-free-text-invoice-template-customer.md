---
title: Bir müşteriye serbest metin faturası şablonu atayın
description: Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53bff33083a78c0bb1c7d243fe9965fb264d209e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843061"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Bir müşteriye serbest metin faturası şablonu atayın

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir. USMF demo şirketinin kullanıldığı bu görev, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.

1. Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Eylem Bölmesinde, Fatura öğesine tıklayın.
4. Yinelenen faturalar'a tıklayın.
    * Müşterilere serbest metin faturası şablonları atamak ve faturaların müşterilere ne sıklıkta gönderileceğini belirlemek için bu sayfayı kullanın.  
5. Müşteriye yeni şablon atamak için Yeni'ye tıklayın.
6. Müşteriye atamak istediğiniz serbest metin faturası şablonunu seçin.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. İlk faturanın oluşturulacağı tarihi girin.
    * Bir yineleme bitiş tarihi girin.  
    * Şunlardan birini seçin: Bitiş tarihi yok – Faturalar sonsuz olarak oluşturulur ve şablon müşteri hesabından kaldırılana kadar geçerli kalır.  Faturalama bitiş tarihi – Bu seçeneği belirtin ve faturanın oluşturulabileceği son tarihi girin.  
    * Fatura oluşturmayı sona erdirecek maksimum toplam tutar.  
    * Seçili şablon kullanarak erişilebilen maksimum toplam tutarı girin. Örneğin 1000,00 girer ve her biri 100,00 tutarında aylık faturalar oluşturursanız, onuncu fatura oluşturulduktan sonra fatura oluşturma süreci sona erer.  
    * Serbest metin faturası şablonundan veya müşteri hesabından alınan varsayılan değerleri kullanarak yinelenen faturalar oluşturun.  
    * Faturaları oluştururken dil, deftere nakil profili, satış vergisi grubu, madde satış vergisi grubu, liste kodu, teslimat ülkesi/bölgesi, ödeme koşulları, para birimi, ödeme koşulları, ödeme yöntemi, ödeme belirtimi, ödeme planı, nakit iskontosu, mali boyutlar ve havale makbuzu için varsayılan değerleri belirlemek üzere serbest metin faturası şablonunu veya müşteri hesabını kullanın.  
10. Yineleme şablonunu seçin.
    * Günlük – Bu seçeneği belirtin ve Dönem alanına gün sayısını girin. Örneğin 15 girerseniz, bu müşteri için 15 günde bir fatura oluşturulur.  Haftalık – Bu seçeneği belirtin Dönem alanına hafta sayısını girin. Örneğin 2 girerseniz, bu müşteri için 2 haftada bir fatura oluşturulur.  Aylık – Bu seçeneği belirtin ve Dönem alanına ay sayısını girin. Örneğin 6 girerseniz, bu müşteri için her altı ayda bir fatura oluşturulur.  Yıllık – Bu seçeneği belirtin ve Dönem alanına yıl sayısını girin. Örneğin 2 girerseniz, bu müşteri için her iki yılda bir fatura oluşturulur.  
11. Dönem alanına bir sayı girin.

