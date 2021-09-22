---
title: Satış siparişleri hakkında sık sorulan sorular
description: Bu sayfada, Dynamics 365 Supply Chain Management'ta satış siparişleriyle çalışırken ortaya çıkan sık sorulan sorular ele alınmaktadır.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477839"
---
# <a name="sales-order-faqs"></a>Satış siparişi hakkında SSS

Bu sayfada, Dynamics 365 Supply Chain Management'ta satış siparişleriyle çalışırken ortaya çıkan sık sorulan sorular ele alınmaktadır.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Talebi karşılamak için bir satınalma siparişini bir satış siparişine bağlayabilir miyim?

Satış siparişinden satınalma siparişi oluşturabilirsiniz. Daha fazla bilgi için, bkz. [Satış siparişinden satınalma siparişi oluşturma](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Satış siparişini veya iade siparişini iptal edebilir miyim ya da silebilir miyim?

Yalnızca, *Oluşturuldu* durumundaki satış siparişlerini ve iade siparişlerini iptal edebilirsiniz. Daha fazla bilgi için bkz. [İade siparişlerini iptal etme](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Silinmiş bir faturalandırılmış satış siparişini geri yükleyebilir miyim?

Faturalanan bir satış siparişi yanlışlıkla silindiyse bunu geri yükleyebilir veya ayrıntılarını görüntüleyebilirsiniz.

**Müşteri hesabı \> Hareketler \> Özgün belge \> Ayrıntıları görüntüle**'ye gidin. Aradığınız faturayı bulun ve ayrıntılarını görüntülemek için seçin. Bu ayrıntılar satış siparişi referansını içerir. Ayrıca, bu sayfadan satış siparişi ayrıntılarına de erişebilmelisiniz.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Sahipsiz satış siparişi kayıtlarını nasıl silebilirim?

Sahipsiz satış siparişi kayıtlarını temizlemek için, aşağıdaki yerlerden birine giderek *Satış siparişi silme* dönemsel işini çalıştırın:

- Satış ve pazarlama \> Dönemsel görevler \> Temizle \> Satış siparişlerini sil
- Retail and commerce \> Retail and commerce IT \> Temizleme \> Satış siparişlerini sil

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Deftere nakledilmiş olan faturalardaki komisyonları hesaplanmanın bir yolu var mı?

Supply Chain Management, şu anda deftere nakledilen faturaların komisyonlarını hesaplamayı desteklememektedir.
