---
title: "Bir fiş"
description: "Mali günlükler için Bir fiş (yevmiye fişi, sabit kıymet günlüğü, satıcı ödeme günlüğü vb.), tek bir fiş bağlamında birden fazla yardımcı defter hareketi girmenizi sağlar."
author: kweekley
manager: AnnBe
ms.date: 03/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3831a6b5ec458495134b4b490d33a9acd76b6d2e
ms.openlocfilehash: 76ea8470786bd50896400a65564d698d96119d6f
ms.contentlocale: tr-tr
ms.lasthandoff: 03/20/2018

---

# <a name="one-voucher"></a>Bir fiş

[!include[banner](../includes/banner.md)]

> [!NOTE]
>  Bu işlev, 2018 yılı bahar aylarında piyasaya sunulacak olan Dynamics 365 for Finance and Operations sürüm 8.0'da kullanılabilir.   

<a name="what-is-one-voucher"></a>"Bir fiş" nedir?
======================

Mali günlükler için (yevmiye fişi, sabit kıymet günlüğü, satıcı ödeme günlüğü vb.) mevcut işlev, tek bir fiş bağlamında birden fazla yardımcı defter hareketi girmenizi sağlar. Bu işlevi "Bir fiş" olarak adlandırıyoruz. Bir fiş'i aşağıdaki yöntemlerden birini kullanarak oluşturabilirsiniz:

-   Günlük adını (**Genel muhasebe** \> **Günlük ayarı** \>**Günlük adları**), **Yeni fiş** alanı **Yalnızca bir fiş numarası** olacak şekilde ayarlayın. Günlüğe eklediğiniz her satır artık aynı fişte yer alır. Her satır aynı fişe eklendiğinden fiş, aynı satırda bir hesap/mahsup hesap veya birleşimi olarak çok satırlı bir fiş şeklinde girilebilir.

[![Tek satır](./media/same-line.png)](./media/same-line.png)

-   Mahsup hesabın olmadığı çok satırlı bir fiş girin.

[![Çok satırlı fiş](./media/Multi-line.png)](./media/Multi-line.png)

-   Hesabın ve mahsup hesabın satıcı/satıcı, Müşteri/müşteri, satıcı/müşteri veya banka/banka gibi bir yardımcı defter hesap türü içerdiği bir fiş girin.

[![Yardımcı defter fişi](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Bir fiş ile ilgili sorunlar
=======================

Bir fiş işlevi; hesap kapatma, vergi hesaplaması, yardımcı defterin genel muhasebeye mutabakatı, mali raporlama ve daha fazlası sırasında sorunlara neden olur. (Örneğin, hesap kapatma sırasında meydana gelen sorunlar hakkında daha fazla bilgi için bkz. [Birden fazla müşteri veya satıcı kaydına sahip tek bir fiş](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Düzgün bir şekilde çalışmak ve raporlamak için bu işlemler ve raporlar, hareket ayrıntıları gerektirir. Bazı senaryolar, kuruluşunuzun kurulumuna bağlı olarak yine de düzgün çalışmaya devam etse de; bir fişte birden çok hareket girildiğinde çoğunlukla sorunlar oluşur.

Örneğin, aşağıdaki fişi deftere naklettiğinizi düşünelim.

[![Örnek](./media/example.png)](./media/example.png)

Daha sonra **Mali Bilgiler** çalışma alanında, **Satıcıya göre giderler** raporunu oluşturursunuz. Rapor, gider hesap bakiyelerini satıcı grubu ve ardından satıcı altında gruplar. Rapor oluşturulurken, sistem 250,00 tutarındaki giderin hangi satıcı grupları/satıcılar tarafından tahakkuk edildiğini belirleyemez. Hareket ayrıntıları eksik olduğundan sistem, 250,00 tutarının tamamının fişte bulunan ilk satıcı tarafından tahakkuk edildiğini varsayar. 600120 numaralı ana hesap bakiyesine dahil olan 250,00 tutarı, o satıcı grubu/satıcı altında gösterilir. Fişteki ilk satıcı, çok yüksek olasılıkla doğru satıcı olmayacağından rapor yanlıştır.

[![Gider](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Bir fiş'in geleceği
=========================

Daha önce belirtilen sorunlar nedeniyle, Bir fiş işlevselliği geçersiz duruma getirilecektir. Ancak bu işleve bağlı olan işlevsel boşluklar olduğundan, işlev aynı anda tamamen geçersiz olmayacaktır. Bunun yerine, aşağıdaki planı kullanacağız: 

-   **2018 İlkbahar sürümü**: İşlev, Genel muhasebe parametresi aracılığıyla kapatılacaktır. Ancak kuruluşunuzun, bu konunun ilerleyen bölümlerinde listelenen iş senaryosu boşluklarına denk gelen bir senaryosu varsa işlevi açabilirsiniz.

    -   Bir fiş gerektirmeyen bir iş senaryonuz varsa işlevi açmayın. Başka bir çözüm varken bu işlev kullanılırsa bu konunun ilerleyen bölümlerinde tanımlanan alanlardaki "hataları" düzeltmeyeceğiz.

    -   İşlevsel boşluklardan biri için gerekli olmadıkça Microsoft Dynamics 365 Finance and Operations tümleştirmelerinde Bir fiş'i kullanmayı bırakın.

-   **2018 Sonbahar ve sonraki sürümler**: İşlevsel boşluklar doldurulacaktır. İşlevsel boşluklar doldurulduktan sonra Bir fiş işlevi kalıcı olarak kapatılacaktır.

<a name="why-use-one-voucher"></a>Bir fiş neden kullanılır?
====================

Müşterilerle yapılan görüşmelere dayanarak, müşterilerin Bir fiş işlevini kullandıkları senaryoları veya neden kullandıklarını gösteren aşağıdaki senaryo listesini derledik. Bu iş gereksinimlerinden bazıları yalnızca Bir fiş kullanılarak karşılanabilir. Ancak birçok senaryo için alternatifler de aynı iş gereksinimlerini karşılayabilir.

<a name="scenarios-that-require-one-voucher"></a>Bir fiş gerektiren senaryolar
----------------------------------

Aşağıdaki senaryolar yalnızca Bir fiş işlevi kullanılarak gerçekleştirilebilir. Bu işlevsel boşluklar, 2018 Sonbahar ve sonraki sürümlerdeki diğer özellikler ile doldurulacaktır.

-   **Satıcı veya müşteri ödemelerini özet biçiminde banka hesabına nakletme**

    -   Kuruluş, bankasına satıcılardan ve tutarlardan oluşan bir liste iletir ve banka da kuruluş adına satıcılara ödeme yapmak için bu listeyi kullanır. Banka, ödemelerin toplamını tek bir geri çekme olarak banka hesabına nakleder.

>   Satıcı ödemelerinin özetlenmesi yalnızca Bir fiş aracılığıyla desteklenir. Her satıcı, Borç Hesapları yardımcı defterindeki ayrıntıları korumak için ayrı bir satır olarak girilir ancak tüm ödemeler için özetlenen tutar, banka hesabı için tek bir satırda mahsup edilir. Bu nedenle, geri çekme işlemi banka yardımcı defterinde tek bir özetlenmiş tutar olarak gösterilir.

-   Kuruluş, müşteri ödemelerini havale yapar veya banka, müşteri ödemelerini kuruluş adına havale yapar ve havale banka hesabında bir peşin ödeme olarak gösterilir.

>   Müşteri ödemelerinin özetlenmesi genellikle havale işleviyle desteklenir. Ancak ödeme yönteminde "köprü" kullanıyorsanız bu senaryo yalnızca Bir fiş ile desteklenir. Müşteri ödemeleri, satıcı ödeme özeti için açıklanan şekilde girilir.

-   **İş olayından hareketleri gruplama mekanizması**

    -   Kuruluşun birden fazla hareketi tetikleyen tek bir iş olayı vardır. Ancak Muhasebe departmanı daha iyi denetlenebilirlik için muhasebe girişlerini görüntülemek istemektedir.

>   Kuruluşun, bir iş olayına ait muhasebe girişlerini birlikte görüntülemesi gerekiyorsa Bir fiş'i kullanması gerekir. 

-   **Ülkeye özgü özellikler**

 -   Polonya için Tek İdari Belge (SAD) özelliği şu anda bir fişin kullanılmasını gerektirir. Bu özellik için bir gruplandırma seçeneği yayımlanıncaya kadar Bir fiş işlevini kullanmaya devam etmeniz gerekir. Bir fiş işlevini gerektiren ülkeye özgü başka özellikler olabilir.

-   **Birden çok "satırda" vergiler olan müşteri ön ödemesi ödeme günlüğü**

 -   Müşteri, bir sipariş için ön ödeme yapar ve sipariş satırlarında ön ödeme için kaydedilmesi gereken farklı vergiler vardır. Müşteri ön ödemesi, siparişin satırlarının benzetimini yapan bir işlemdir, böylece her satırdaki tutar için uygun vergi kaydedilebilir.

Bu senaryoda, tek fişteki müşteriler aynı müşteridir çünkü hareket müşteri siparişinin satırlarının benzetimini yapar. Ön ödeme, tek bir fişe girilmelidir çünkü vergi hesaplamasının, müşterinin yaptığı tek ödemenin "satırlarında" yapılması gerekir.

-   **Sabit kıymet bakımı: Yakalama amortismanı, bölünmüş kıymet, elden çıkarmada amortismanı hesaplama**

Aşağıdaki sabit kıymet hareketleri de tek bir fiş içinde birden fazla hareket oluştur:
-   Bir kıymet üzerinde ek bir alım yapılır ve "yakalama" amortismanı hesaplanır.
-   Bir kıymet bölünür.
-   Elden çıkarma amortismanını hesaplamak için bir parametre etkinleştirilir ve ardından kıymet elden çıkarılır.

<a name="scenarios-that-dont-require-one-voucher"></a>Bir fiş gerektirmeyen senaryolar
----------------------------------------

Aşağıdaki senaryolar başka yollarla gerçekleştirilebilir ve Bir fiş kullanılmamalıdır.

-   **Müşteri ödemelerini özet biçiminde banka hesabına nakletme**

Kuruluş, müşteri ödemelerini havale yapar veya banka, müşteri ödemelerini kuruluş adına havale yapar ve havale banka hesabında bir peşin ödeme olarak gösterilir.

Müşteri ödemelerinin özetlenmesi, ödeme yönteminde köprü özelliği kullanılmadığında havale işleviyle desteklenir.

-   **Mahsuplaşma**

Mahsuplaşma sırasında, bir satıcı ve müşteri için bakiyeler birbiriyle mahsup edilir çünkü satıcı ve müşteri aynı taraftır. Bu yaklaşım, kuruluş ile müşteri/satıcı tarafı arasındaki para değişimini en aza indirir.

Mahsuplaşma, artışı ve azalışı farklı fişlere girerek ve farkı bir takas genel muhasebe hesabına naklederek gerçekleştirilebilir.

-   **Özeti genel muhasebe defterine nakletme**

Kuruluşlar genellikle veri miktarını en aza indirgemek için genel muhasebe defterine özet olarak nakletmek ister. Ancak yine de kuruluş genellikle hareket ayrıntısının korunmasını gerektirir. Deftere nakil, tek bir fişle özet olarak yapılırken hareket ayrıntısı bilinmemektedir ve korunamaz.

   -   Hareket ayrıntısı şu anda korunamadığından, özet olarak deftere nakilde Bir fiş özelliğinin kullanılmamasını öneririz.
   -   Bir fiş desteği kaldırıldıktan sonra, Kaynak belgesini ve Muhasebe çerçevelerini günlüklere uygulayabiliriz. Bu çerçeveler, daha sonra hareket ayrıntısını korur ve genel muhasebede özetlemeyi destekler.

-   **Aynı faturada birden fazla deftere nakledilmemiş ödemeyi kapatma**

Bu senaryo genellikle, müşterilerin satınalma ödemeleri için birden çok ödeme yöntemi kullanabildiği perakende kuruluşlarında bulunur. Bu senaryoda, kuruluşun birden çok deftere nakledilmemiş ödemeleri kaydetmesi ve bunları müşteri faturasına göre kapatabilmesi gerekir.

Microsoft Dynamics 365 for Operations sürüm 1611'e (Kasım 2016) eklenen yeni bir özellik, birden fazla deftere nakledilmemiş ödemeyi tek bir faturaya göre kapatabilmeye olanak tanır. Birden çok müşteri ödemesi artık tek bir fişe girilmek zorunda değildir.

-   **Banka ekstresi hareketlerini içe aktarma**

Bankalar genellikle bir kuruluş adına ödeme yapıp ödeme alır ve bu hareketler bankadan alınan bir dosya aracılığıyla Finance and Operations'ta kaydedilir. Kuruluşlar genellikle bu hareketleri dosyadaki banka ekstresi numarasını kullanarak birlikte gruplandırmak ister. Her bir hareket, banka ekstresinde ayrıntılı olarak gösterildiğinden banka yardımcı defterinde özetleme yapılması gerekmez.

Hareketler, günlük toplu iş numarasının kendisi veya belge numarası gibi günlükteki diğer alanlar kullanılarak gruplandırılabilir.

-   **Bakiyeleri aktar**

Kuruluş bir hata nedeniyle veya başka bir satıcı yükümlülüğü üstlendiğinden bir satıcıdan bir başka satıcıya bakiye transfer etmek zorunda kalabilir. Bu tür transferler, müşteriler ve banka hesapları gibi hesap türleri için de geçerlidir.

Bir hesaptan (satıcı, müşteri, banka hesabı vb.) başka bir hesaba bakiye transferleri ayrı fişlerle yapılabilir ve fark, bir takas genel muhasebe hesabına nakledilebilir.

-   **Başlangıç bakiyelerini girme**

Kuruluşlar genellikle yardımcı defter hesapları için (satıcılar, müşteriler, sabit kıymetler vb.) başlangıç bakiyelerini tek bir fiş hareketi olarak girer. Her bir yardımcı defter hesabı için başlangıç bakiyeleri ayrı fişler olarak girilebilir ve fark, bir takas genel muhasebe hesabına nakledilebilir.

-   **Deftere nakledilen bir müşteri veya satıcı belgesinin muhasebe girişini düzeltme**

Kuruluş, deftere nakledilen bir faturaya ait muhasebe girişi için Borç hesaplarını veya Alacak hesaplarını düzeltmek zorunda kalabilir ancak fatura başka bir mekanizma aracılığıyla tersine çevrilemez veya düzeltilemez.

Alacak hesapları veya borç hesapları genel muhasebe hesabında bir düzeltme yapılması gerekiyorsa ayarlama doğrudan genel muhasebe hesabında yapılmalıdır. Ayarlama, satıcı veya müşteri üzerinden deftere nakil işlemiyle yapılamaz. Bu yaklaşım, ayarlamanın bir "kesinti süresi" sırasında yapılmasını gerektirir. Böylece genel muhasebe hesabı geçici olarak el ile girişe izin verebilir.

-   **"Sistem buna izin veriyor"**

Kuruluşlar genellikle Tek fiş işlevini yalnızca sistem kullanmalarına olanak tanıdığından ve etkilerini anlamadan kullanır.

