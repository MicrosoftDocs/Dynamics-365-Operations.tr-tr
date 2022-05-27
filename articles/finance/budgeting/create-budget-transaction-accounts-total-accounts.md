---
title: İşlem hesapları ve toplam hesaplar için bütçe oluşturma
description: Bu makalede, toplam hesaplara göre bütçe oluşturma işlemine genel bir bakış verilmektedir. Makalede, bütçe kontrolü gerektiği zaman toplam hesaplar için bütçe kontrolünün nasıl etkinleştirileceği de açıklanmaktadır.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: kfend
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33f7e49c56a5780644023b6b4fdcbc0937f7f90b
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714411"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>İşlem hesapları ve toplam hesaplar için bütçe oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede, toplam hesaplara göre bütçe oluşturma işlemine genel bir bakış verilmektedir. Makalede, bütçe kontrolü gerektiği zaman toplam hesaplar için bütçe kontrolünün nasıl etkinleştirileceği de açıklanmaktadır.

Hem bütçe planı hem bütçe kaydı giriş belgeleri, ana hesap türü **Toplam** olan ana hesaplarda bütçe oluşturulmasına izin verir. Fiziksel emtialar yalnızca işlem ana hesaplarına nakledilebilir. 

**Genel defterden genel bütçe planı** periyodik işlemi için, **Kaynak** sekmesi için **Toplam** ana hesap tipini bir kriter olarak belirleyebilirsiniz. Bu durumda, her bir toplam ana hesap hedef bütçe planında yer alacak ve miktar, seçilen ana hesap aralığındaki toplam miktara eşit olacaktır. 

**Toplam** türündeki ana hesaplar için bütçe kontrolünü etkinleştirebilirsiniz. Bu işlev, bütçe gruplarının kullanımıyla desteklenir. Her bir toplam an hesap için, bir bütçe grubu için kontrol edilmiş olan bütçe, **Bütçe denetim yapılandırma** sayfasında oluşturulmalıdır. Belirlediğiniz kriter, toplam ana hesabı ve hesap aralığını içermelidir. Bütçe grupları oluşturma işlemini hızlandırmak için, Bütçe kontrol grupları veri varlığından yararlanabilirsiniz. 

Raporlamada, örneğin bir mali tabloda bir bütçe kullanılıyorsa toplam hesap için bütçe toplamı şu hesaplardan meydana gelir:

-   Toplam hesap aralığında her bir işlem defter hesabından oluşturulan bütçeler.
-   Toplam hesaba doğrudan girilen bütçe tutarı.

Bu nedenle, toplam hesap aralığındaki en önemli işlem hesapları için ayrı bütçeler oluşturabilir ve mevcut bütçe tutarını toplam hesaba ekleyebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
