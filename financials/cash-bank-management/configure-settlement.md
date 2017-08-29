---
title: "Kapatma yapılandırma"
description: "Hareketlerin neden ve ne zaman kapatıldığı karmaşık konular olabilir. O yüzden, iş gereksinimlerinizi karşılayacak parametreleri doğru bir şekilde anlayıp tanımlamanız çok önemlidir. Bu makalede, hem Borç hesapları hem Alacak hesapları için kapanışta kullanılan parametreler açıklanmaktadır."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 059513de66827aa3a839b9eb06973ec4c1549f73
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="configure-settlement"></a>Kapatma yapılandırma

[!include[banner](../includes/banner.md)]


Hareketlerin neden ve ne zaman kapatıldığı karmaşık konular olabilir. O yüzden, iş gereksinimlerinizi karşılayacak parametreleri doğru bir şekilde anlayıp tanımlamanız çok önemlidir. Bu makalede, hem Borç hesapları hem Alacak hesapları için kapanışta kullanılan parametreler açıklanmaktadır. 

Aşağıdaki parametreler, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kapatmaların nasıl işleneceğini etkiler. Kapatma işlemi bir faturanın bir ödemeye veya bir alacak dekontuna karşılık kapatılmasını içerir. Bu parametreler **Alacak hesapları parametreleri** ve **Borç hesapları parametreleri** sayfalarının **Kapatma** alanında bulunur.

-   **Otomatik kapatma** – Nakledildiğinde bir hareketin diğer açık hareketlere karşılık otomatik olarak kapatılması gerekiyorsa bu seçeneği **Evet** konumuna ayarlayın. Bu seçenek **Hayır** olarak ayarlanırsa kullanıcılar, ödemeleri girdiğinde veya daha sonra **Hareketleri kapat** sayfasını kullanarak hareketleri el ile kapatabilirler.
-   **Nakit iskontosu yönetimi** – Bir [nakit iskontosunun fatura fazla ödendiğinde nasıl yönetileceğini belirtir](cash-discount-handling-overpayments.md). Fazla ödeme için, nakit iskontosu azaltılabilir, fark olarak kabul edilebilir veya satıcı veya müşteri hesabında kalabilir.
    -   **Belirsiz** – Nakit iskontosu tutarı, fazla ödeme tutarıyla giderilir. Bu davranış, fazla ödeme tutarının **Maksimum fazla ödeme veya eksik ödeme** alanına girilen miktardan fazla veya düşük olup olmamasından bağımsız olarak her zaman uygulanır.
    -   **Özel** – Fazla ödeme tutarı bir nakit iskontosu farkı defter hesabına nakledilir veya müşteri veya satıcı hesabında bir bakiye olarak kalır. Bu özel davranış, fazla ödeme tutarının 0.00 ile **Maksimum fazla ödeme veya eksik ödeme** alanında belirlenen tutar arasında olup olmadığına veya fazla ödeme tutarının **Maksimum fazla ödeme veya eksik ödeme** tutarından yüksek olup olmadığına göre değişir.
-   **Maksimum kuruş farkı** – Kapatılan hareketler için izin verilen maksimum kuruş farkını girin. Fark, bu alanda belirtilen kuruş farkına eşit veya daha düşükse fark, **Otomatik hareket hesapları** sayasında belirtilen kuruş farkı genel muhasebe hesabına nakledilecektir.
-   **Maksimum fazla ödeme veya eksik ödemedeki** – Fazla ödeme veya eksik ödeme olarak kabul edilecek tutarı girin. Fazla veya eksik ödemelerdeki vergiyi hesaplamak için, **Genel muhasebe parametreleri** sayfasında **Satış vergisi** öğesini tıklayın ve ardından **Fazla veya eksik ödemedeki satış vergisi** seçeneğini işaretleyin.
    -   Fazla ödeme veya eksik ödeme, **Maksimum kuruş farkı** alanında tanımlanan farktan daha az kuruş farkı oluşturursa, kuruş farkı tutarı kuruş farkı hesabına nakledilir.
    -   Fazla ödeme veya eksik ödeme, **Maksimum kuruş farkı** alanında tanımlanan farktan daha fazla bir fark üretiyorsa fark tutarı, **Otomatik hareketler için hesaplar** sayfasındaki **Müşteri nakit iskontosu** veya **Satıcı nakit iskontosu** nakil türü için seçilen fark hesabına nakledilir.
-   **Kısmi ödemeler için nakit iskontolarını hesapla** – Nakit iskontolarının kısmi ödemeler için otomatik olarak hesaplanmasını sağlamak için bu seçeneği **Evet** konumuna ayarlayın.
    -   Bu seçeneğin etkisi, **Hareketleri kapat** sayfasındaki **Nakit iskontosu kullan** alanının değerine bağlıdır. Bu seçenek **Evet** konumuna ayarlanırsa, **Nakit iskontosu kullan** alanı **Normal** konumuna ayarlandığında iskonto alınır. **Nakit iskontosu kullan** alanı **Her zaman** konumuna ayarlanırsa bu alanın ayarından bağımsız olarak her zaman nakit iskontosu alınır. **Nakit iskontosu kullan** alanı **Hiçbir zaman** konumuna ayarlanırsa bu alanın ayarından bağımsız olarak hiçbir zaman nakit iskontosu alınmaz.
    -   Bu seçenek **Evet** konumuna ayarlanırsa ve kullanıcı, **Hareketleri kapat** sayfasındaki **Kapatılacak tutar** alanındaki değeri değiştirirse, iskonto otomatik olarak hesaplanır ve **Alınacak nakit iskonto tutarı** alanında varsayılan giriş olarak görüntülenir.
    -   Bu seçenek **Hayır** olarak ayarlanırsa ve bir kullanıcı **Hareketleri kapat** sayfasındaki **Kapatılacak tutar** alanındaki bir değeri değiştirirse, **Alınacak nakit iskontosu tutarı** alanındaki varsayılan giriş **0** (sıfır) olur.
-   **Alacak dekontları için nakit iskontoları hesapla** – Alacak dekontları için bir nakit iskontosunu otomatik olarak hesaplamak için bu seçeneği **Evet** konumuna ayarlayın. Alacak hesaplarında bir alacak dekontu hareketi **Serbest metin faturası** sayfasındaki **Fatura** alanında bir değere veya **Satış emri** sayfasında bir iadeye sahip olan bir negatif harekettir.
    -   Bu seçeneğin etkisi, **Hareketleri kapat** sayfasındaki **Nakit iskontosu kullan** alanının değerine bağlıdır. Bu seçenek **Evet** konumuna ayarlanırsa, ****Nakit iskontosu**** kullan alanı **Normal** konumuna ayarlandığında iskonto alınır. ****Nakit iskontosu kullan**** alanı **Her zaman** konumuna ayarlanırsa bu alanın ayarından bağımsız olarak her zaman nakit iskontosu alınır. ****Nakit iskontosu kullan****alanı **Hiçbir zaman** konumuna ayarlanırsa bu alanın ayarından bağımsız olarak hiçbir zaman nakit iskontosu alınmaz.
    -   Bu seçenek **Evet** konumuna ayarlanır ve **Hareketleri kapat** sayfasında bir alacak dekontu işaretlenirse, iskonto otomatik olarak hesaplanır ve **Alınacak nakit iskonto tutarı** alanında varsayılan giriş olarak görüntülenir.
    -   Bu seçenek **Hayır** konumuna ayarlanırsa ve **Hareketleri kapat** sayfasında bir alacak dekontu işaretlenirse, **Alınacak nakit iskonto tutarı** alanındaki varsayılan giriş **0**'dır (sıfır).
-   **İskonto mahsup hesapları (yalnızca AP)** – Nakit iskontoları muhasebe girişi için kullanılacak varsayılan nakit iskontosu genel muhasebe hesabını tanımlayın.
    -   **Satıcı iskontoları için Ana hesabı kullan** – Nakit iskontosu **Nakit iskontosu kurulumu** sayfasında tanımlanan ana hesaba aktarılır.
    -   **Fatura satırlarındaki hesaplar** – Nakit iskontosu, orijinal fatura üzerindeki genel muhasebe hesaplarına nakledilir.
-   **Serbest metin faturalarındaki ve vade farkı dekontlarındaki satırları işaretle (yalnızca AR)** – Bu seçeneği **Evet** konumuna getirerek **Müşteri ödemelerini gir**, **Ödeme günlüğü fişi** ve **Hareketleri kapat** sayfalarındaki **Fatura satırlarını işaretle** düğmesini etkinleştirin. Bu düğme kullanıcının kapatma için tek tek satırları işaretlemesini sağlar.
-   **Kapatmaya öncelik belirle (yalnızca AR)** – Bu seçeneği **Evet** konumuna getirerek **Müşteri ödemelerini gir** ve **Hareketleri kapat** sayfalarındaki **Önceliğe göre işaretle** düğmesini etkinleştirin. Bu düğme, kullanıcıların önceden belirlenmiş kapama siparişlerini hareketlere atamalarını sağlar.  Bir harekete kapatma siparişi uygulandıktan sonra, sipariş ve ödeme tahsisatı deftere nakilden önce değiştirilebilir.
-   **Otomatik kapatmalar için öncelik kullan** – Hareketler otomatik kapatıldıklarında belirlenmiş önceliği kullanmak için bu seçeneği **Evet** olarak ayarlayın. Bu alan yalnızca **Kapanışa öncelik ver** ve **Otomatik kapanış** seçenekleri **Evet** olarak ayarlanmışsa kullanılabilir.





