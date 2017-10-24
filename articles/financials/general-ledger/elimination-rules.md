---
title: "Eleme kuralları"
description: "Bu konuda, eleme kuralları ve elemeler hakkında raporlama için çeşitli seçenekler ile ilgili bilgiler verilmektedir."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f8fe754a27a825ace862d5eac992c42ef973f10
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="elimination-rules"></a>Eleme kuralları

[!include[banner](../includes/banner.md)]


Bu konuda, eleme kuralları ve elemeler hakkında raporlama için çeşitli seçenekler ile ilgili bilgiler verilmektedir.

Bir ana tüzel kişilik bir veya daha fazla tüzel kişilikle iş yapıyor ve konsolide finansal raporlama kullanıyorsa eleme hareketleri gerekir. Konsolide mali tablolar yalnızca konsolide kuruluş ve bu kuruluşların dışındaki diğer varlıklar arasındaki hareketleri içerebilir. Bu nedenle, aynı kuruluşun parçası olan tüzel kişilikler arasındaki hareketler genel muhasebeden kaldırılarak veya elenerek mali raporlarda görünmemesi sağlanmalıdır. Elemeler hakkında rapor hazırlamanın birden çok yolu vardır:

-   Konsolidasyon veya eleme şirketinde bir eleme kuralı oluşturabilir veya işlenebilir.
-   Elemeler hesaplarını ve boyutlarını belirli satır veya sütunda göstermek için mali raporlama kullanılabilir.
-   Elemeleri izlemek üzere el ile hareket girişlerini nakletmek için ayrı bir tüzel kişilik kullanılabilir.

Bu konuda, konsolidasyon veya eleme şirketinde işlenen eleme kurallarına odaklanılmaktadır. Elemeler için hedef tüzel kişilik olarak belirtilen bir tüzel kişilikte eleme hareketleri oluşturmak için eleme kuralları ayarlayabilirsiniz. Bu hedef tüzel kişilik, eleme tüzel kişiliği olarak bilinir. Eleme günlükleri konsolidasyon işlemi sırasında veya bir eleme günlüğü teklifi kullanılarak oluşturulabilir. Eliminasyon günlükleri ayarlamadan önce aşağıdaki terimler hakkında bilginiz olmalı:

-   **Kaynak tüzel kişilik** – Elenmekte olan tutarların nakledildiği tüzel kişilik.
-   **Hedef tüzel kişilik** – Eleme kurallarının çıkarıldığı tüzel kişilik.
-   **Eleme tüzel kişiliği** – Elemeler içi hedef tüzel kişilik olarak belirtilen tüzel kişilik.
-   **Konsolide edilen tüzel kişilik** – Bir tüzel kişilikler grubu için oluşturulan mali sonuçların raporunu hazırlamak için oluşturulmuş bir tüzel kişilik. Tüzel kişiliklerden gelen mali veriler bu tüzel kişilikte konsolide edilir ve birleştirilmiş veriler kullanılarak bir mali rapor oluşturulur.

Aşağıdaki tabloda, elenmesi gerekebilecek hareket türleri gösterilmektedir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Hareket türü</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Satış siparişi girişi ve faturalandırma (merkezi işlem)</td>
<td>Bir müşteriye kuruluşunuzdaki başka bir tüzel kişilik adına bir ürün satıyorsunuz.</td>
</tr>
<tr class="even">
<td>Satış siparişi girişi (şirketlerarası/şirketiçi) ve faturalandırma</td>
<td>Kuruluşunuzdaki tüzel kişilikler arasında ürünler satıyorsunuz.</td>
</tr>
<tr class="odd">
<td>Satın alma siparişleri (merkezi işlem)</td>
<td>Bir satıcıdan kuruluşunuzdaki başka bir tüzel kişilik adına stok, malzemeler, hizmetler, sabit kıymetler ve başka ürünler alıyorsunuz.</td>
</tr>
<tr class="even">
<td>Stok yönetimi (şirketlerarası/şirketiçi)</td>
<td><ul>
<li>Bir tüzel kişiliğin stoğunu, kuruluşunuzdaki başka bir tüzel kişiliğin sabit kıymetlerine aktarıyorsunuz.</li>
<li>Bir tüzel kişiliğin stoğunu, kuruluşunuzdaki başka bir tüzel kişiliğin stoğuna aktarıyorsunuz.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transit stok izleme</td>
<td>Aynı tüzel kişilikte farklı coğrafi tesislerdeki ambarlar arasında madde aktarıyorsunuz.</td>
</tr>
<tr class="even">
<td>Borç hesapları merkezi fatura işleme</td>
<td>Kuruluşunuzdaki başka bir tüzel kişilik adına fatura kaydediyorsunuz.</td>
</tr>
<tr class="odd">
<td>Borç hesapları merkezi ödeme işleme</td>
<td>Kuruluşunuzdaki başka bir tüzel kişilik adına fatura ödüyorsunuz.</td>
</tr>
<tr class="even">
<td>Nakit yönetimi ve hazine (merkezi işlem)</td>
<td><ul>
<li>Vergi ödemelerini, vergi iadelerini, faiz giderlerini, ödünç verilenleri, avansları, temettü ödemelerini, önceden ödenmiş hak bedellerini veya komisyonları işliyorsunuz.</li>
<li>Kuruluşunuzdaki başka bir tüzel kişilik adına gider ödüyorsunuz. Fatura, hedef tüzel kişiliğin defterlerine girilir ve tüzel kişilikler arasında çapraz kapatma yapmanız gerekir. Örneğin, bir tüzel kişilik başka bir tüzel kişilikteki bir çalışanın gider raporunu öder. Bu durumda, çalışanın gider raporunda başka bir tüzel kişilikle ilgili giderler olur.</li>
<li>Nakdi kuruluşunuzdaki bir tüzel kişilikten bir diğerine aktarırsınız.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Alacak hesapları (merkezi işlem)</td>
<td>Başka bir tüzel kişiliğin müşteri faturası için nakit alırsınız ve çeki o tüzel kişiliğin banka hesabına havale edersiniz.</td>
</tr>
<tr class="even">
<td>Bordro (merkezi işlem, şirketlerarası/şirketiçi)</td>
<td><ul>
<li>Başka bir tüzel kişiliğin bordrosunu ödüyorsunuz. Örneğin, bir tüzel kişilik kendi çalışanları için olan kendi bordrosunu ödüyor, ancak bir çalışanın bu bordro işlemi sırasında başka bir tüzel kişilik için yaptığı işi geri masraflandırıyor. Veya bir çalışan A tüzel kişiliği için yarı zamanlı ve B tüzel kişiliği için yarı zamanlı çalışmıştır ve kazançlar tüm ödemelere yayılmıştır. Bu gibi durumlarda çalışana ödeme, her iki tüzel kişilikten yapılan ödemeleri içerir. Yalnızca maaşlar nakledilmez, maaşlar için vergiler, kazançlar, kesintiler ve tahakkuklar da nakledilir.</li>
<li>Bir departman veya bölümden bir diğerine işgücü aktarıyorsunuz.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sabit kıymetler (şirketlerarası/şirketiçi)</td>
<td>Bir tüzel kişiliğin sabit kıymetlerine veya stoğuna sabit kıymetler aktarıyorsunuz.</td>
</tr>
<tr class="even">
<td>Tahsisatlar (şirketlerarası/şirketiçi)</td>
<td>Şirket tahsisatlarını işliyorsunuz. Tahsisatlar, kaynak modülden bağımsız olarak tahsis edilmiş herhangi bir hesaba yönelik faaliyetlerdir.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Örnek
Tüzel kişiliğiniz (A tüzel kişiliği) kuruluşunuzdaki başka bir tüzel kişiliğe (B tüzel kişiliği) bir şeyler satıyor. Aşağıdaki örnekte, iki tüzel kişilik arasında gerçekleşen hareketlerin nasıl elenmesi gerekebileceği gösterilmektedir.

-   A tüzel kişiliği, 10,00 lira maliyetli bir malı B tüzel kişiliğine 10,00 liraya satıyor.
-   A tüzel kişiliği 10,00 lira maliyetli bir malı B tüzel kişiliğine 10,00 lira artı 2,00 lira fiili sevkiyat maliyetiyle satıyor.
-   A tüzel kişiliği, 10,00 lira maliyetli bir malı B tüzel kişiliğine 15,00 liraya satıyor ve satıştan bir marj elde ediyor.
-   A tüzel kişiliği, 10,00 lira maliyetli bir malı B tüzel kişiliğine 15,00 liraya satıyor ve satıştan marjın yarısını elde ediyor. B tüzel kişiliği, satıştan elde edilen marjın diğer yarısını alıyor. Böylece, gelir bölünüyor. Bölünmüş gelir, dışarıdan bir kuruluştan değil de kuruluştaki başka bir tüzel kişilikten siparişe bir teşvik oluşturuyor.

Tüm bu hareketler, borç ve alacak hesaplarına nakledilen şirketlerarası hareketleri oluşturur. Ayrıca bu hareketler, şirketlerarası satış ve satılan malların maliyeti eşit olmadığı zaman artırma ve azaltma tutarlarını da içerebilir.

## <a name="set-up-elimination-rules"></a>Eliminasyon kurallarını ayarlama
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içinde eleme kuralları ayarlanırken, eleme amaçlı ayrı bir mali boyut oluşturmanızı öneririz. Müşterilerin çoğu buna Ticaret Ortağı veya benzer bir ad verirler. Bir mali boyut kullanmamaya karar verirseniz, yalnızca şirketlerarası harektelere özel bir ana hesaba sahip olduğunuzdan emin olun. 

Elemeler için kurulum, Konsolidasyonlar modülünün kurulum alanında bulunur. Bir kural için bir açıklama girdikten sonra, eleme günlüğünün nakledeceği şirketi seçmeniz gerekir. Bu, Tüzel varlık kurulumunda **Mali eleme sürecini kullan**'ın seçilmiş olduğu bir şirket olmalıdır. 

Gerekirse, eleme kuralının ne zaman geçerli olacağını ve ne süresinin ne zaman dolacağını seçebilirsiniz. Eleme öneri işleminde kullanılabilir olmasını istiyorsanız **Etkin**'i **Evet** olarak ayarlamanız gerekir. Bir tür **Eleme**'ye sahip bir günlük adı seçin.

Temelleri tanımladıktan sonra, **Satırlar** üzerine tıklatarak gerçek işleme kurallarını tanımlayabilirsiniz. Elemeler için iki seçenek mevcuttur; net değişim tutarını eleme veya sabit bir tutar tanımlama. 

Kaynak hesabınızı seçin. Joker karakter olarak bir yıldız (\*) kullanabilirsiniz. Örneğin, 1\* tahsisat için veri kaynağı olarak 1 ile başlayan tüm hesapları seçer. 

Kaynak hesaplarınızı seçtikten sonra **Hesap belirtimi**, hedef şirketinden kullanılan hesabı belirler. **Kaynak** hesabında tanımlanan aynı ana hesabı kullanmak istiyorsanız **Kaynak**'ı seçin. **Kullanıcı tanımlı**'yı seçerseniz, bir hedef hesabı belirtmeniz gerekir. 

Boyut belirtimi de aynı şekilde davranır. **Kaynak**'ı seçerseniz, hedef şirkette de kaynak şirkette kullandığı aynı boyutları kullanır. **Kullanıcı tanımlı**'yı seçerseniz, hedef şirketteki boyutları **Hedef boyutları** menü öğesini seçerek belirtmeniz gerekir. 

Kaynak boyutları ve eleme için kaynakta kullanılacak finansal boyutları ve değerleri seçin.

## <a name="process-elimination-transactions"></a>Eliminasyon hareketlerini işleme koy
Eleme hareketlerini işlemenin iki yolu vardır; birleştirme işlemi sırasında veya bir eleme günlüğü oluşturarak ve eleme teklif işlemini yürüterek. Bu bölüm, günlüğü oluşturmaya ve eleme işlemini çalıştırmaya odaklanır. 

Bir eleme şirketi olarak tanımlanan bir şirkette, Birleştirme modülü içerisinde **Eleme günlüğü**'nü seçin. Günlük adını seçtikten sonra, **Satırlar**'ı tıklatın. **Teklifler** menüsünü seçtikten sonra **Eleme teklifi**'ni seçerek teklifi çalıştırabilirsiniz.

Birleştirilmiş verinin kaynağı olan şirketi seçin ve sonra işlemek istediğiniz kuralı seçin. Eleme tutarlarını aramaya başlamak için bir başlangıç tarihi ve eleme tutarları bitişi için bir bitiş tarihi girin. **GL deftere nakil tarihi** alanı, günlüğü genel muhasebe defterine nakletmek için kullanılan tarihtir. **Tamam**'ı tıklattıktan sonra, tutarları görebilir ve günlüğü deftere nakledebilirsiniz.




