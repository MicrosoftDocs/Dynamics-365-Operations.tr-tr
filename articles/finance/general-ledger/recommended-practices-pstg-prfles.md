---
title: Deftere nakil profilleri için önerilen yöntemler
description: Bu makalede, deftere nakil profillerini yapılandırmak için önerilen yöntemler açıklanmaktadır.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849916"
---
# <a name="recommended-practices-for-posting-profiles"></a>Profilleri deftere nakletmek için önerilen yöntemler

Sistem genelinde deftere nakil profillerini konfigüre ettiğinizde izlemeniz gereken birkaç önerilen yöntem vardır. Bu makalede, farklı senaryoları ve ilgili önerilen yöntemler açıklanmaktadır.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>El ile girişe izin verme bayrağı ayarlanıyor

**Ana firmalar** sayfasında, bir deftere nakil profili için kullanılan tüm ana hesaplar için **El ile girişe izin verme** onay kutusu seçilmelidir. Bu ayar kullanıcıların bir günlük girişini ana hesaba el ile postadan almasını engeller. Bu sayede yardımcı defterin genel muhasebe ile dengeli olmasına ve mutabakat sürecini kolaylaştırmaya yardımcı olur.

Sistem tarafından denetlenen ve otomatik olarak deftere nakledilen bir hesap için ayarlamalar gerekiyorsa, aşağıdaki yaklaşımlardan birini kullanabilirsiniz:

- Ayarlamaların deftere nakledilebileceği bir ikincil ana hesap oluşturun. Daha sonra hesapları gruplamak ve toplamak için mali raporlarınızda bir Toplam hesap veya özel bir satır kullanın.
- İlgili alt muhasebedeki orijinal hareketleri tersine çevirin, gerekli düzeltmeleri yapın ve hareketi aynı alt hesap üzerinden yeniden deftere nakledin.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Hareketlerin ardından deftere nakil profillerini değiştirme

Hareketler var olduktan sonra bir deftere nakil profilini değiştirirseniz, mutabakat başarısız olabilir ve alt genel muhasebe ve genel muhasebe bakiyesi dışında kalabilir. Genel olarak, hareketler var olduktan sonra deftere nakil profilini **değiştirmemenizi** öneririz.

Değişiklikler gerekliyse, sistemin bütünlüğünü sağlamaya yardımcı olmak için aşağıdaki yönergeleri kullanın:

- Bir dönem kapanışı sırasında değişiklikleri yapın.
- Sistemde başka hareket gerçekleşmezken değişiklikleri yapın.
- Genel muhasebeyi doğrulayın ve siz değişiklikleri yapmadan önce ve sonra bu raporu alt muhasebeyle karşılaştırın.
- Deftere nakil profilini değiştirirseniz, deftere nakledilen hareketler güncelleştirilmez. Değişiklik için herhangi bir ayarlama girişinin gerekli olup olmadığını dikkatle değerlendirin.
- Stok deftere nakil profillerini değiştiriyorsanız, değişikliklerin eldeki stokunuzu ve genel muhasebe bakiyelerini nasıl etkileyeceğini dikkate alın. Bazı değişiklikler, stoku 0'a (sıfır) getirmeyi, stoku kapatmayı ve değişiklikler yapıldıktan sonra stoku geri getirmeyi gerektirebilir.
- Değişikliklerinizi, üretim sırasında gerçekleştirmeden önce üretim dışı bir ortamda test edin.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Deftere nakil profillerinde yapılan değişiklikleri denetlemek için veritabanı günlüğünü kullanma

Deftere nakli kontrol eden her deftere nakil profili ve parametre tablosu için veritabanı günlükleri ayarlamayı düşünebilirsiniz. Sonra bir parametre veya profil değiştirilirse, hangi değerin değiştirildiği, kim tarafından değiştirildiği, ne zaman değiştirildiği ve önceki değerin ne olduğu ile ilgili olan tam denetim kaydınız olur. Bu bilgiler mutabakat işleminiz sırasında kritik olabilir ve denetçi destekleyici belgeleri gerektirebilir.

Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Deftere nakil profilleri ve ilgili deftere nakil parametreleriyle ilgili ortak tablo adları için referans olarak aşağıdaki tabloyu kullanın.

| Sayfa adı | Gezinti yolu | Tablo adı |
|-----------|-----------------|------------|
| Borç hesapları parametreleri | Borç hesapları &gt; Kurulum &gt; Borç hesapları parametreleri'ne gidin | VendParm |
| Satıcı deftere nakil profili | Borç hesapları &gt; Kurulum &gt; Satıcı nakil profili | VendPosting |
| Masraf kodu | Borç hesapları &gt; Masraflar kurulum &gt; Masraf kodu veya Borç hesapları &gt; Masraflar kurulum &gt; Masraflar kodu | MarkupTable |
| Ödeme yöntemleri | Borç hesapları &gt; Ödeme kurulumu &gt; Ödeme yöntemleri | VendPaymMode |
| Nakit iskontoları | Borç hesapları &gt; Ödeme kurulumu &gt; Nakit iskontoları veya Alacak hesapları &gt; Ödeme kurulumu &gt; Nakit iskontoları | CashDisc |
| Ödeme ücreti (Satıcı) | Borç hesapları &gt; Ödeme kurulumu &gt; Ödeme Ücreti | VendPaymFee |
| Alacak hesapları parametreleri | Alacak hesapları &gt; Kurulum &gt; Alacak hesapları parametreleri | CustParm |
| Müşteri deftere nakil profilleri | Alacak hesapları &gt; Kurulum &gt; Müşteri nakil profili | CustPosting |
| Ödeme yöntemleri | Alacak hesapları &gt; Ödeme kurulumu &gt; Ödeme yöntemi | CustPaymMode |
| Ödeme ücreti (Müşteri) | Alacak hesapları &gt; Ödeme kurulumu &gt; Ödeme yöntemleri | CustPaymFee |
| Kıymet kiralama parametreleri | Varlık kiralama &gt; Kurulum &gt; Varlık kiralama parametreleri | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Banka hesapları | Nakit ve banka yönetimi &gt; Banka hesapları &gt; Banka hesapları | BankAccountsTable |
| Banka hareketi türleri | Nakit ve Banka yönetimi &gt; Kurulum &gt; Banka hareket türleri | BankTransType |
| Eleme kuralları | Konsolidasyonlar &gt; Kurulum &gt; Eliminasyon kuralı | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Gider kategorileri | Gider yönetimi &gt; Kurulum &gt; Genel &gt; Gider kategorileri | ProjCategories |
| Sabit kıymet parametreleri | Sabit kıymetler &gt; Kurulum &gt; Sabit kıymet parametreleri | AssetParameters |
| Sabit kıymet deftere nakil profilleri | Sabit kıymetler &gt; Kurulum &gt; Sabit kıymet deftere nakil profilleri | AssetLedgerAccounts<br>AssetDisposalParameters |
| Para birimi yeniden değerleme hesapları | Genel muhasebe &gt; Para birimleri &gt; Para birimi yeniden değerlendirme hesapları | CurrencyLedgerGainLossAccount |
| Otomatik hareketler için hesaplar | Genel muhasebe &gt; Deftere nakil kurulumu &gt; Otomatik hareketler için hesaplar | LedgerSystemAccounts |
| Şirketlerarası muhasebe | Genel muhasebe &gt; Deftere nakil kurulumu &gt; Şirketlerarası hesaplar | LedgerIntercompany |
| Hareketin deftere nakil tanımı | Genel muhasebe &gt; Nakil kurulumu &gt; Hareket deftere nakil tanımları | JournalizingDefinitionTrans |
| Deftere nakil tanımları | Genel muhasebe &gt; Nakil kurulumu &gt; Deftere nakil tanımları | JournalizingDefintion |
| Deftere nakil (Stok) | Stok Yönetimi &gt; Kurulum &gt; Deftere nakil &gt; Deftere nakil | InventPosting |
| Maliyet türü kodları | Varış yeri maliyeti &gt; Maliyetlendirme kurulumu &gt; Maliyet türü kodları | ITMCostTypeTable |
| Kaynaklar | Üretim denetimi &gt; Kurulum &gt; Kaynaklar &gt; Kaynaklar | WrkCtrTable |
| Kaynak grupları | Üretim denetimi &gt; Kurulum &gt; Kaynaklar &gt; Kaynaklar grupları | WrkCtrResourceGroup |
| Üretim grupları | Üretim kontrolü &gt; Kurulum &gt; Üretim &gt; Üretim grubu | ProdGroup |
| Maliyet kategorileri | Üretim kontrol &gt; Kurulum &gt; Rotalar &gt; Maliyet kategorileri | ProjCategory |
| Proje grupları | Proje yönetimi ve muhasebe &gt; Kurulum &gt; Deftere nakil &gt; Proje grupları | ProjGroup |
| Genel muhasebeye nakil ayarı (Projeler) | Proje yönetimi ve muhasebe &gt; Kurulum &gt; Deftere Nakil &gt; Deftere Nakil kurulumu | ProjPosting |
| Giderler için varsayılan mahsup hesaplar | Proje yönetimi ve muhasebe &gt; Kurulum &gt; Deftere nakil &gt; Giderler için varsayılan mahsup hesaplar | ProjDefaultOffsetSetup |
| İndirim yönetimi deftere nakil profilleri | İndirim yönetimi &gt; İndirim yönetimi deftere nakil kurulumu &gt; İndirim yönetimi deftere nakil profilleri | TAMRebatePosting |
| Genel muhasebe deftere nakil grubu (Vergi) | Vergi &gt; Kurulum &gt; Satış vergisi &gt; Genel muhasebe deftere nakil grubu | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Hareketler var olduktan sonra grupları değiştirme

Ana verilerdeki grupları değiştirirken dikkatli olun. Deftere nakil profillerinizi tanımlamak için grupları kullanıyorsanız, bir ana kayıttaki bir grupta yapılan herhangi bir değişiklik, genel muhasebeye mutabakat yeteneği üzerinde olumsuz etkiye sahip olabilir. Örneğin, her madde grubu için farklı bir gelir hesabı kullanılacak şekilde, satış siparişi geliri için stok deftere nakil profilini konfigüre edebilirsiniz. Hareketler varolduktan sonra bir maddeye atanan madde grubunu değiştirirseniz, yeni hareketlerdeki gelir güncelleştirilmiş hesaba nakledilir. Ancak, değişiklikten önce deftere nakledilen gelir orijinal hesapta kalacaktır.

## <a name="testing-posting-profiles"></a>Deftere nakil profillerini test etme

Etkinleştirmeden önce ve deftere nakil profilinize veya ilgili parametrelerinize herhangi bir değişiklik veya ekleme yaptıktan sonra, her bir senaryoyu sınamanız gerekir. Deftere nakil işlemi doğru şekilde çalıştığını doğrulamak için en azından her bir deftere nakil türünü sınamanız gerekir. Ancak, önerilen yaklaşım her bir deftere nakil profili hareketini ve kombinasyonunu test etmektir.

Örneğin, her birinin müşteri gruplarına özel üç kaydı olan iki müşteri deftere nakil profiliniz vardır. Bu durumda, her hareket türünü test etmelisiniz.

**Deftere nakil profilleri:**

- **GEN** – Çalışanlar için bir, müşteriler için bir, şirketlerarası için bir grubu olan genel deftere nakil profili. Her grup, farklı bir Alacak hesabı Ticari hesabına işaret eder.
- **PRE** – Müşteri ön ödeme hesaplarına işaret eden tüm ön ödemeler için tek bir kayıt bulunan ön ödeme deftere nakil profili.

### <a name="testing-scenarios"></a>Test senaryoları

- **GEN** deftere nakil profilini kullanan **Çalışan** grubundaki bir müşteri için serbest metin faturası
- **PRE** deftere nakil profilini kullanan **Çalışan** grubundaki bir müşteri için serbest metin faturası
- **GEN** deftere nakil profilini kullanan **Çalışan** grubundaki bir müşteri için satış siparişi faturası
- **PRE** deftere nakil profilini kullanan **Çalışan** grubundaki bir müşteri için satış siparişi faturası
- **GEN** deftere nakil profilini kullanan **Çalışan** grubundaki bir müşteri için müşteri ödeme günlüğü
- **PRE** deftere nakil profilini kullanan **Çalışan** grubundaki bir müşteri için müşteri ödeme günlüğü

Önceki örnek için, her müşteri grubu için bir test senaryosu tekrarlayın ve her bir ek hareket türü (örneğin, proje faturaları ve servis yönetimi) için her test senaryosu grubunu yineleyin.

## <a name="reconciling-the-ledger-to-the-subledger"></a>Yardımcı defterin genel muhasebeye yeniden mutabakatını sağlama

Genel muhasebenin, her dönem için yardımcı deftere mutabakatı sağlanmalıdır. Birçok modül, bu mutabakata yardımcı olmak için kullanıma hazır, yerleşik raporlar içerir. Ancak, yerel gereksinimlerinize göre özel raporlar geliştirmek veya varolan raporları, raporlama gereksinimlerinizi karşılayacak şekilde genişletmeniz gerekebilir.

Bir sahte dönem kapanışı yapmanız ve tüm yardımcı defterlerin her birini genel muhasebe ile yapılan etkin dönemlere göre mutabakatını sağlamanızı öneririz. Ayrıca, etkinleştirme öncesinde tüm açık bakiyelerin ve açık hareketlerin sahte bir servise almasını yapmanız önerilmektedir. Bu işlemin bir parçası olarak, bakiyelerin ve açık hareketlerin eski sistemlerle dengelenip dengelenmemesini sağlamak için tam bir mutabakat çalıştırmanız ve yeni hareketler oluşturulmadan önce tüm yardımcı defterler için genel muhasebe bakiyesi yapmanız gerekir.
