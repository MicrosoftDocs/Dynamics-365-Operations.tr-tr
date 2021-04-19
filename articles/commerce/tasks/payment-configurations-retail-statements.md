---
title: " Perakende ekstreleri için ödeme yapılandırmaları"
description: Bu yordam, Ticaret ekstrelerinin oluşturulması ve nakledilmesini etkileyen Ticaret mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edd4a73523934e1fd70995c9275c564a50809957
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796718"
---
# <a name="payment-configurations-for-retail-statements"></a> Perakende ekstreleri için ödeme yapılandırmaları

[!include [banner](../includes/banner.md)]

Bu yordam, Ticaret ekstrelerinin oluşturulması ve nakledilmesini etkileyen Ticaret mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir.

Bu kayıt, USRT demo şirketini kullanır.

1. Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Eylem Bölmesinde Kurulum'a tıklayın.
5. Ödeme yöntemleri'ne tıklayın.
6. Nakil bölümünü genişletin veya daraltın.
7. Düzenle öğesine tıklayın.
    * Bu ödeme yöntemi için alınan tutarların genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.  
    * Bu ödeme yöntemi için alınan tutarların nakledileceği hesabı seçin.  
    * Alınan toplam hareket tutarı ile bu ödeme yöntemi için sayılan tutar arasındaki olası farkların nakledileceği bir hesap seçin.  
    * Bu alana, fark tutarının ne zaman başka bir fark hesabına nakledileceğini belirlemek için bir tutar girebilirsiniz. Bu özelliği büyük farkları izlemek için kullanabilirsiniz.  
    * "Maksimum fark tutarı" alanında belirlenen değerden daha yüksek olduğunda, alınan toplam hareket tutarı ile sayılan tutar arasındaki olası farkları nakletmek için bir hesap seçin.  
    * Bankaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.  
    * Bu alanda, bankaya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçebilirsiniz.  
    * Banka para nakil tutarlarının nakledileceği hesabı seçin.  
    * Bankaya nakledilen tutarları banka hesabına aktarırken kullanılacak banka hareketi türünü seçin.  
    * Kasaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.  
    * Kasya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.  
    * Kasaya nakil tutarlarının nakledileceği hesabı seçin.  
8. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]