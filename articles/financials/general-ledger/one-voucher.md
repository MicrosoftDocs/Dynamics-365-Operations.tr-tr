---
title: Bir fiş
description: Mali günlükler için Bir fiş (yevmiye fişi, sabit kıymet günlüğü, satıcı ödeme günlüğü vb.), tek bir fiş bağlamında birden fazla yardımcı defter hareketi girmenizi sağlar.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: ada04948c4775091091cc30664dd7d9405b4f9da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "308564"
---
# <a name="one-voucher"></a>Bir fiş

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>"Bir fiş" nedir?

Mali günlükler için (günlük fişi, sabit kıymet günlüğü, satıcı ödeme günlüğü vb.) mevcut işlev, tek bir fiş bağlamında birden fazla yardımcı defter hareketleri (müşteri, satıcı, sabit kıymetler, proje ve banka) girmenizi sağlar. Microsoft, bu işlevi *Bir fiş* olarak adlandırır. Tek bir fişi aşağıdaki yöntemlerden birini kullanarak oluşturabilirsiniz:

- Günlük adını (**Genel muhasebe** \> **Günlük ayarı** \> **Günlük adları**), **Yeni fiş** alanı **Yalnızca bir fiş numarası** olacak şekilde ayarlayın. Günlüğe eklediğiniz her satır artık aynı fişte yer alır. Bu nedenle fiş, aynı satırda bir hesap/mahsup hesap veya birleşimi olarak çok satırlı bir fiş şeklinde girilebilir.

    [![Tek satır](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Bir fiş tanımının **yalnızca Bir fiş numarası** olarak ayarlanan günlük adlarını **içermediğini** ve kullanıcının yalnızca Genel muhasebe türlerini içeren bir fiş girdiğini unutmayın. Bu konuda Bir fiş, birden çok satıcı, müşteri, banka, sabit kıymet veya proje içeren bir fiş olduğu anlamına gelir.

- Mahsup hesabın olmadığı çok satırlı bir fiş girin.

    [![Çok satırlı fiş](./media/Multi-line.png)](./media/Multi-line.png)

- Hesabın ve mahsup hesabın **Satıcı**/**Satıcı**, **Müşteri**/**müşteri**, **Satıcı**/**Müşteri** veya **Banka**/**Banka** gibi bir yardımcı defter hesap türü içerdiği bir fiş girin.

    [![Yardımcı defter fişi](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Bir fiş ile ilgili sorunlar

Bir fiş işlevi; hesap kapatma, vergi hesaplaması, hareketi geri alma, yardımcı defterin genel muhasebeye mutabakatı, mali raporlama ve daha fazlası sırasında sorunlara neden olur. (Hesap kapatma sırasında meydana gelen sorunlar hakkında daha fazla bilgi için bkz., örneğin [Birden fazla müşteri veya satıcı kaydına sahip tek bir fiş](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) Düzgün bir şekilde çalışmak ve raporlamak için bu işlemler ve raporlar, hareket ayrıntıları gerektirir. Bazı senaryolar, kuruluşunuzun kurulumuna bağlı olarak yine de düzgün çalışmaya devam etse de; bir fişte birden çok hareket girildiğinde çoğunlukla sorunlar oluşur.

Örneğin, aşağıdaki fişi deftere naklettiğinizi düşünelim.

[![Örnek](./media/example.png)](./media/example.png)

Daha sonra **Mali Bilgiler** çalışma alanında, **Satıcıya göre giderler** raporunu oluşturursunuz. Bu raporda, gider hesap bakiyelerini satıcı grubu ve ardından satıcı altında gruplar. Rapor oluşturulurken, sistem 250,00 tutarındaki giderin hangi satıcı grupları/satıcılar tarafından tahakkuk edildiğini belirleyemez. Hareket ayrıntıları eksik olduğundan sistem, 250,00 harcamanın tamamının fişte bulunan ilk satıcı tarafından tahakkuk edildiğini varsayar. Bu nedenle, 600120 numaralı ana hesap bakiyesine dahil olan 250,00 harcama, o satıcı grubu/satıcı altında gösterilir. Ancak, fişteki ilk satıcı çok yüksek olasılıkla doğru satıcı değildir. Bu nedenle, rapor büyük olasılıkla hatalıdır.

[![Gider](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Bir fiş'in geleceği

Daha önce belirtilen sorunlar nedeniyle, Bir fiş işlevselliği geçersiz duruma getirilecektir. Ancak bu işleve bağlı olan işlevsel boşluklar olduğundan, işlev aynı anda tamamen geçersiz olmayacaktır. Bunun yerine, aşağıdaki planı kullanacağız:

- **Bahar 2018 sürümü** – Varsayılan olarak, işlev varsayılan olarak **Genel muhasebe parametreleri** sayfasındaki **Genel** sekmesinde bulunan **Tek bir fiş içinde birden fazla harekete izin ver** aracılığıyla kapatılır. Ancak kuruluşunuzun, bu konunun ilerleyen bölümlerinde listelenen işlevsel boşluklardan birine denk gelen bir senaryosu varsa işlevi açabilirsiniz.

    - Müşterilerin Bir fiş gerektirmeyen bir iş senaryosu varsa işlevi açmamalıdır. Microsoft, başka bir çözüm varken bu işlev kullanılırsa bu konunun ilerleyen bölümlerinde tanımlanan alanlardaki "hataları" düzeltmez.
    - İşlevsel boşluklardan biri için gerekli olmadıkça Microsoft Dynamics 365 for Finance and Operations tümleştirmelerinde Bir fiş'i kullanmayı bırakın.

- **Sonraki sürümler**: Tüm işlevsel boşluklar doldurulacaktır. **İşlevsel boşluklar doldurulduğunda ve yeni özellikler sunulduğunda, Bir fiş işlevi kalıcı olarak kapatılmadan önce en az bir yıl geçer**, çünkü müşteriler ve bağımsız yazılım satıcıları (ISV'ler), yeni işleve tepki vermek üzere yeterli zamana ihtiyacı olur. Örneğin, kendi iş süreçleri, varlık ve tümleştirmeleri güncelleştirmesi gerekebilir.

> [!IMPORTANT]
> **Yalnızca bir fiş numarası** seçeneğinin Günlük adı kurulumundan **kaldırılmamış** olduğunu unutmayın. Bu seçenek, fiş yalnızca genel muhasebe hesap türlerini içerdiğinde hala desteklenmektedir. Müşterilerin bu ayarı kullanırken dikkatli olması gerekir çünkü fiş **Yalnızca tek fiş numarası** seçeneğini kullanıp ardından birden fazla müşteri, satıcı, banka, sabit kıymet veya proje girmeleri durumunda deftere nakledilmez. Ayrıca, müşteriler **Satıcı**/**Banka** hesap türlerini içeren tek bir fiş içindeki bir ödeme gibi yardımcı defter hesap türlerinin bir karışımını da girebilir.

## <a name="why-use-one-voucher"></a>Bir fiş neden kullanılır?

Microsoft, müşterilerle yapılan görüşmelere dayanarak, müşterilerin Bir fiş işlevini kullandıkları senaryoları veya neden kullandıklarını gösteren aşağıdaki senaryo listesini derledi. Bu iş gereksinimlerinden bazıları yalnızca Bir fiş kullanılarak karşılanabilir. Ancak birçok senaryo için alternatifler de aynı iş gereksinimlerini karşılayabilir.

### <a name="scenarios-that-require-one-voucher"></a>Bir fiş gerektiren senaryolar

Aşağıdaki senaryolar yalnızca Bir fiş işlevi kullanılarak gerçekleştirilebilir. Kuruluşunuzda bu senaryolardan herhangi biri varsa, fişe girilecek birden çok hareketi etkinleştirmeniz gerekir; **genel muhasebe parametreleri** sayfasındaki **Tek bir fiş içinde birden fazla harekete izin ver** parametresi ayarını değiştirin. Bu işlevsel boşluklar, sonraki sürümlerdeki diğer özellikler ile doldurulacaktır.

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Satıcı veya müşteri ödemelerini özet biçiminde banka hesabına nakletme

**Senaryo** Kuruluş, bankasına satıcılardan ve tutarlardan oluşan bir liste iletir ve banka da kuruluş adına satıcılara ödeme yapmak için bu listeyi kullanır. Banka, ödemelerin toplamını tek bir geri çekme olarak banka hesabına nakleder.

Satıcı ödemelerinin özetlenmesi yalnızca Bir fiş aracılığıyla desteklenir. Her bir satıcı, Borç hesapları yardımcı defterindeki ayrıntıları korumak için ayrı bir satır olarak girilir. Bununla birlikte, tüm ödemeler için özet bir tutar, banka hesabı için tek bir satıra mahsup edilir. Bu nedenle, geri çekme işlemi banka yardımcı defterinde tek bir özetlenmiş tutar olarak gösterilir.

**Senaryo** Kuruluş, müşteri ödemelerini havale yapar veya banka, müşteri ödemelerini kuruluş adına havale yapar ve havale banka hesabında bir peşin ödeme olarak gösterilir.

Müşteri ödemelerinin özetlenmesi genellikle havale işleviyle desteklenir. Ancak ödeme yönteminde "köprü" kullanıyorsanız bu senaryo yalnızca Bir fiş ile desteklenir. Müşteri ödemeleri, satıcı ödeme özeti için açıklanan şekilde girilir.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>İş olayından hareketleri gruplama mekanizması

**Senaryo** Kuruluşun birden fazla hareketi tetikleyen tek bir iş olayı vardır. Ancak Muhasebe departmanı daha iyi denetlenebilirlik için muhasebe girişlerini görüntülemek istemektedir.

Kuruluşun, bir iş olayına ait muhasebe girişlerini birlikte görüntülemesi gerekiyorsa Bir fiş'i kullanması gerekir. 

### <a name="country-specific-features"></a>Ülkeye özgü özellikler

**Senaryo** Polonya için Tek İdari Belge (SAD) özelliği şu anda bir fişin kullanılmasını gerektirir. Bu özellik için bir gruplandırma seçeneği yayımlanıncaya kadar Bir fiş işlevini kullanmaya devam etmeniz gerekir. Bir fiş işlevini gerektiren ülkeye özgü başka özellikler olabilir.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Birden çok "satırda" vergiler olan müşteri ön ödemesi ödeme günlüğü

Bu senaryoda, tek fişteki müşteriler aynı müşteridir çünkü hareket müşteri siparişinin satırlarının benzetimini yapar. Ön ödeme, tek bir fişe girilmelidir çünkü vergi hesaplamasının, müşterinin yaptığı tek ödemenin "satırlarında" yapılması gerekir.

### <a name="customer-reimbursement"></a>Müşteri iadesi

**Senaryo** Müşteri, bir sipariş için ön ödeme yapar ve sipariş satırlarında ön ödeme için kaydedilmesi gereken farklı vergiler vardır. Müşteri ön ödemesi, siparişin satırlarının benzetimini yapan bir işlemdir, böylece her satırdaki tutar için uygun vergi kaydedilebilir.

İade periyodik görevi Alacak hesapları modülünden çalışırsa bakiyeyi bir müşteriden satıcıya taşımak için bir hareket oluşturur. Bu senaryo için, müşteriye iade yapmak üzere Bir fiş kullanılmalıdır.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Sabit kıymet bakımı: Yakalama amortismanı, bölünmüş kıymet, elden çıkarmada amortismanı hesaplama
Aşağıdaki sabit kıymet hareketleri de tek bir fiş içinde birden fazla hareket oluştur:

- Bir kıymet üzerinde ek bir alım yapılır ve "yakalama" amortismanı hesaplanır.
- Bir kıymet bölünür.
- Elden çıkarma amortismanını hesaplamak için bir parametre açılır ve ardından kıymet elden çıkarılır.
- Bir kıymetin servis tarihi alım tarihinden öncedir. Bu nedenle, bir amortisman düzeltmesi deftere nakledilir.

### <a name="bills-of-exchange-and-promissory-notes"></a> Kambiyo senetleri ve senetler
Kambiyo senetleri ve senetler, Bir fiş kullanımı gerektirir çünkü hareketler, müşteri veya satıcı bakiyesini ödeme durumuna bağlı olarak Alacak hesapları/Borç hesapları genel muhasebe hesabından başkasına taşır.

## <a name="scenarios-that-dont-require-one-voucher"></a>Bir fiş gerektirmeyen senaryolar

Aşağıdaki senaryolar başka yollarla gerçekleştirilebilir ve Bir fiş işlevi kullanılmamalıdır.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Müşteri ödemelerini özet biçiminde banka hesabına nakletme

Kuruluş, müşteri ödemelerini havale yapar veya banka, müşteri ödemelerini kuruluş adına havale yapar ve havale banka hesabında bir peşin ödeme olarak gösterilir.

Müşteri ödemelerinin özetlenmesi, ödeme yönteminde "köprü" özelliği kullanılmadığında havale işleviyle desteklenir.

### <a name="netting"></a>Mahsuplaşma

Mahsuplaşma sırasında, bir satıcı ve müşteri için bakiyeler birbiriyle mahsup edilir çünkü satıcı ve müşteri aynı taraftır. Bu yaklaşım, kuruluş ile müşteri/satıcı tarafı arasındaki para değişimini en aza indirir.

Mahsuplaşma, artışı ve azalışı farklı fişlere girerek ve farkı bir takas genel muhasebe hesabına naklederek gerçekleştirilebilir.

### <a name="post-in-summary-to-the-general-ledger"></a>Özeti genel muhasebe defterine nakletme

Kuruluşlar genellikle veri miktarını en aza indirgemek için genel muhasebe defterine özet formu olarak nakletmek ister. Ancak yine de kuruluş genellikle hareket ayrıntılarının korunmasını gerektirir. Deftere nakil, tek bir fişle özet formu olarak yapılırken hareket ayrıntıları bilinmemektedir ve korunamaz.

- Hareket ayrıntıları şu anda korunamadığından, özet formu olarak deftere nakilde kurumun Bir fiş özelliğini **kullanmamasını** öneririz.
- Bir fiş desteği kaldırıldıktan sonra, Kaynak belgesi ve Muhasebe çerçeveleri günlüklere uygulanabilir. Bu çerçeveler, daha sonra hareket ayrıntılarını korur ve genel muhasebede özetlemeyi destekler.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Aynı faturada birden fazla deftere nakledilmemiş ödemeyi kapatma

Bu senaryo genellikle, müşterilerin satınalma ödemeleri için birden çok ödeme yöntemi kullanabildiği perakende kuruluşlarında bulunur. Bu senaryoda, kuruluşun birden çok deftere nakledilmemiş ödemeleri kaydetmesi ve bunları müşteri faturasına göre kapatabilmesi gerekir.

Microsoft Dynamics 365 for Operations sürüm 1611'e (Kasım 2016) eklenen yeni bir özellik, birden fazla deftere nakledilmemiş ödemeyi tek bir faturaya göre kapatabilmeye olanak tanır. Birden çok müşteri ödemesi artık tek bir fişe girilmek zorunda değildir.

### <a name="import-bank-statement-transactions"></a>Banka ekstresi hareketlerini içe aktarma

Bankalar genellikle bir kuruluş adına ödeme yapıp ödeme alır ve bu hareketler bankadan alınan bir dosya aracılığıyla Finance and Operations'ta kaydedilir. Kuruluşlar genellikle bu hareketleri dosyadaki banka ekstresi numarasını kullanarak birlikte gruplandırmak ister. Her bir hareket, banka ekstresinde ayrıntılı olarak gösterildiğinden banka yardımcı defterinde özetleme yapılması gerekmez.

Hareketler, günlük toplu iş numarasının kendisi veya belge numarası gibi günlükteki diğer alanlar kullanılarak gruplandırılabilir.


### <a name="transfer-balances"></a>Bakiyeleri aktar

Kuruluş bir hata nedeniyle veya başka bir satıcı yükümlülüğü üstlendiğinden bir satıcıdan bir başka satıcıya bakiye transfer etmek zorunda kalabilir. Bu tür transferler, **Müşteri** ve **Banka** gibi hesap türleri için de geçerlidir.

Bir hesaptan (satıcı, müşteri, banka vb.) başka bir hesaba bakiye transferleri ayrı fişlerle yapılabilir ve fark, bir takas genel muhasebe hesabına nakledilebilir.

### <a name="enter-beginning-balances"></a>Başlangıç bakiyelerini girme

Kuruluşlar genellikle yardımcı defter hesapları için (satıcılar, müşteriler, sabit kıymetler vb.) başlangıç bakiyelerini tek bir fiş hareketi olarak girer. Her bir yardımcı defter hesabı için başlangıç bakiyeleri ayrı fişler olarak girilebilir ve fark, bir takas genel muhasebe hesabına nakledilebilir.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Deftere nakledilen bir müşteri veya satıcı belgesinin muhasebe girişini düzeltme

Kuruluş, deftere nakledilen bir faturaya ait muhasebe girişi için Borç hesaplarını veya Alacak hesaplarını düzeltmek zorunda kalabilir ancak fatura başka bir mekanizma aracılığıyla tersine çevrilemez veya düzeltilemez.

Alacak hesapları veya Borç hesapları genel muhasebe hesabında bir düzeltme yapılması gerekiyorsa ayarlama doğrudan genel muhasebe hesabında yapılmalıdır. Ayarlama, satıcı veya müşteri üzerinden deftere nakil işlemiyle yapılamaz. Bu yaklaşım, ayarlamanın bir "kesinti süresi" sırasında yapılmasını gerektirir. Böylece genel muhasebe hesabı geçici olarak el ile girişe izin verebilir.

### <a name="the-system-allows-it"></a>"Sistem buna izin veriyor"

Kuruluşlar genellikle Tek fiş işlevini yalnızca sistem kullanmalarına olanak tanıdığından ve etkilerini anlamadan kullanır.