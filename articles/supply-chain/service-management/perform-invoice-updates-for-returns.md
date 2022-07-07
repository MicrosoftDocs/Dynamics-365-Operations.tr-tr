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
ms.openlocfilehash: 32a108694c11a2ebd922a71d5c82691584bbb397
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014763"
---
# <a name="perform-invoice-updates-for-returns"></a>İadeler için fatura güncelleştirmeleri gerçekleştirme 

[!include [banner](../includes/banner.md)]


İade siparişi, iade edilen sipariş olarak işaretlenmiş bir satış siparişi türüdür. Bu nedenle, iade siparişler için fatura oluşturmak üzere **İade siparişleri** formu yerine **Tüm satış siparişleri** liste sayfası kullanılır. Bu işlev sipariş iadelerinin ve satış siparişlerinin aynı anda ve aynı kişi tarafından faturalanmasını isteyen kuruluşların iş süreçlerini destekler.

İade edilen maddenin faturası negatif bir tutar olduğu için buna alacak dekontu denir.

Fatura güncelleştirmesini toplu iş işlemesi için ayarladığınızda, **İade edilen sipariş** türündeki satış siparişi, siparişin sevk irsaliyesinin güncelleştirildiğini gösteren, **Alındı** iade satırı durumuna sahip olmalıdır.

## <a name="post-an-invoice-for-a-return-order"></a>İade siparişine ait bir faturayı deftere nakletme

1.  **Alacak hesapları** \> **Siparişler** \> **Tüm satış siparişleri** öğelerini tıklayın.

2.  **Sipariş türü** alanında **İade edilen sipariş** olarak görünen bir satış siparişi seçin.

3.  Eylem Bölmesinde, **Fatura** sekmesindeki **Oluştur** gurubunda **Fatura**'ya tıklayın.

4.  **Parametreler** sekmesinde **Deftere nakil** onay kutusunu seçin.

5.  Formdaki bilgileri gözden geçirerek gerekli düzeltmeleri yapın.

6.  **Tamam** seçeneğini tıklatın. Alacak dekontu deftere nakledilir.

## <a name="see-also"></a>Ayrıca bkz.

[İadeler için sevk irsaliyesi güncelleştirmeleri](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]