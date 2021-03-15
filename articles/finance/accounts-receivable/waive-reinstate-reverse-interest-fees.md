---
title: Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme
description: Bu makale, faiz ve masraflar için giderlerden nasıl feragat edileceğini, giderlerin nasıl eski durumuna getirileceğini ve tersine çevrileceğini açıklar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: roschlom
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080b46e69d9959f7a10a291552603f80071a934a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003243"
---
# <a name="waive-reinstate-or-reverse-interest-fees"></a>Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme

[!include [banner](../includes/banner.md)]

Bu makale, faiz ve masraflar için giderlerden nasıl feragat edileceğini, giderlerin nasıl eski durumuna getirileceğini ve tersine çevrileceğini açıklar.

Giderlerde feragat etmek, tersine çevirmek veya eski durumuna getirmek için **tüm müşteriler** liste sayfası **toplama** sekmesindeki düğmeleri kullanabilirsiniz:

-   Silinen giderler unutulur. Örneğin, bir müşteri gidere itiraz ederse ve o müşteri ile iyi iş ilişkileri sürdürmek istiyorsanız, giderden feragat edebilirsiniz.
-   Eski halin getirilen giderler yeniden son haline gelir. Daha önce feragat edilen giderleri eski haline getirebilirsiniz. Bunların feragat edilmemesi gerektiğini belirlerseniz, giderleri eski haline getirebilirsiniz.
-   Ters işlem ücretleri müşterinin hesabından kaldırılır ve artık vadesi gelmez. Örneğin, bir müşterinin borçlu olduğu tutarı hesaplamak için yanlış faiz oranı seçildiyse, giderleri ters çevirebilirsiniz. Faizi yeniden hesaplamak ve müşteri için yeni ücretleri içeren bir vade farkı dekontu oluşturmak için ayrı bir işlem kullanabilirsiniz.

Bu eylemler bir vade farkı dekontunu değiştirir. Vade farkı dekontu faiz veya ücretlerin ne zaman hesaplarına yüklendiğini müşterilere bildiren bir iş belgedir. Faiz ve ücretleri feragat ederken veya ters çevirirken ücretleri kapatmak için bir borç dekontu veya fatura ayarlama otomatik olarak oluşturulur. Feragat giderleri eski durumuna getirirseniz, borç tutarı olan fatura müşterinin borçlu olduğu giderler yeniden başlatmak için otomatik olarak oluşturulur. Aşağıdaki tabloda her eylemin sonuçları açıklanmıştır.

| Eylem                                                                                                                                                                                                            | Müşteri için sonuç                                                                                             | İşle                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tüm vade farkı dekontlarının vade farkı ve içerdikleri ücretleri feragat edin. – veya – Masrafları veya vade farkı dekontları parçası olan vade farkı işlemleri seçin ve feragat edin.                                        | Giderler unutulur.                                                                                           | Bir borç dekontu veya ayarlama fatura müşteri için oluşturulur. Kredi, vade farkı dekontu veya vade farkı işlemleri veya seçtiğiniz ücretleri otomatik olarak kapatmak için kullanılmaz. Kapatılan tutar müşterinin yaptığı herhangi bir önceki ödeme eksi ve daha önce feragat edilen veya yazılmış tutarları eksi giderler toplam miktarına eşittir. Alacak dekontunun tutarı müşterinin borçlu olduğu tutarı aşarsa, alacak dekontunu bir satıcı faturası dönüştürebilirsiniz. Müşteriye sonra para iadesi verebilirsiniz.                                                       |
| Tüm vade farkı dekontlarının vade farkı ve içerdikleri ücretleri eski haline getirir. – veya – Masrafları veya vade farkı dekontları parçası olan vade farkı işlemleri seçin ve eski haline getirin.                                | Feragat edilen tutar yeniden vadeli olur.                                                                                     | Borç tutarı içeren bir fatura oluşturulur ve tutarı önceden feragat edilen masraflara karşı otomatik olarak kapatılır. Gerçek vade farkı dekontları eski haline getirilmez. Bunun yerine, müşteriden kalan tutarı gösteren bir fatura oluşturulur. Vade farkı dekontları kapatılacak kullanılmamışsa, alacak dekontları veya feragat edilen vade farkı dekontları kapatmak için oluşturulan ayarlama faturaları hâlâ varolabilir. Bu durumda, bekleyen alacak dekontları iptal edilir. Vade farkı dekontları feragat edildiğinde, bekleyen alacak dekontları genellikle otomatik olarak kapatılır. Ancak, bir müşteriye bir vade farkı dekontu ödendiği takdirde müşteri ücretlere itiraz etmesine rağmen bekleyen bir alacak dekontu varolmayabilir. |
| Tüm vade farkı dekontlarını tersine çevirin. – veya – Seçilen vade farkı dekontları parçası olan vade farkı işlemleri ters çevirin. **Not:** Bir ücreti ters çeviremezsiniz. Ancak, bir ücret içeren bir tüm vade farkı dekontunu ters çevirebilirsiniz. | Giderleri artık müşterinin ödemesi gerekmez. Ancak faizi yeniden hesaplarsanız giderler yeniden vadeli hale gelir. | İşlem vade farkı dekontları veya seçili vade farkı işlemleri feragat işlemi için aynıdır. Bir borç dekontu veya ayarlama fatura müşteri için oluşturulur. Bu kredi notu, otomatik olarak vade farkı dekontu kapatmak için kullanılır. Faiz yeniden hesaplamak ve yeni bir vade farkı dekontu oluşturmak için ayrı bir işlem kullanabilirsiniz.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Ödenmeyen borçlar yazmak için ayrı bir işlem de kullanabilirsiniz. Bu işlem, yalnızca vade farkı dekontlarının parçası olan giderlerde feragat etmek yerine tüm müşteri hareketlerini kapatılmak üzere işaretler.

## <a name="adjust-interest-for-invoices"></a>Faturalar için faiz ayarla
Vade farkı dekontları ayarlamaya ek olarak, aşağıdaki işlemlerden birini kullanarak faturalarda faiz giderlerini kaldırabilirsiniz. Her iki işlem de ilgili vade farkı dekontları düzenlemeler yapar.

### <a name="correct-an-invoice-that-has-associated-interest"></a>İlişkili faizi olan faturayı düzeltme

Bir vade farkı dekontundaki deftere nakledilen bir faturayı düzeltebilirsiniz. Bu işlem, varolan faturadan istediğiniz düzeltmeler yapmak için yeni bir fatura ayrıntıları kopyalar. Fatura iptal edilir ve yeni bir fatura oluşturulur. Vade farkı dekontunu deftere nakledilmişse faiz hareketi de vade farkı dekontunda tersine çevrilir. 

Serbest metin faturasının Eylem Bölmesindeki **doğru fatura** düğmesini kullanarak düzeltme yapabilirsiniz. Bu düğme sadece **Serbest metin fatura düzeltmesi** konfigürasyon anahtarı seçiliyse kullanılabilir.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Faiz ilişkili müşteri hareketini ters çevirin

Fatura hatalı oluşturulmuşsa bir faturada müşteri hareketini ters çevirebilirsiniz. Tersine çevrilen müşteri hareketi bir vade farkı dekontuna dahil edilen faiz varsa ve vade farkı dekontunu deftere nakledilmişse, hareket üzerinde faiz de vade farkı dekontundaki tersine çevrilir. Vade farkı dekontunu deftere taşınmazsa iptal edilir. 

Müşteri hareketlerini **müşteri hareketleri** sayfasındaki **ters** düğmesini kullanarak ters çevirebilirsiniz.

## <a name="waive-or-reinstate-interest-notes"></a>Vade farkı dekontlarını feragat et veya eski duruma getir
Seçtiğiniz vade farkı dekontları üzerindeki tüm giderler feragat edebilir veya eski haline getirebilirsiniz. Ücretleri feragat ettiğinizde, feragat edilen toplam tutar ayarlanmış olan tüm tutar limitlerini aşamaz. Sadece bunu daha önce feragat edilmiş bir vade farkı dekontunu eski durumuna getirebilirsiniz. 

**müşteri** sayfasındaki **toplama** sekmesinde **vade farkı dekontu** düğmesini kullanarak vade farkı dekontlarını feragat edebilir veya eski durumuna getirebilirsiniz.

## <a name="waive-or-reinstate-interest-transactions"></a>Faiz hareketlerinden feragat etme, bunları eski durumuna getirme veya tersine çevirme
Bu faiz dekontundaki tüm giderleri ayarlama yerine bir vade farkı dekontundaki belirli vade farkı işlemlerden feragat edebilir veya eski durumuna getirebilirsiniz. Ücretleri feragat ettiğinizde, feragat edilen toplam tutar ayarlanmış olan tüm tutar limitlerini aşamaz. Sadece bunu daha önce feragat edilmiş bir vade farkı işlemini eski durumuna getirebilirsiniz. 

**müşteri** sayfasındaki **toplama** sekmesinde **İşlem faizi** düğmesini kullanarak vade farkı dekontlarını feragat edebilir veya eski durumuna getirebilirsiniz.

## <a name="waive-or-reinstate-fees"></a>Ücretlerden feragat et veya eski durumuna getir
Bu faiz dekontundaki tüm giderleri ayarlama yerine bir vade farkı dekontundaki belirli ücretlerden feragat edebilir veya eski durumuna getirebilirsiniz. Ücretleri feragat ettiğinizde, feragat edilen toplam tutar ayarlanmış olan tüm tutar limitlerini aşamaz. Sadece bunu daha önce feragat edilmiş bir ücreti eski durumuna getirebilirsiniz. 

**müşteri** sayfasındaki **toplama** sekmesinde **Ücret** düğmesini kullanarak vade farkı dekontlarını feragat edebilir veya eski durumuna getirebilirsiniz.

## <a name="reverse-interest-notes"></a>Vade farkı dekontlarını tersine çevir
Seçtiğiniz vade farkı dekontları üzerindeki tüm giderleri ters çevirebilirsiniz. Ters işlem ücretleri müşterinin hesabından kaldırılır ve artık vadesi gelmez. Vade farkı dekontu ters çevrildikten sonra, faiz yeniden hesaplayabilir ve yeni bir vade farkı dekontu oluşturabilirsiniz. 

**müşteri** sayfasındaki **toplama** sekmesinde **vade farkı dekontu** düğmesini kullanarak vade farkı dekontlarını ters çevirebilirsiniz.

## <a name="reverse-interest-transactions"></a>Faiz hareketlerini tersine çevir
Seçtiğiniz tüm faiz işlemlerini ters çevirebilirsiniz. Ters işlem ücretleri müşterinin hesabından kaldırılır ve artık vadesi gelmez. İşlemler ters çevrildikten sonra, faiz yeniden hesaplayabilir ve yeni bir vade farkı dekontu oluşturabilirsiniz.

**müşteri** sayfasındaki **toplama** sekmesinde **İşlem faizi** düğmesini kullanarak faiz işlemlerini ters çevirebilirsiniz.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Feragat edilmiş, eski durumuna getirilmiş veya ters çevrilmiş giderler için ayarlamalar geçmişini görüntüleyin
Ayarlamayı giren kullanıcı, ayarlama türü, tutar ve ayarlamanın ne zaman girildiği gibi vade farkı dekontları için yapılan ayarlamaların ayrıntılı geçmişini görüntüleyebilirsiniz. Örneğin, yeni bir vade farkı dekontu oluşturmadan önce bir vade farkı dekontu için girilen önceki ayarlamaları görüntülemek isteyebilirsiniz. 

**müşteri** sayfasındaki **toplama** sekmesinde **Geçmiş** düğmesini kullanarak faiz işlemlerini ters çevirebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]