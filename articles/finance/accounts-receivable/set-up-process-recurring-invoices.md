---
title: Yinelenen faturalar oluşturma ve işleme
description: Bu makalede, yinelenen faturaların nasıl ayarlanıp işleneceği açıklanmaktadır. Müşterilere düzenli olarak aynı tutar için fatura kesmeniz gerekiyorsa, yinelenen faturalar kullanabilirsiniz.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce734567f0c5bf02e30c36484449c3869b82dc84
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724769"
---
# <a name="set-up-and-process-recurring-invoices"></a>Yinelenen faturalar oluşturma ve işleme

[!include [banner](../includes/banner.md)]

Bu makalede, yinelenen faturaların nasıl ayarlanıp işleneceği açıklanmaktadır. Müşterilere düzenli olarak aynı tutar için fatura kesmeniz gerekiyorsa, yinelenen faturalar kullanabilirsiniz.

## <a name="create-a-recurring-free-text-invoice-template"></a>Bir yinelenen serbest metin faturası şablonu oluşturun

Müşterilere düzenli olarak tekrarlanan aynı hizmetler için fatura düzenlemek için, faturaların oluşturulması için yeniden oluşturulabilen bir serbest metin faturası şablonu tanımlamanız gerekir. Bu şablon şu bilgiler içerir:

-   Vergi grupları, ödeme süreleri ve ödeme yöntemi gibi başlık bilgileri
-   Hizmet açıklaması, gelir hesapları, birim fiyatı ve fatura tutarı gibi satırı bilgileri
-   Sevkiyat veya işleme giderleri
-   Maliyet merkezleri ve iş birimleri gibi mali boyut bilgilerinin yanı sıra hesap dağıtımları

Pratikte, tüm bir fatura oluşturur ve bunu şablon olarak kaydedersiniz. **Yinelenen faturalar** sayfasını kullanarak şablonlar oluşturabilirsiniz.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Bir müşteriye bir serbest metin fatura şablonu atayın ve yineleme bilgilerini girin
Şablon oluşturulduktan sonra faturalamak istediğiniz müşteriler için şablon atamanız gerekir. Ayrıca, faturanın ne zaman ve ne sıklıkla kullanılacağını da belirtmelisiniz. **Müşteriler** sayfasındaki **Fatura** sekmesindeki şablonları atayabilirsiniz. Şablonu listeye ekleyin ve aşağıdaki bilgileri güncelleştirin:

-   Yinelenen faturalama için başlangıç tarihi ve isteğe bağlı olarak bitiş tarihi
-   Yineleme faturasının sıklığı (öreğin her gün veya ayda bir)
-   Maksimum faturalama tutarı (bu bilgiler gerekiyorsa)

Bir müşteri, farklı sıklıklara sahip, birden fazla şablona sahip olabilir.

## <a name="generate-the-recurring-invoices"></a>Yinelenen faturalar oluşturma
**Yinelenen faturalar** sayfasında, yinelenen fatura şablonlarının işlenmesi için bir görev mevcuttur. Fatura tarihini ve faturaların oluşturulacağı şablonu belirtirsiniz. Faturalar oluşturulur ve işlenen her bir fatura grubu için tek bir yineleme kimlik numarası atanır.

## <a name="post-recurring-free-text-invoices"></a>Yinelenen serbest metin faturalarını nakletme

Yinelenen faturalar oluşturulduktan sonra fatura yineleme kimlikleri **Yinelenen faturalar** sayfasındaki bir nakil görevinde görüntülenir. Bağlantıyı tıklayarak bir yineleme kimliği için faturaların tümünü görüntüleyebilirsiniz. Yineleme kimliği için faturaları gözden geçirerek faturaları ayrı ayrı silebilirsiniz. Müşterinin yineleme ayarları o şablon için sıfırlanır ve böylece daha sonra yeniden oluşturulabilir. Bir yineleme kimliği için faturaların biri, birden fazlası veya tümü nakledilebilir. İş akışları etkinleştirilirse, faturaları nakletmeden önce mutlaka **Gönder** düğmesini tıklamalısınız.

## <a name="print-recurring-free-text-invoices"></a>Yinelenen serbest metin faturalarını yazdırma

Yinelenen faturalar nakledildikten sonra serbest metin faturası listesi sayfasından faturaları yazdırabilirsiniz. Seçili faturaları yazdırabilirsiniz veya yazdırmak üzere bir seri fatura seçebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
