---
title: "Eleme kuralları"
description: "Bu konu, eleme kuralları ve elemeler hakkında raporlama için çeşitli seçenekler hakkında bilgi sağlar."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Eleme kuralları

Bu konu, eleme kuralları ve elemeler hakkında raporlama için çeşitli seçenekler hakkında bilgi sağlar.

Bir ana tüzel kişilik bir veya daha fazla tüzel kişilikle iş yapıyor ve konsolide finansal raporlama kullanıyorsa eleme hareketleri gerekir. Konsolide mali tablolar yalnızca konsolide kuruluş ve bu kuruluşların dışındaki diğer varlıklar arasındaki hareketleri içerebilir. Bu nedenle, aynı kuruluşun parçası olan tüzel kişilikler arasındaki işlemleri kaldırılmalı, veya finansal raporlarda görünür olmayan şekilde, Genel muhasebeden ortadan kalkar. Elemeler hakkında rapor hazırlamanın birden çok yolu vardır:

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
Dynamics 365 işlemleri için eleme kuralları kurarken eleme amacıyla özellikle mali boyut oluşturmanızı öneririz. Müşterilerin çoğu ticaret ortağı veya benzeri adlandırın. Ardından mali boyut kullanmamaya karar verirseniz, yalnızca şirketlerarası hareketler belirli ana hesaplarına sahip emin olun. 

Elemeler için Kurulum Konsolidasyonları modülü Kurulum alanında bulunur. Kural için bir açıklama girin sonra Eliminasyon günlüğünün deftere nakleder şirket seçmeniz gerekir. Bu sahip bir şirket olması gerekir **kullanılmak üzere mali eleme işlemi** tüzel kurulumda seçili. 

Gerekirse, Eliminasyon kuralının geçerli olur ve ne zaman dolmuş, üzerinde bir tarihi ayarlayabilirsiniz. Ayarlamanız gerekir **etkin** için **Evet** eleme öneri işlemine kullanılabilir olmasını istiyorsanız. Bir tür olan bir günlük adı seçin **eleme**.

Temel tanımladıktan sonra tıklatarak gerçek işleme kuralları tanımlayabilirsiniz **satırları**. Net tutara elemek veya sabit bir tutar tanımlama elemeler için iki seçenek vardır. 

Kaynak hesabınızı seçin. Yıldız kullanabilirsiniz (\*) joker kart olarak. Örneğin, 1\* ayırma için veri kaynağı olarak 1 ile başlayan tüm hesapların seçersiniz. 

Kaynak hesaplarınızı seçtikten sonra **hesap belirtimi** kullanılan hedef şirket hesabından belirler. Seçin **kaynak** tanımlanan aynı ana hesabı kullanmak isterseniz, **kaynak** hesabı. Seçerseniz **kullanıcı tanımlı**, sonra da hedef hesabı belirtmeniz gerekir. 

Boyut belirtimi aynı şekilde davranır. Seçerseniz **kaynak**, onu aynı boyutları hedef şirket kaynak şirket olarak kullanır. Seçerseniz **kullanıcı tanımlı**, tıklatarak hedef şirkete ait boyutları belirtmek gerekir **hedef boyutları** menü öğesi. 

Kaynak boyutları ve mali boyutları ve eleme kaynağı olarak kullanılan değerleri seçin.

## <a name="process-elimination-transactions"></a>Eliminasyon hareketlerini işleme koy
Çevrimiçi birleştirme işlemi sırasında veya eleme günlük oluşturma ve eleme teklif işlemini çalıştırarak işlemi eleme hareketleri için iki yol vardır. Bu bölümde, günlük oluşturma ve eleme işlemi çalıştıran odaklanır. 

Bir eleme şirket olarak tanımlanan bir şirkette seçin **eleme günlük** Konsolidasyonlar modülünde. Günlük adı seçtikten sonra'ı **satırları**. Teklifi seçerek çalıştırabilirsiniz **tekliflerini** menü ve daha sonra seçerek **eleme teklif**.

Şirket konsolide veri kaynağını seçin ve sonra işlem yapmak istediğiniz kuralı seçin. Eleme tutarlar için aramayı başlatmak için bir başlangıç tarihi ve bitiş eleme tutarlar için arama tarihi bitiş tarihi girin. **G/m deftere nakil tarihi** günlüğü genel muhasebeye nakletmek için kullanılan tarih bir alandır. Siz tıklattıktan sonra **Tamam**, tutarları gözden geçirin ve günlüğü deftere nakledin.


