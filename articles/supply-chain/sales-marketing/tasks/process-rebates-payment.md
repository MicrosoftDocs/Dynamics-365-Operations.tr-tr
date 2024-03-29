---
title: Ödeme için indirimleri işleme
description: Bu yordam, onaylanmış ve işlenmiş müşteri indirimlerini alacak dekontlarına dönüştürmeyi göstermektedir.
author: Henrikan
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce813f0f5d9aa750828b524dd9fdf9b4a9f0854
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572493"
---
# <a name="process-rebates-for-payment"></a>Ödeme için indirimleri işleme

[!include [banner](../../includes/banner.md)]

Bu yordam, onaylanmış ve işlenmiş müşteri indirimlerini alacak dekontlarına dönüştürmeyi göstermektedir. Bu kılavuzu USMF demo şirketinde kullanabilirsiniz. Bu kılavuz için önkoşul İşaretli duruma sahip bir veya daha fazla indirim talep olmasıdır. USMF kullanıyorsanız,"Müşteri indirimleri oluştur ve işle" kılavuzunu bu kılavuza başlamadan önce işleyin.


## <a name="convert-rebate-claims-to-credit-note"></a>Alacak dekontunu indirim talebine dönüştürme
1. Tüm müşteriler'e gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Eylem Bölmesinde, Tahsil et'e tıklayın.
5. Hareketleri kapat'a tıklayın.
6. İşlevler'i tıklatın.
7. İndirim programı'na tıklayın.
    * Bu indirim sayfası müşteri indirim çalışma ekranında işlediğiniz ve İşaretli durumda olan indirim taleplerini listeler.    
8. Düzenle öğesine tıklayın.
    * Alacak dekontuna dahil etmek istediğiniz talepler için İşaretle alanında onay işaretleri koyun.   
9. İşlevler'i tıklatın.
10. Alacak dekontu oluşturma'ya tıklayın.
    * Bir günlüğün nakledildiğini bildiren bir ileti görüntülenir (Alacak hesapları parametreleri sayfasında belirtildiği gibi bu, alacak hesapları tüketim günlüğüdür). Bu işlem gerçek borç (alacak) tutarının müşteri bakiyesine aktarılmasına neden olur. Yani müşterinin hesabına alacak kaydedildiği ve İndirim tahakkuk hesabına borç kaydedildiği anlamına gelir.  
11. Sayfayı kapatın.
12. İptal'e tıklayın.
    * Güncelleştirmeleri görebilmeniz için sayfayı yeniler.  
13. Eylem Bölmesinde, Tahsil et'e tıklayın.
14. Hareketleri kapat'a tıklayın.
    * Toplam indirim miktarını temsil eden negatif bir miktar hareketinin, fatura referansı olmadan müşterinin hesabına eklendiğini unutmayın.   
15. İptal'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]