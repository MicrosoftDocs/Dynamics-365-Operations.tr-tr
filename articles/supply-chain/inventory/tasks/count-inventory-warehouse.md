---
title: Ambardaki stoğu sayma
description: Bu konu, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7f85cb91f36004a6bd6da714e7baa460a83a66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000119"
---
# <a name="count-inventory-in-a-warehouse"></a>Ambardaki stoğu sayma

[!include [banner](../../includes/banner.md)]

Bu konu, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini açıklar. Yordam, "temel depolama" işlevi içindir ve Stok Yönetimi modülünde yer alır; Ambar Yönetimi modülünde bulunan ambarlama işlevi için geçerli değildir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz. Kendi verilerinizi kullanıyorsanız, ürünlerin ve yerleşimlerin ayarlandığından ve sayım günlükleri için bir stok günlüğü adı oluşturduğunuzdan emin olun. Stok sayımı normalde bir ambar çalışanı tarafından gerçekleştirilir.


## <a name="create-an-inventory-counting-journal"></a>Stok sayım günlüğü oluşturma
1. **Gezinti bölmesi > Modüller > Stok yönetimi > Günlük girişleri > Ürün sayımı > Sayım**'a gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanında açılır listeden kullanmak istediğini stok sayımı günlük adını seçin. Diğer bazı alanlar, seçtiğiniz stok sayımı günlük adı kurulumu temel alınarak doldurulur.  
4. **Çalışan** alanında, aramayı açmak için açılır menü düğmesini seçin.
5. Listede kullanmak istediğiniz çalışanı **Seçin**.
6. **Tamam**'ı seçin.

## <a name="create-journal-lines"></a>Günlük satırları oluştur
1. **Yeni**'yi seçin.
2. **Madde numarası** alanında, açılır menü listesinden istediğiniz kaydı seçin. Demo verileri şirket USMF'yi kullanıyorsanız, **A0001** öğesini seçin.  
3. **Tesis** alanında, açılır menü listesinden istediğiniz kaydı seçin. Demo verileri şirket USMF'yi kullanıyorsanız, tesis **2** öğesini seçin.
4. **Ambar** alanında, açılır menü listesinden istediğiniz kaydı seçin. Demo verileri şirket USMF'yi kullanıyorsanız, ambar **24** öğesini seçin.  
5. **Konum** alanında, açılır menü listesinden istediğiniz kaydı seçin. Demo verileri şirket USMF'yi kullanıyorsanız, yerleşim **BULK-001** öğesini seçin.  
6. Sayılan alanında bir sayı girin. **Eldeki ürün** alanında gösterilen sayıdan farklı bir sayım rakamı girerseniz **Miktar** alanı uyuşmazlığı gösterecek şekilde güncelleştirilir.  
7. **Kaydet**'i seçin.

## <a name="post-the-inventory-counting-journal"></a>Stok sayım günlüğünü deftere nakletme
1. **Naklet**'i seçin. Bir stok sayım günlüğünü deftere naklettiğinizde, sayım miktarı **Eldeki ürün** alanında belirtilenden farklıysa deftere bir stok girişi veya sorun nakledilir, stok düzeyi ve değer değiştirilir ve genel muhasebe hareketleri oluşturulur.
2. **Tamam**'ı seçin.

## <a name="view-inventory-transactions"></a>Stok hareketlerini görüntüle
1. **Stok**'u seçin.
2. **Hareketler**'i seçin. Burada, stok sayım günlüğünüzü deftere naklettiğinizde oluşturulacak tüm ilgili hareketleri görebilirsiniz.   

