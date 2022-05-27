---
title: İadeler için fatura güncelleştirmeleri gerçekleştirme
description: Bu işlev sipariş iadelerinin ve satış siparişlerinin aynı anda ve aynı kişi tarafından faturalanmasını isteyen kuruluşların iş süreçlerini destekler.
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
ms.openlocfilehash: 2f999dec6639183015b1be9378dc4e8ea01c9a84
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670902"
---
# <a name="perform-invoice-updates-for-returns"></a>İadeler için fatura güncelleştirmeleri gerçekleştirme 

[!include [banner](../includes/banner.md)]


İade siparişi, iade edilen sipariş olarak işaretlenmiş bir satış siparişi türüdür. Bu nedenle, iade siparişler için fatura oluşturmak üzere **İade siparişleri** formu yerine **Tüm satış siparişleri** liste sayfası kullanılır. Bu işlev sipariş iadelerinin ve satış siparişlerinin aynı anda ve aynı kişi tarafından faturalanmasını isteyen kuruluşların iş süreçlerini destekler.

İade edilen maddenin faturası negatif bir tutar olduğu için buna alacak dekontu denir.

Fatura güncelleştirmesini toplu iş işlemesi için ayarladığınızda, **İade edilen sipariş** türündeki satış siparişi, siparişin sevk irsaliyesinin güncelleştirildiğini gösteren, **Alındı** iade satırı durumuna sahip olmalıdır.

## <a name="post-an-invoice-for-a-return-order"></a>İade siparişine ait bir faturayı deftere nakletme

1.  **Alacak hesapları** \> **Genel** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne tıklayın.

2.  **Sipariş türü** alanında **İade edilen sipariş** olarak görünen bir satış siparişi seçin.

3.  Eylem Bölmesinde, **Fatura** sekmesindeki **Oluştur** gurubunda **Fatura**'ya tıklayın.

4.  **Parametreler** sekmesinde **Deftere nakil** onay kutusunu seçin.

5.  Formdaki bilgileri gözden geçirerek gerekli düzeltmeleri yapın.

6.  **Tamam** seçeneğini tıklatın. Alacak dekontu deftere nakledilir.

## <a name="see-also"></a>Ayrıca bkz.

[İadeler için sevk irsaliyesi güncelleştirmeleri](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]