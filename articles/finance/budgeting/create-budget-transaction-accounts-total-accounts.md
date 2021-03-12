---
title: İşlem hesapları ve toplam hesaplar için bütçe oluşturma
description: Bu makalede, toplam hesaplara göre bütçe oluşturma işlemine genel bir bakış verilmektedir. Makalede, bütçe kontrolü gerektiği zaman toplam hesaplar için bütçe kontrolünün nasıl etkinleştirileceği de açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c2298a774e35bc92fafb8bc24871b288fb198d7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003093"
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



